---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 2G_séquençage
  - librairie
  - flow_cell
  - amplification_clonale
  - multiplexage
  - index
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Séquençage de 2ᵉ génération — points communs

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_516 Pyroséquençage 454 Roche]] | [[16_517 Séquençage Ion Torrent]] | [[16_518 Séquençage Illumina]] | [[16_520 Séquençage 2G - capture et amplicons]] | [[16_535 Le pipeline bioinformatique]] | [[16_550 NGS 3ème génération]]

## Principe général

Toutes les plates-formes de **séquençage 2G** partagent **4 étapes obligatoires** :
1. Construction d’une **librairie** (fragmentation + adaptateurs)
2. Fixation **clonale** de molécules uniques sur un **support** (puce, flow cell, bille)
3. **Amplification locale** par PCR (bridge, émulsion) pour rendre le signal détectable
4. **Séquençage en temps réel**, base par base, sur **chaque cluster/bille**

> Pourquoi pas de molécule unique en 2G ? Parce qu’**aucun système classique** (microscope à fluorescence, pH-mètre) ne détecte UNE seule molécule. Il faut un **cluster de milliers de copies identiques** pour amplifier le signal. La détection single-molecule est ce qui définit la **3G** ([[16_550 NGS 3ème génération]]).


![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p02_00.jpeg]]


## Étape 1 — Construction de la librairie

### Fragmentation
- ADN coupé entre **100 et 500 pb** (selon la plate-forme)
- Limite imposée par la **PCR** (efficace sur fragments courts) et la longueur de read maximale en 2G

### Ligation des adaptateurs
À chaque extrémité du fragment d’intérêt, on ligue **deux adaptateurs distincts** comportant :
- une **séquence d’ancrage** complémentaire à la puce/bille (ex. **P5/P7** chez Illumina)
- une **amorce de séquençage** (forward et reverse → permet le **paired-end**)
- un **index / barcode** unique par patient → **multiplexage**

> Analogie : l’ADN fragmenté = planches de bois ; les adaptateurs = fixations qui en font des skis.



![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p04_01.png]]


## Étape 2 — Fixation sur un support

| Plate-forme | Support |
|---|---|
| **Illumina** | **Flow cell** plate, 8 lignes (lanes) recouvertes d’oligos P5/P7 covalents |
| **Ion Torrent / 454** | **Billes** recouvertes d’oligos, distribuées dans des **puits** d’une plaque |

Le support porte des oligos covalents complémentaires des adaptateurs P5 / P7 → l’ADN s’ancre **par hybridation**.

### Quantification de la librairie
La **dilution** doit être parfaite :
- Trop concentré → clusters fusionnés, **caméra incapable de discriminer**
- Trop dilué → surface gaspillée, **coût/base augmenté**

> Comparaison de l’ingénieur David Grand : c’est comme un **ensemencement de boîte de Petri**.

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p07_00.jpeg]]


![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p08_00.jpeg]]

## Étape 3 — Amplification clonale locale

Chaque molécule unique est amplifiée **in situ** en quelques milliers de copies identiques :

| Technologie | Plate-forme |
|---|---|
| **Bridge PCR** (pont) | **Illumina** — amplification sur la flow cell |
| **PCR en émulsion (emPCR)** | **Roche 454**, **Ion Torrent** — gouttes huile/eau, 1 bille + 1 fragment par micelle |

Le résultat est un **cluster** (Illumina) ou une **bille « cheveux longs »** (454/Ion) portant des milliers de copies identiques à la matrice initiale.

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p09_00.png]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p10_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p10_01.jpeg]]


![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p10_03.jpeg]]

## Étape 4 — Séquençage de chaque cluster

Chaque cluster est lu **base par base, en temps réel**, en parallèle de tous les autres → produit un **read** par cluster.

3 chimies de détection (cf [[16_510 Principes du séquençage massif parallèle]]) :
- **454 Roche** → lumière (PPi + luciférase) ([[16_516 Pyroséquençage 454 Roche]])
- **Ion Torrent** → variation de pH (H+) ([[16_517 Séquençage Ion Torrent]])
- **Illumina** → fluorescence avec **terminateurs réversibles** ([[16_518 Séquençage Illumina]])

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p11_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p11_01.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p11_02.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p11_03.jpeg]]

## Multiplexage par index / barcode

Chaque patient reçoit un **index** unique (ex. ATCGTCAT) ligué dans l’adaptateur :
- ADN de Mme Dupont = index **ATCGTCAT**
- ADN de M. Durand = index **CGTAACGT**

Tous les patients sont **mélangés** sur la flow cell → après séquençage, le pipeline bioinformatique **démultiplexe** chaque read selon son barcode → un **fichier FASTQ par patient**.

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p12_00.png]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p12_01.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p13_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-515 Le séquençage de deuxième génération, les points communs audio pdf/p14_00.jpeg]]

## Spécifications & métriques communes

| Métrique | 2G typique |
|---|---|
| Longueur de read | **100-400 pb** |
| Nombre de réactions simultanées | **>100 000** (souvent millions) |
| Système de détection | Capteur digital (caméra ou pH semi-conducteur) |
| Lecture | **Quantitative** (intensité ∝ nb de matrices) |
| Format de sortie | **FASTQ** (raw reads + score qualité) |

## Avantages / Limites des 2G

| Avantages | Limites |
|---|---|
| Massif, multiplexable, automatisé | Nécessite **PCR clonale** → biais d’amplification (GC, longueur) |
| Très bon rapport coût/base | **Reads courts** → zones répétées difficiles à assembler |
| Détection de clones rares avec profondeur élevée | Préparation de librairie longue et délicate |
| Quantitatif (CNV par profondeur de couverture) | Quantification précise indispensable (sinon clusters fusionnés) |

## Tableau récapitulatif des plates-formes 2G

| Plate-forme | Support | Amplification | Détection | Reads | Spécificité |
|---|---|---|---|---|---|
| **454 Roche** (arrêt commercial 2016) | Bille / puits | **emPCR** | **Lumière** (PPi + luciférase) | ~700 pb | 1ʳᵉ plate-forme historique |
| **Ion Torrent** | Bille / puits | **emPCR** | **pH** (H+) | 200-400 pb | Pas de chimie fluo, économique |
| **Illumina** | **Flow cell** | **Bridge PCR** | **Fluorescence** + terminateurs réversibles | 2×150 à 2×300 pb | Le + utilisé en routine |

---

## 🔑 Points clés à retenir

1. **4 étapes communes** : librairie → fixation → amplification clonale → séquençage en temps réel.
2. La 2G **n’est pas du single-molecule** : elle nécessite un **cluster** de milliers de copies pour détecter le signal.
3. **Librairie** = ADN fragmenté **100-500 pb** + adaptateurs (P5/P7 chez Illumina) + index.
4. **Adaptateurs** apportent : ancrage à la puce + amorces forward/reverse + index pour multiplexage.
5. **Bridge PCR** (Illumina) vs **emPCR** (454, Ion Torrent) — toujours une **amplification locale**.
6. **Quantification précise** de la librairie = critique (clusters trop denses = caméra aveugle).
7. **Index/barcode** → **multiplexage** de plusieurs patients sur une même flow cell.
8. Reads 2G : **100-400 pb**, vs **>20 kb** pour la 3G.
9. Sortie = **FASTQ** par patient après démultiplexage.
10. La 2G permet une **lecture quantitative** (la profondeur reflète le nombre de matrices initiales).
