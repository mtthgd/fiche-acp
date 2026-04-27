---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - bioinformatique
  - pipeline
  - alignement
  - BWA
  - GATK
  - VCF
  - BAM
  - FASTQ
  - variant_calling
  - annotation
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Le pipeline bioinformatique

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_515 Séquençage 2G - points communs]] | [[16_518 Séquençage Illumina]] | [[16_520 Séquençage 2G - capture et amplicons]] | [[16_560 Évaluation de la charge mutationnelle (TMB)]] | [[16_550 NGS 3ème génération]] | [[16_190 Bases publiques de variants]]

## Principe général

La **bioinformatique** est née de la rencontre entre la **biologie** et l’**informatique** pour analyser le **boom quantitatif** des données génomiques.

Un **pipeline bioinformatique** (ou **workflow**) est un **ensemble de logiciels exécutés en série** : la sortie de chaque logiciel sert d’**entrée** au suivant.

```
Données séquenceur → [LOG 1] → [LOG 2] → [LOG 3] → … → [LOG N] → Résultats
```

Ce pipeline est **indispensable** pour exploiter les données brutes d’un séquenceur NGS et permet :
- **Automatisation** (gain de temps, moins d’intervention humaine)
- **Reproductibilité** (mêmes paramètres pour tous les échantillons d’un projet)
- **Standardisation** au sein d’un panel diagnostique en routine





## Workflow d’un séquençage NGS en pathologie

| Étape | Phase | Acteur |
|---|---|---|
| 1 | **Examen morphologique** (% cellules tumorales) | Pathologiste |
| 2 | **Extraction & qualification** ADN | Technicien |
| 3 | Préparation **librairie** + amplification | Technicien |
| 4 | **Séquençage** sur instrument | Séquenceur |
| 5 | **Pipeline bioinformatique** | Bioinformaticien |
| 6 | **Visualisation, interprétation, compte rendu** | Pathologiste / biologiste |



## Données du séquenceur (en amont du pipeline)

Le séquenceur acquiert le **signal** (ex. flash de fluorescence Illumina via prise de photo) puis effectue le **base-calling** :
- **Convertit** chaque signal en nucléotide (A/T/C/G)
- Associe à chaque base un **score de qualité** **Phred** (probabilité d’erreur)

Format de sortie initial : **BCL** (Illumina) → converti en **FASTQ**.

## Étape 1 — Démultiplexage et trimming

**Logiciel 1** : `bcl2fastq`, **Demultiplex**, **Trimmomatic**, **Cutadapt**

| Action | Description |
|---|---|
| **Démultiplexage** | Réattribue chaque read à son **patient** d’origine grâce à son **index/barcode** |
| **Trimming** | Supprime les **séquences d’adaptateurs** restantes en bout de read |

**Sortie** : un **fichier FASTQ par échantillon** (1 patient = 1 ou 2 fichiers FASTQ pour paired-end).

> **FASTQ (Sequence with Quality)** = format texte contenant la séquence + le score qualité Phred caractère par caractère.

![[assets/pathologie-moleculaire/ngs/16 535 le pipeline bioinformatique/p03_02.jpeg]]




## Étape 2 — Alignement

**Logiciels** : **BWA** (Burrows-Wheeler Aligner), **Bowtie2**, **STAR** (RNA), **HISAT2**

| Entrée | FASTQ |
|---|---|
| Action | Aligner chaque read sur un **génome de référence** (ex. **GRCh38 / hg38**) |
| **Sortie** | **BAM (Binary Alignment Map)** — version binaire compressée du SAM |

Étapes complémentaires post-alignement :
- **Sort** + **index** (samtools)
- **Mark duplicates** (Picard MarkDuplicates) — supprime les duplicates PCR
- **Recalibration des scores qualité** (BQSR de GATK)
- **Réalignement local** autour des indels



![[assets/pathologie-moleculaire/ngs/16 535 le pipeline bioinformatique/p04_02.jpeg]]




## Étape 3 — Variant calling

**Logiciels** : **GATK HaplotypeCaller**, **VarScan2**, **MuTect2** (somatique), **Strelka2**, **DeepVariant**

| Entrée | BAM |
|---|---|
| Action | Comparer chaque position du BAM au génome de référence et **lister les variants** |
| Types de variants | **SNV** (single nucleotide variants), **indels** (insertions/délétions), CNV, fusions (modules dédiés) |
| **Sortie** | **VCF (Variant Call Format)** |

> **Variant calling somatique** vs **germinal** :
> - Germinal : 1 BAM (HaplotypeCaller, DeepVariant)
> - Somatique : BAM tumeur + BAM normal apparié (MuTect2, Strelka2)




![[assets/pathologie-moleculaire/ngs/16 535 le pipeline bioinformatique/p05_03.jpeg]]


## Étape 4 — Annotation

**Logiciels** : **Mutalyzer**, **ANNOVAR**, **Ensembl VEP**, **SnpEff**

| Entrée | VCF brut |
|---|---|
| Action | Ajouter à chaque variant des **métadonnées** |
| **Sortie** | **VCF annoté** |

### Informations apportées
- **Nom du gène**, position, exon/intron
- **Nomenclature HGVS** (Human Genome Variation Society) — c.XXX, p.XXX
- **Fréquence allélique populationnelle** (gnomAD, 1000G, ExAC)
- **Pathogénicité** : ClinVar, COSMIC, OncoKB
- **Prédiction in silico** : **PolyPhen-2**, **SIFT**, **CADD**, **REVEL**

Cf [[16_190 Bases publiques de variants]] pour le détail des bases consultées.

## Étape 5 — Filtrage

**Objectif** : ne conserver que les **variants d’intérêt** pour interprétation.

### Filtres typiques (mutations somatiques)
| Filtre | Seuil typique |
|---|---|
| **Qualité du variant** | QUAL > 30 |
| **Profondeur de lecture (DP)** | **≥ 30×** (souvent **≥ 100×** en somatique) |
| **Fréquence allélique (VAF)** | **≥ 5 %** (≥ 1 % si haute profondeur, ctDNA) |
| Brins forward + reverse | Variant vu sur les **2 brins** |
| **Polymorphismes** populationnels | gnomAD < 0,1 % éliminés |
| **Mutations silencieuses** | Exclues (sauf splicing) |
| Bases publiques | ClinVar/COSMIC enrichissent |

### Sortie finale
- **Liste de variants annotés et filtrés**
- Format **VCF filtré**, **TSV/CSV** ouvert dans **Excel** ou interface dédiée
- Permet **interprétation** + **compte rendu**




![[assets/pathologie-moleculaire/ngs/16 535 le pipeline bioinformatique/p06_03.jpeg]]


## Récapitulatif — Workflow et formats de fichiers

```
Séquenceur (.bcl/signal)
       │ base-calling
       ▼
   FASTQ (raw reads + Phred)
       │ démultiplexage + trimming   →   1 FASTQ / patient
       ▼
   BAM (alignement sur génome de référence GRCh38)
       │ MarkDuplicates, BQSR, IndelRealignment
       ▼
   VCF brut (variant calling : SNV + indels)
       │ annotation HGVS, gnomAD, COSMIC, ClinVar
       ▼
   VCF annoté
       │ filtres qualité, VAF, polymorphismes
       ▼
   VCF / TSV final → Visualisation → Interprétation → Compte rendu
```

| Format | Contenu | Étape produite |
|---|---|---|
| **BCL** | Signal brut Illumina | Sortie séquenceur |
| **FASTQ** | Reads + score Phred | Démultiplexage |
| **BAM** | Reads alignés au génome de référence (binaire) | Alignement |
| **VCF (Variant Call Format)** | Liste des variants détectés | Variant calling |
| **VCF annoté** | Variants enrichis (HGVS, fréquences, prédiction) | Annotation |


![[assets/pathologie-moleculaire/ngs/16 535 le pipeline bioinformatique/p12_00.jpeg]]


## Outils logiciels par étape

| Étape | Outils courants |
|---|---|
| **Base-calling / démultiplexage** | bcl2fastq, BCL Convert, MiSeq Reporter |
| **Trimming** | Trimmomatic, Cutadapt, FastP |
| **Contrôle qualité FASTQ** | **FastQC**, MultiQC |
| **Alignement ADN** | **BWA-MEM**, Bowtie2 |
| **Alignement ARN** | STAR, HISAT2 |
| **Variant calling germinal** | **GATK HaplotypeCaller**, DeepVariant, VarScan2 |
| **Variant calling somatique** | **MuTect2**, Strelka2, VarDict |
| **CNV** | CNVkit, GATK CNV, ExomeDepth |
| **Annotation** | **VEP**, **ANNOVAR**, SnpEff |
| **Visualisation** | **IGV** (Integrative Genomics Viewer), Alamut |

## Avantages / Limites des pipelines

| Avantages | Limites |
|---|---|
| **Automatisation** → débit ↑↑, moins d’erreurs humaines | Nécessite un **bioinformaticien** dédié |
| **Reproductibilité** sur série d’échantillons | Mises à jour fréquentes (génome de référence, bases) |
| **Standardisation** indispensable en routine clinique | **Maintenance** + traçabilité des versions |
| **Stockage centralisé** des résultats | **Volumes de données** considérables (To/run) |
| Adaptable à chaque type d’analyse (panel, exome, RNA, fusion) | Validation analytique nécessaire (norme ISO 15189) |

![[assets/pathologie-moleculaire/ngs/16 535 le pipeline bioinformatique/p14_00.png]]

---

## 🔑 Points clés à retenir

1. **Pipeline bioinformatique = workflow** = chaîne de logiciels où la sortie de l’un est l’entrée du suivant.
2. **Workflow standard NGS** : morpho → ADN → librairie → séquençage → pipeline → interprétation → CR.
3. Sortie séquenceur = **signal + base-calling + score qualité Phred** → fichier **FASTQ**.
4. **5 grandes étapes du pipeline** : démultiplexage/trimming → alignement → variant calling → annotation → filtrage.
5. **Formats clés** : **FASTQ** (reads bruts) → **BAM** (alignement) → **VCF** (variants).
6. Logiciels phares : **BWA** (alignement), **GATK / MuTect2 / VarScan2** (calling), **VEP / ANNOVAR** (annotation).
7. Filtres standards somatiques : **DP ≥ 100×, VAF ≥ 5 %**, élimination des polymorphismes (gnomAD).
8. Annotation = **HGVS, ClinVar, COSMIC, gnomAD, prédicteurs** (PolyPhen, SIFT).
9. Le pipeline garantit **reproductibilité, automatisation, standardisation** — essentiel en routine.
10. Visualisation finale par **IGV** ou tableurs ; interprétation par le biologiste/pathologiste pour le CR.
