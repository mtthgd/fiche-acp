---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 3G_séquençage
  - PacBio
  - Nanopore
  - ZMW
  - long_reads
  - single_molecule
date: 2024
source: DES ACP - Pathologie moléculaire
---

# NGS 3ème génération (PacBio, Oxford Nanopore)

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_515 Séquençage 2G - points communs]] | [[16_518 Séquençage Illumina]] | [[16_535 Le pipeline bioinformatique]]

## Principe général

Le **séquençage de 3ᵉ génération** (3G) atteint l’**objectif initial** des NGS : observer **une seule molécule d’ADN** lue par **une seule polymérase** (ou décryptée par un **nanopore**), **sans étape de PCR**.

Deux technologies dominent le marché :
| Technologie | Société | Détection |
|---|---|---|
| **PacBio (Pacific Biosciences)** | PacBio | **Fluorescence** dans nano-puits **ZMW** |
| **Oxford Nanopore (ONT)** | Oxford Nanopore Technologies | **Variation de potentiel de membrane** dans un **nanopore** |



## Technologie 1 — PacBio (SMRT Sequencing)

### Principe — Single Molecule Real Time
- Puce comportant **des millions de nano-puits** appelés **ZMW** (**Zero-Mode Waveguide**)
- **Volume de détection minuscule** : ~**20 zeptolitres** (10⁻²¹ L) — le plus petit volume de détection au monde
- La lecture de fluorescence se fait dans les **20-30 nm les plus inférieurs** du puits, là où se trouve la polymérase
- **Une polymérase immobilisée** au fond de chaque ZMW avec sa **matrice d’ADN**

### Mécanisme d’incorporation
1. Les 4 nucléotides sont marqués avec des **fluorochromes** **liés à la partie γ-phosphate** (et non à la base)
2. Quand la polymérase incorpore un nucléotide → **clivage** au niveau du phosphate α → **PPi marqué libéré** → **flash fluorescent** détecté
3. Le fluorochrome diffuse hors du volume de détection → la lecture du **suivant** redevient possible

> **Avantage clé** : pas de chimie de blocage/déblocage entre cycles → la polymérase travaille **en continu** à sa vitesse naturelle.

### Spécifications
| Métrique | PacBio |
|---|---|
| Longueur de read | **20 000 à 50 000 pb** (jusqu’à 100 kb) |
| Précision **CCS / HiFi** | **>99 %** (consensus circulaire) |
| Précision read brut | ~85-90 % |
| Plate-formes | **Sequel II, Revio** |
| Particularité | **Mode CCS HiFi** : circulariser et lire plusieurs fois → consensus précis |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-550%20Les%20techniques%20%20NGS%20de%203eme%20g%C3%A9n%C3%A9ration/p02_00.jpeg)



## Technologie 2 — Oxford Nanopore (ONT)

### Principe — décryptage par nanopore
- **Pas d’ADN polymérase**, **pas de séquençage par synthèse**
- Le séquençage repose sur un **nanopore** (canal protéique synthétique) inséré dans une **membrane synthétique** résistante à l’électricité (analogue à une membrane cellulaire)
- Une **différence de potentiel** (~−70 mV) est appliquée à travers la membrane
- Quand un brin d’ADN traverse le pore, le **potentiel de membrane varie** selon la nature du **triplet de nucléotides** présent dans le canal à un instant donné (ex. ACC ≠ ACG)
- La **trace électrique** est convertie en séquence par un algorithme de **base-calling deep learning**

### Préparation de l’échantillon
- L’ADN à séquencer **garde sa nature naturelle** (ADN ou ARN)
- Ligation d’un **adaptateur** très affin pour le nanopore
- Une **enzyme « protéine motrice »** :
  - **dénature** l’ADN double brin en simple brin
  - **propulse** la molécule à travers le nanopore à vitesse contrôlée

### Format de la flow cell
- Lame contenant des **milliers à centaines de millions** de **spots**, chacun = membrane percée par 1 nanopore

### Spécifications
| Métrique | Oxford Nanopore |
|---|---|
| Longueur de read | **Plusieurs kb à >100 kb**, voire **2 Mb** (ultra-long reads) |
| Précision read brut | ~95-98 % (s’améliore avec chaque chimie) |
| Plate-formes | **MinION** (USB, portable), **GridION**, **PromethION** |
| Lecture | **Temps réel** — accessible dès la 1ʳᵉ molécule séquencée |
| Particularité | **Détecte les modifications de bases** (méthylation directe) |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-550%20Les%20techniques%20%20NGS%20de%203eme%20g%C3%A9n%C3%A9ration/p04_00.jpeg)


## Comparaison 3G — PacBio vs Nanopore

| Critère | PacBio (SMRT) | Oxford Nanopore (ONT) |
|---|---|---|
| Détection | **Fluorescence** dans **ZMW** | **Variation de potentiel** dans **nanopore** |
| Polymérase | **Oui** (immobilisée) | **Non** (lecture passive du brin) |
| Reads | 20-50 kb (HiFi) | Plusieurs kb à >2 Mb |
| Précision raw | 85-90 % (CCS HiFi >99 %) | ~95-98 % (chimie R10.4) |
| Méthylation | Indirecte | **Directe** (signal modifié) |
| Plate-forme | **Sequel II, Revio** | **MinION (portable USB), PromethION** |
| Coût plate-forme | Élevé | Faible (MinION ~1000 €) |

## Comparaison 2G vs 3G

| Critère | 2G (Illumina, Ion) | 3G (PacBio, ONT) |
|---|---|---|
| Molécule lue | **Cluster** (milliers de copies) | **Molécule unique** |
| **PCR clonale** | **Indispensable** | **Aucune** (donc pas de biais d’amplification) |
| Reads | 100-400 pb | **20 kb à >100 kb** |
| Erreur principale | Substitution Q30 | Indels (réduits par chimie récente) |
| Détection CNV / SV | Limitée (paired-end) | **Excellente** (long reads) |
| Méthylation | Bisulfite nécessaire | **Détection directe** (ONT) |
| Coût/base | **Très bas** | Plus élevé |
| Indications | Panels, exome, génome resequencing | **De novo**, zones répétées, SV complexes |

## Indications

| Indication | Pourquoi 3G ? |
|---|---|
| **Assemblage de novo** d’un génome inconnu | Long reads → assemblage sans référence |
| **Zones répétées** (centromères, télomères, segmental duplications) | Long reads traversent les répétitions |
| **Anomalies structurales complexes** (translocations, inversions, CNV larges) | Couvre les points de cassure |
| **Phasing haplotypique** | Long reads couvrent plusieurs SNP simultanément |
| **Méthylome direct** (ONT) | Pas de bisulfite |
| **Fusions complexes** non détectées en 2G | Long reads adaptés |

> **NGS 2G ou 3G ?** Le 2G reste **excellent pour le re-séquençage ciblé** (oncologie somatique), où le génome humain est connu et les mutations cibles sont bien définies. Le 3G ne **remplacera pas** le 2G — comme la **télévision n’a pas tué la radio**.

## Avantages / Limites

| Avantages 3G | Limites 3G |
|---|---|
| **Single-molecule** : pas de PCR → pas de biais d’amplification | Précision raw plus faible (corrigée par CCS HiFi PacBio) |
| **Reads longs** (10-100 kb, voire Mb) → assemblage de novo | Coût/base supérieur à Illumina |
| Détection des **modifications de bases** (méthylation, ONT) | Pipeline bioinformatique adapté nécessaire (cf [[16_535 Le pipeline bioinformatique]]) |
| Lecture **en temps réel** (ONT MinION → résultats dès la 1ʳᵉ heure) | Maturité variable selon plate-forme |
| Plate-forme **portable** (MinION, ~taille d’une clé USB) | Volumes de données massifs |

---

## 🔑 Points clés à retenir

1. **3G** = lecture d’une **molécule unique**, **sans PCR clonale** — atteint l’objectif initial du NGS.
2. **PacBio** : fluorescence dans des nano-puits **ZMW** (Zero-Mode Waveguide), volume de **20 zeptolitres**.
3. PacBio = polymérase immobilisée, fluorochrome lié au **γ-phosphate**, lu à chaque incorporation.
4. **Mode HiFi (CCS)** : circulariser + relire plusieurs fois → précision **>99 %**.
5. **Oxford Nanopore** : ADN traverse un **nanopore** synthétique, lecture par **variation de potentiel** (triplet de nucléotides).
6. ONT = pas de polymérase, juste une **protéine motrice** qui propulse l’ADN.
7. **MinION** = séquenceur **portable USB** (~1000 €), résultats en **temps réel**.
8. Reads **20-50 kb (PacBio)**, **plusieurs kb à >2 Mb (ONT)** vs **100-400 pb en 2G**.
9. Indications 3G : **assemblage de novo**, zones répétées, anomalies structurales complexes, **méthylation directe** (ONT).
10. Le 3G **ne remplacera pas** le 2G : panels ciblés en routine restent l’apanage du 2G.
