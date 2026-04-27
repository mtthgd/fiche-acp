---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - connaissances_fondamentales
  - instabilité_génétique
  - MSI
  - charge_mutationnelle
  - CGH
  - NGS
  - CNV
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Instabilité génétique

> Liens : [[16_210 Oncogènes et gènes suppresseurs de tumeurs]] | [[16_260 Réparation des lésions de l'ADN]] | [[16_280 Modifications épigénétiques - Méthylation de l'ADN et histones]] | [[16_510 Principes du séquençage massif parallèle]] | [[16_1035 Statut MSI en onco-immunologie]]

## Définitions

- **Stabilité génétique** : transmission **conforme** du matériel génétique de la cellule mère aux cellules filles lors de la division
- **Instabilité génétique** : toute **non-conformité** du matériel transmis ; **propriété inhérente aux cellules cancéreuses**
- Résulte d’un **déséquilibre** entre les altérations de l’ADN et les capacités de réparation

## Mécanismes

### Sources d’altérations

| Origine | Exemples |
|---------|----------|
| **Lésions exogènes** | Agents chimiques, **UV**, rayonnements ionisants |
| **Lésions endogènes** | Mutations spontanées, anomalies de la division cellulaire, défauts de recombinaison |

> Estimation : **~25 000 altérations/jour/cellule humaine**, tous types confondus.

### Devenir des altérations

- **Tolérées** (rare ; ex. répertoire combinatoire des lymphocytes)
- **Réparées** (le plus souvent — voir [[16_260 Réparation des lésions de l'ADN]])
- **Non tolérées** → arrêt du cycle ou **apoptose**

### Origine de l’instabilité génétique

Déséquilibre entre :
- ↑ altérations de l’ADN
- ↓ capacités de réparation
- ou **les deux**


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p04_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p05_00.png)

## Catégories d’instabilité génétique

| Catégorie | Mécanisme | Synonyme |
|-----------|-----------|----------|
| **Instabilité chromosomique** (anomalies du **nombre** ou de **structure**) | Aneuploïdie, translocations, délétions chromosomiques | **CIN** (Chromosomal INstability) |
| **Instabilité génique** | Amplifications, délétions, mutations ponctuelles, **instabilité microsatellitaire (MSI)** | — |
| **Instabilité épigénétique** | Modifications **non structurelles** : méthylation, acétylation | — |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p09_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p10_00.png)

## Outils d’analyse — instabilité chromosomique

### Cytogénétique conventionnelle (années 1960)

- **Caryotype** : largement utilisé pour le diagnostic des **leucémies**

### Cytogénétique moléculaire

- **FISH** (Fluorescent In Situ Hybridization) — y compris **FISH multicolore (M-FISH, SKY)**
- Recherche de **translocations spécifiques** d’une maladie (sarcomes, lymphomes)

### Hybridation génomique

- **CGH-array** (Comparative Genomic Hybridization)
- **SNP-array**
- → Analyses **pangénomiques** des gains et pertes de matériel chromosomique

### Exemples d’application

- **Compilation de 150 cancers du sein** par CGH-array : identification d’**anomalies récurrentes** (gains 1q, 8q, 17q, 20q)
- **Cancers colorectaux** : profils variables d’un même type tumoral — de **génomes stables** à **chaos génomique**
- **Index génomique** : mesure de la fraction de génome avec anomalies du nombre de copies, ou nombre de cassures
- L’instabilité chromosomique survient surtout pendant la **transition adénome → carcinome**, peu entre stade localisé et métastase



![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p13_00.jpeg)

## Outils d’analyse — instabilité génique

### Techniques classiques

- **Séquençage Sanger** (enzymatique)
- **PCR ciblée** : recherche de mutations, pertes alléliques, **MSI** par analyse de fragments

### NGS (séquençage massif parallèle, deuxième génération)

Approches **globales et complètes** sur ADN ou ARN — voir [[16_510 Principes du séquençage massif parallèle]].

#### Application 1 — Charge mutationnelle (TMB)

| Notion | Définition |
|--------|-----------|
| **TMB** (Tumor Mutational Burden) | Nombre total de **mutations + indels** dans le génome tumoral |
| Unité | **Mutations par mégabase** ou par exome |
| Gold standard | **Exome entier (WES)** |
| Pratique courante | **Larges panels** (≥ 300 gènes minimum) |

**But** : identifier les tumeurs **hypermutées** ou **ultramutées**, **très sensibles à l’immunothérapie** (anti-PD1/PD-L1).

**Limites** :
- Nécessite un **pipeline bio-informatique** adapté
- Pas de **seuil universel** de TMB (varie selon le type tumoral et la méthode)

Trousses commerciales (FoundationOne) ou prestations externes.

#### Application 2 — Sous-classification (TCGA)

Dans le **cancer colorectal** :
- Tumeurs avec **TMB élevée** (> 10 mut/Mb) ↔ tumeurs **MSI**
- Tumeurs **ultramutées** (> 40-100 mut/Mb) ↔ déficit de **POLE** (polymérase ε réplicative à activité de relecture)

| Sous-groupe CCR | Caractéristique |
|-----------------|------------------|
| **CIN** (chromosomal instability) | Le plus fréquent ; aneuploïdie ; APC, KRAS, TP53 |
| **CIMP** | Phénotype hyperméthylé |
| **MSI** | Hypermutés (> 10 mut/Mb) |
| **Ultramutés** | **POLE** déficient (> 40-100 mut/Mb) |

#### Application 3 — Analyse des microsatellites par NGS

- Au-delà des **5 marqueurs Pentaplex** classiques (BAT26, BAT25, NR21, NR24, NR27)
- NGS = analyse de **centaines** de microsatellites
- A permis d’identifier la **MSI hors syndrome de Lynch** : ex. **corticosurrénalome**, **mésothéliome**

#### Application 4 — Détection des CNV (Copy Number Variants)

- Recherche d’**amplifications** ou **délétions** sur un panel de gènes
- À partir des données NGS ADN, nécessite une **bio-info dédiée**
- Indications similaires à la **CGH-array** ; **avantages** : analyse simultanée mutations + CNV
- Validation : **mélanomes** (amplification MDM2, délétion CDKN2A), CCR (amplification AKT2, délétion SMAD4) ; corrélation parfaite avec CGH-array

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p15_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p16_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p17_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p18_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p19_00.png)

### Séquençage ARN

- Application principale : **recherche de fusions de gènes** (visée diagnostique ou thérapeutique)
- Premières trousses commerciales : **panels de 50 gènes** (NTRK, ROS, FGFR…)
- Panels élargis (> 500 gènes) → identification de **nouveaux gènes de fusion** (ex. sarcome oropharyngé)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p22_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-270%20Instabilit%C3%A9%20g%C3%A9n%C3%A9tique/p23_00.jpeg)

## Tableau récapitulatif — outils d’analyse

| Type d’instabilité | Niveau analysé | Techniques |
|---------------------|-----------------|------------|
| **Chromosomique** | Caryotype, gains/pertes pangénomiques | Caryotype, FISH, M-FISH, **CGH-array**, **SNP-array** |
| **Génique ciblée** | Mutation, MSI, CNV ciblé | Sanger, **PCR**, fragment analysis (Pentaplex) |
| **Génique pangénomique** | Mutations, indels, CNV, fusions | **NGS** (panels, exome, génome) |
| **Microsatellitaire** | MSI | PCR Pentaplex, **NGS** étendu |
| **Charge mutationnelle (TMB)** | Hypermutation | NGS large panel ou exome |
| **Fusions** | Translocations | FISH, RT-PCR, **NGS ARN** |
| **Épigénétique** | Méthylation | Voir [[16_285 Techniques d'analyse de la méthylation de l'ADN]] |

## Implications cliniques

| Indication | Application |
|------------|-------------|
| **Diagnostic** | Sarcomes (fusions), lymphomes (translocations), MSI dans CCR |
| **Pronostic** | Index génomique, TMB |
| **Thérapeutique** | Choix d’immunothérapie (TMB-élevée, MSI), thérapies ciblées (fusions, mutations actionnables) |

---

## 🔑 Points clés à retenir

1. **Instabilité génétique = propriété inhérente aux cellules cancéreuses** ; ~25 000 altérations/jour/cellule à équilibrer
2. Trois grandes catégories : **chromosomique (CIN)**, **génique** (mutations, MSI), **épigénétique** (méthylation)
3. **Outils chromosomiques** : caryotype, **FISH**, **CGH-array**, **SNP-array**
4. L’instabilité chromosomique survient surtout pendant la transition **adénome → carcinome**
5. **NGS** : approche globale qui révolutionne l’analyse de l’instabilité (TMB, MSI, CNV, fusions)
6. **TMB** = nb mutations/Mb ; tumeurs **hypermutées (> 10)** ou **ultramutées (> 40-100)** = excellent répondeurs à l’**immunothérapie**
7. **CCR** : 4 sous-groupes — **CIN, CIMP, MSI, ultramutés (POLE déficient)**
8. **MSI hors syndrome de Lynch** identifiée par NGS dans corticosurrénalome, mésothéliome
9. **CNV par NGS** = alternative à la CGH-array (mélanome : MDM2 amp, CDKN2A del ; CCR : AKT2 amp, SMAD4 del)
10. **NGS ARN** = méthode de référence pour la recherche de **fusions de gènes** (NTRK, ROS, ALK, FGFR, RET…)
