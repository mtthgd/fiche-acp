---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 2G_séquençage
  - IonTorrent
  - emPCR
  - pHmètre
  - puce_semiconducteur
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Séquençage Ion Torrent

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_515 Séquençage 2G - points communs]] | [[16_516 Pyroséquençage 454 Roche]] | [[16_518 Séquençage Illumina]] | [[16_520 Séquençage 2G - capture et amplicons]]

## Principe général

**Ion Torrent** (Thermo Fisher, plates-formes **Ion PGM**, **Ion Proton**, **Ion S5**) repose sur la détection d’un **ion H+** libéré à chaque incorporation d’un nucléotide par la polymérase. Aucune chimie fluorescente n’est nécessaire : la mesure est **électrique** sur une **puce semi-conductrice** dérivée des capteurs photo numériques.

> Concept : « **Ion Torrent = pH-mètre** ». Chaque puits = un mini pH-mètre haute résolution.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p02_00.jpeg)

## Étapes techniques

### Étape 1 — Préparation de la librairie
Identique aux principes de [[16_515 Séquençage 2G - points communs]] : fragmentation ~200-400 pb + ligation des adaptateurs.

### Étape 2 — Amplification clonale (emPCR)
- **PCR en émulsion** sur bille (Ion Sphere Particle, ISP), **strictement identique** au principe **454**
- 1 bille = milliers de copies identiques d’une matrice unique

### Étape 3 — Distribution dans les puits de la puce
- **Puce semi-conductrice** Ion Chip (314, 316, 318, **520, 530, 540, 550 selon la plate-forme**)
- **1 bille par puits** déposée par centrifugation
- Sous chaque puits : un **transistor à effet de champ ISFET** mesurant le pH

### Étape 4 — Cycle de séquençage
À chaque cycle, **un seul nucléotide** (A, T, C ou G) est introduit dans tous les puits :
- Si incorporation → **libération d’H+** → **chute de pH** → **courant électrique** détecté par l’ISFET
- Si non incorporation → pH stable → nucléotide non intégré

**Linéarité du signal** : un homopolymère **AA** donne un pic 2× plus grand que **A**. Bonne linéarité jusqu’à **5-6 bases identiques**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p04_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p06_00.png)

| Étape | Détail | Outil/Plate-forme |
|---|---|---|
| Fragmentation | 200-400 pb | Mécanique / enzymatique |
| Amplification | **emPCR** sur ISP | Émulsion |
| Distribution | 1 bille / puits | **Ion Chip** (semi-conducteur) |
| Détection | **Variation de pH (H+)** | **ISFET** sous chaque puits |
| Acquisition | **Courant électrique** | Pas de chimie fluo, pas de caméra |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p07_00.jpeg)

## Spécifications / Métriques

| Plate-forme | Reads | Débit | Indication |
|---|---|---|---|
| **Ion PGM** (314/316/318) | ~200-400 pb | 30 Mb à 2 Gb / run | Petits panels |
| **Ion Proton** | ~200 pb | ~10 Gb / run | Exomes |
| **Ion S5 / S5 XL** (chips 520-550) | 200-400 pb | 0,3 à 25 Gb / run | Routine clinique |

| Métrique | Ion Torrent |
|---|---|
| Longueur de read | **200-400 pb** |
| Précision | ~99,5 % sur bases isolées |
| Temps de run | **2-4 h** (le plus rapide des 2G) |
| Coût/base | Économique (pas de fluo) |

## Indications / Applications

- **Panels ciblés en oncologie somatique** (ex. Oncomine Focus, Comprehensive)
- Routine clinique en **pathologie moléculaire** (poumon, colon, mélanome…)
- **TMB** : kit dédié **Oncomine Tumor Mutation Load** (cf [[16_560 Évaluation de la charge mutationnelle (TMB)]])
- Idéal pour des panels < 50 gènes en TAT court

## Avantages / Limites

| Avantages | Limites |
|---|---|
| **Pas de chimie fluorescente** → coût ↓ | **Erreur sur les homopolymères ≥ 6** → décalage de séquence (indels artefactuels) |
| **Run très rapide** (2-4 h) | Reads courts (200-400 pb) |
| Chimie **naturelle** (pas de nucléotides modifiés) | Précision en deçà d’Illumina |
| Puces semi-conductrices = scalabilité industrielle | Pas adapté à un débit massif type Illumina NovaSeq |
| Détection électrique = appareils plus compacts | emPCR longue à mettre en œuvre |

> **Piège diagnostic** : devant un indel suspect dans un homopolymère sur un run Ion Torrent, **vérifier en Sanger** ou par une autre technologie (Illumina) — risque de **faux positif**.

---

## 🔑 Points clés à retenir

1. **Ion Torrent** = pH-mètre semi-conducteur, détecte un **ion H+** par incorporation.
2. Plates-formes : **Ion PGM**, **Ion Proton**, **Ion S5** (chips 520/530/540/550).
3. Amplification par **emPCR** sur **Ion Sphere Particle** (1 bille / 1 fragment).
4. **1 bille / 1 puits** sur la puce, transistor **ISFET** sous chaque puits.
5. Nucléotides présentés **un à un** (A, T, C, G), **chimie naturelle** (pas de fluo).
6. Linéarité du pH → mesure du nb de bases incorporées (jusqu’à **5-6 homopolymère**).
7. **Erreur majeure sur homopolymères ≥ 6** → indels artefactuels — **vérifier en Sanger**.
8. **Run rapide** (2-4 h), **coût modéré** — adapté aux **panels ciblés en routine**.
9. Reads **200-400 pb**.
10. Plate-forme couramment utilisée en pathologie moléculaire pour panels théranostiques (poumon, côlon, mélanome).
