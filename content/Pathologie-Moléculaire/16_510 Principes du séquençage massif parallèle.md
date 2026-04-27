---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 2G_séquençage
  - 3G_séquençage
  - séquençage_Sanger
  - principes_NGS
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Principes du séquençage massif parallèle (NGS)

> Liens : [[16_515 Séquençage 2G - points communs]] | [[16_516 Pyroséquençage 454 Roche]] | [[16_517 Séquençage Ion Torrent]] | [[16_518 Séquençage Illumina]] | [[16_520 Séquençage 2G - capture et amplicons]] | [[16_535 Le pipeline bioinformatique]] | [[16_550 NGS 3ème génération]]

## Principe général

**NGS = Next Generation Sequencing**, terme historique apparu en 2008 — préférer aujourd’hui **séquençage massif et parallèle (SMP)**, voire **massif parallèle et en temps réel**.

| Génération | Période | Principe |
|---|---|---|
| **1G — Sanger** | 1980 (Prix Nobel) | Terminateurs de chaîne (**ddNTP**) en solution, analyse en point final |
| **2G — NGS** | 2007–2008 → actuel | Détection **base par base en temps réel** d’une polymérase clonale (PCR-amplifiée) |
| **3G** | 2016–2017 → | Détection sur **molécule unique** (PacBio, Oxford Nanopore) |


## Rappel — Action de l’ADN polymérase

L’**ADN polymérase** assure une **liaison phosphodiester** covalente entre le **3’-OH** du désoxyribose précédent et le phosphate (α) du **dNTP** entrant. Elle nécessite :
- une **matrice simple brin**
- une **amorce** (impossible de partir d’ADN double brin direct)
- des **dNTP** (A, T, C, G)

Lors de chaque incorporation **2 sous-produits** sont libérés :
- une **molécule de pyrophosphate (PPi)** — exploitée par le **pyroséquençage 454**
- un **ion H+** — exploité par **Ion Torrent**


![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p03_01.jpeg]]



## Séquençage de 1ʳᵉ génération — Sanger

Méthode enzymatique utilisant des **ddNTP** (didésoxyribonucléotides) **terminateurs de chaîne** : absence de **3’-OH** → la polymérase ne peut plus former de liaison phosphodiester.

Mélange dans 4 tubes (un par base) → fragments de tailles variables → **migration électrophorétique base à base** → reconstitution de la séquence.

- Réaction **en solution**
- Analyse **en point final**, **non en temps réel**
- Reads ≈ 800-1000 pb avec haute qualité

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p04_01.png]]






![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p05_02.jpeg]]

## Séquençage de 2ᵉ génération — principe en temps réel

L’opérateur **propose** successivement A, T, C, G à la polymérase et **enregistre** quel nucléotide a été incorporé. La séquence des nucléotides intégrés constitue un **read** (séquence d’une molécule d’ADN).

> Un **read** en 2G fait typiquement **100 à 400 bases**.
> En 3G, on atteint **plusieurs milliers à plusieurs centaines de milliers de bases**.

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p07_00.png]]

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p08_00.jpeg]]


## Trois technologies 2G — trois modes de détection

| Sous-produit | Détecté par | Plate-forme |
|---|---|---|
| **PPi** + sulfurylase + luciférase → **lumière** | Capteur photonique | **Pyroséquençage 454 Roche** |
| **Ion H+** → variation de **pH** | pH-mètre semi-conducteur | **Ion Torrent** |
| Nucléotide marqué **fluorescent** | Caméra haute définition | **Illumina** |

Code couleur Illumina : **A rouge, C jaune, G vert, T bleu** (un flash bleu = T incorporé).

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p11_00.jpeg]]



![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p13_00.jpeg]]

## Le caractère « massif et parallèle »

On ne lit pas **une** polymérase, mais des **dizaines à des millions** simultanément, sur :
- une **flow cell** (Illumina) → **clusters spatialement adressables** (X,Y)
- des **billes** distribuées dans des puits (454, Ion Torrent)

Ensemble des reads → fichier brut **FASTQ** (raw data).

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p15_00.png]]



![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p17_00.jpeg]]



## Prérequis techniques communs

1. **Sortir de la solution** : immobiliser l’ADN sur un support physique (puce, lame, bille)
2. **Amplification clonale locale** par PCR (bridge, émulsion) → milliers de copies identiques d’une molécule unique
3. **Détection adressable** par capteur (caméra ou pH-mètre haute résolution)
4. **Synchronisation** : cycle par cycle, base par base

## Comparaison synthétique 1G / 2G / 3G

| Critère | Sanger 1G | NGS 2G | 3G (PacBio/Nanopore) |
|---|---|---|---|
| Réaction | Solution | Support solide + PCR clonale | Molécule unique, sans PCR |
| Détection | Point final | **Temps réel** | **Temps réel, single molecule** |
| Longueur de read | 800-1000 pb | **100-400 pb** | **20 kb à >100 kb** |
| Débit | Faible (1 fragment/capillaire) | **Massif et parallèle** | Massif, single molecule |
| Coût/base | Élevé | Faible | Intermédiaire |
| Utilisation | Validation, ponctuel | Routine clinique | De novo, longs reads |

## Indications cliniques

- **Onco-somatique ciblée** : panels NGS (mutations EGFR, KRAS, BRAF, IDH, etc.)
- **Constitutionnel** : prédispositions héréditaires (BRCA, syndromes de Lynch…)
- **Exome / génome entier** : recherche, maladies rares
- **Détermination de la TMB**, **MSI**, **fusion** sur ARN ([[16_535 Le pipeline bioinformatique]], [[16_560 Évaluation de la charge mutationnelle (TMB)]])

## Avantages / Limites

| Avantages | Limites |
|---|---|
| Massif, parallèle, en temps réel | Nécessite **PCR clonale** (sauf 3G) → biais d’amplification |
| Détection de **clones rares** (sensibilité ↑ avec la profondeur) | Reads courts (2G) → assemblage difficile sur zones répétées |
| Multiplexage (index/barcode) → coût/échantillon ↓ | Pipeline **bioinformatique** lourd ([[16_535 Le pipeline bioinformatique]]) |
| Quantitatif (CNV par profondeur) | Investissement initial élevé |

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p21_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-510 Les grands principes du sequençage massif et parallele/p21_01.png]]



---

## 🔑 Points clés à retenir

1. Préférer **séquençage massif et parallèle** au terme NGS — actuel = 2ᵉ génération.
2. **1G Sanger** = ddNTP terminateurs en solution, **point final** ; 2G/3G = détection **base par base en temps réel**.
3. La polymérase libère à chaque incorporation un **PPi**, un **ion H+** et incorpore un nucléotide → 3 modes de détection : **lumière** (454), **pH** (Ion Torrent), **fluorescence** (Illumina).
4. Un **read** = séquence d’une molécule d’ADN ; **100-400 pb en 2G**, plusieurs **kb à 100 kb en 3G**.
5. Le caractère **massif** repose sur l’immobilisation et l’amplification clonale locale (cluster Illumina, bille 454/Ion Torrent).
6. **Multiplexage** par **index/barcodes** → mélange de patients sur une même flow cell.
7. **Ensemble des reads = FASTQ** (données brutes) → entrée du pipeline bioinformatique.
8. Sensibilité = profondeur ; **détection de clones rares** impossible en Sanger.
9. **3G** = lecture d’une molécule unique sans PCR (PacBio ZMW, nanopore).
10. La 2G **n’a pas tué** Sanger (validation), la 3G ne **tuera pas** la 2G (panels ciblés robustes).
