---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 2G_séquençage
  - Illumina
  - bridge_PCR
  - flow_cell
  - terminateurs_réversibles
  - paired_end
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Séquençage Illumina

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_515 Séquençage 2G - points communs]] | [[16_516 Pyroséquençage 454 Roche]] | [[16_517 Séquençage Ion Torrent]] | [[16_520 Séquençage 2G - capture et amplicons]] | [[16_535 Le pipeline bioinformatique]]

## Principe général

**Illumina** est aujourd’hui la technologie 2G **la plus utilisée** dans les laboratoires de routine clinique et de recherche. Sa chimie est très proche de **Sanger** : elle utilise des nucléotides à **terminateurs de chaîne réversibles** marqués par **fluorescence**, à 4 couleurs distinctes.

| Plate-forme | Cible | Débit |
|---|---|---|
| **MiniSeq, iSeq** | Petits panels | 1-7 Gb |
| **MiSeq** | Panels ciblés, métagénomique | 0,3-15 Gb |
| **NextSeq 550 / 1000 / 2000** | Exomes, panels larges | 30-360 Gb |
| **HiSeq 2500/4000** (historiques) | Exome, génome | 1 Tb |
| **NovaSeq 6000 / X** | **WGS, exomes en routine** | jusqu’à **6 Tb** / run |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p02_00.jpeg)

## Étapes techniques

### Étape 1 — Librairie
Fragmentation 200-500 pb + ligation des **adaptateurs P5/P7** + index (cf [[16_515 Séquençage 2G - points communs]]).

### Étape 2 — Hybridation sur la flow cell
- La **flow cell** est une lame de verre comportant **plusieurs lignes (lanes)** sur lesquelles sont fixés de manière covalente des oligos complémentaires de **P5** et **P7**
- Chaque fragment de la librairie s’hybride par **un de ses adaptateurs**

### Étape 3 — Amplification clonale par bridge PCR
- L’extrémité libre du fragment se **plie** et hybride **un autre oligo** de la flow cell → formation d’un **pont (bridge)**
- Une polymérase synthétise le brin complémentaire → après dénaturation, **2 molécules attachées** localement
- Cycles successifs → **cluster local** de **milliers de copies identiques**, parfaitement adressable en X,Y
- **Clivage spécifique** pour ne garder que les brins **forward** avant la 1ʳᵉ lecture

### Étape 4 — Séquençage par synthèse (SBS) — lecture forward
- 1ʳᵉ amorce de séquençage hybridée
- À chaque cycle, les **4 nucléotides fluorescents avec terminateur réversible** sont injectés **simultanément**
- Le nucléotide complémentaire s’incorpore, **bloque** la chaîne (terminateur réversible) → un seul nucléotide par cycle
- **Caméra haute définition** lit la **fluorescence** sur l’ensemble de la flow cell, par cluster (X,Y)
- **Clivage chimique** : suppression du **fluorochrome** + suppression du **bloqueur** → cycle suivant

### Étape 5 — Lecture des index puis lecture reverse (paired-end)
- Lecture **index 1** puis **index 2** (multiplexage)
- Repolymérisation, lecture du **brin reverse** par l’autre extrémité → **paired-end sequencing**

### Étape 6 — Bioinformatique
Reads forward + reverse → alignés sur génome de référence (cf [[16_535 Le pipeline bioinformatique]]).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p04_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p06_00.png)

| Étape | Détail | Outil |
|---|---|---|
| Librairie | Adaptateurs P5/P7 + index | Ligation |
| Fixation | Sur **flow cell** (oligos covalents) | — |
| Amplification | **Bridge PCR** in situ → cluster local | Pas d’émulsion |
| Détection | **Fluorescence** 4 couleurs | Caméra HD |
| Particularité | **Terminateurs réversibles** (1 base/cycle) | Chimie sanguinière modifiée |
| Lecture bidirectionnelle | **Paired-end** (forward + reverse) | Compense la perte de qualité en fin de read |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p07_00.jpeg)

## Spécifications / Métriques

| Métrique | Illumina |
|---|---|
| Longueur de read | **2 × 75 à 2 × 300 pb** (paired-end) |
| Précision | **>99,9 %** (Q30) |
| Débit | 1 Gb (MiSeq) à **6 Tb** (**NovaSeq X**) / run |
| Format de sortie | **BCL** → **FASTQ** |
| Particularité | **Pas d’erreur sur homopolymères** (terminateurs réversibles) |

## Indications / Applications

- **Panels ciblés** théranostiques en cancérologie
- **Exomes**, **génomes**, **transcriptomes**
- **TMB** (kits **TruSight Oncology 500**, cf [[16_560 Évaluation de la charge mutationnelle (TMB)]])
- **Single-cell sequencing**, **ChIP-seq**, **methylome**
- Plate-forme **dominante** dans les plateformes onco-moléculaires françaises et internationales

## Avantages / Limites

| Avantages | Limites |
|---|---|
| **Pas de problème d’homopolymère** (1 base / cycle, blocage réversible) | Reads **plus courts** que 454/3G |
| **Précision Q30 > 99,9 %** — la meilleure des 2G | **Bruit de fond** au-delà de **~200 bases** (chimie de clivage imparfaite) |
| **Paired-end** compense la perte de qualité aux extrémités | Run plus long (24-48 h selon plate-forme) |
| Multiplexage massif (centaines d’échantillons par run) | Investissement initial très élevé (NovaSeq) |
| Écosystème logiciel mature, BaseSpace, DRAGEN | Dépendance à un fournisseur unique |

> Mécanisme du bruit de fond : la chimie de **déprotection du fluorophore** + **levée du blocage** n’est jamais à 100 %. Au fil des cycles, les molécules d’un cluster se **désynchronisent**, dégradant la qualité après ~200-300 bases. Le **paired-end** compense en re-séquençant l’autre extrémité.

---

## 🔑 Points clés à retenir

1. **Illumina** = plate-forme NGS 2G **dominante** en routine clinique (MiSeq → **NovaSeq**).
2. Détection par **fluorescence** 4 couleurs avec **terminateurs réversibles** (« Sanger amélioré, base par base »).
3. Amplification clonale **in situ par Bridge PCR** sur **flow cell** (pas d’émulsion).
4. **1 nucléotide par cycle** → **pas d’erreur sur homopolymères** (avantage ++ vs Ion Torrent).
5. **Paired-end** : lecture **forward + reverse** compense la perte de qualité en fin de read.
6. **Bruit de fond** au-delà de ~200 bases (chimie de clivage non 100 %).
7. **Précision Q30 > 99,9 %** — la meilleure des 2G.
8. Adaptateurs **P5/P7** + **index 1 et 2** pour multiplexage massif.
9. Sortie : **BCL** → conversion en **FASTQ** par démultiplexage.
10. Indications : **panels théranostiques, exomes, génomes, TMB, RNA-seq, single-cell**.
