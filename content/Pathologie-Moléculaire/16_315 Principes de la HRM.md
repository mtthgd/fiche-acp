---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - pcr_methodes
  - HRM
  - courbes_fusion
  - criblage_mutations
  - SYBR
  - LC480
  - hétéroduplex
  - IDH1
  - méthylation
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Principes de la HRM

> Liens : [[16_310 Principes de la qPCR]] | [[16_320 PCR digitale - principe et applications]] | [[16_355 Principes de microdissection tissulaire]] | [[16_365 Validation de la qualité de l’échantillon par qPCR]]

## Principe / Définition

La **HRM (High Resolution Melting)** est une technique de **criblage** des mutations basée sur l’analyse fine des **courbes de fusion (melting)** d’un produit de qPCR.

Principalement développée pour la **détection de mutations** (mais aussi applicable à l’**analyse de méthylation** sur ADN bisulfité).

Caractéristiques :
- Système **fermé** en plaque **96 puits**
- **Simple** et **rapide** (résultat en **~ 3 h**)
- **Peu coûteuse**
- Permet d’**économiser** du séquençage en filtrant les ADN normaux


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p01_03.png)

## Indications / Applications

- **Criblage de mutations** ponctuelles dans des **hot-spots** (exon ou codon défini)
- **Analyse de méthylation** (sur ADN bisulfité)
- Applicable à de nombreux gènes : par exemple **IDH1** (codon **R132H** exon 4), **IDH2**, **BRAF**, **KRAS**, **EGFR**

## Étapes techniques

### 1. Préparation des ADN
- Extraction et qualification
- **Témoins indispensables** :
  - ADN **normal** (référence WT)
  - ADN **muté** (positif de référence)
  - Pas obligatoire d’avoir la **mutation ponctuelle identique** mais **mutation sur le codon analysé**

### 2. qPCR avec agent intercalant
- **Agent intercalant** = **LC480** (LightCycler 480) ou équivalent
- Vérification d’une **bonne amplification** :
  - **CT précoce**
  - Pente sigmoïde correcte
  - Échantillons **dans la même gamme de CT** que les témoins
- Détermination du **TM** des produits d’amplification
- Amplicon recommandé : **< 150 pb** (garantie de bonne efficacité)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p04_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p05_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p06_00.jpeg)

### 3. Dénaturation – renaturation
- **Dénaturation** finale du produit PCR à **95 °C**
- **Renaturation lente** (refroidissement progressif) → favorise la formation d’**hétéroduplex** (mésappariements ponctuels ou plus longs entre brins WT et mutés)
- ADN double brin à 100 % → **fluorescence maximale**

### 4. Courbe de fusion (melting)
- Augmentation progressive de la température
- **Relargage du LC480** au fur et à mesure que l’ADN devient simple brin
- Diminution progressive de la fluorescence jusqu’à 0 (ADN 100 % simple brin)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p07_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p08_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p09_00.png)

## Paramètres analysés

| Paramètre | Réglage / Interprétation |
|-----------|-------------------------|
| **TM (Melting Temperature)** | Pic unique attendu pour PCR spécifique ; pic variant ou TM double = suspicion mutation |
| **Courbe de fusion normalisée** | Comparaison de la **cinétique de dénaturation** vs ADN normal |
| **Différents spots** | Position des courbes par rapport à l’axe des abscisses (témoins normaux) |
| **Seuil** | À définir pour discriminer les profils intermédiaires |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p10_00.png)


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p11_03.png)

## Profils de courbes

| Profil HRM | Interprétation | Conduite à tenir |
|-----------|----------------|------------------|
| **Superposable au témoin normal** | ADN sauvage | Rendu direct sans séquençage |
| **Différent du témoin normal**, proche du muté | ADN muté | **Séquencer** l’ADN initial pour caractériser |
| **Profil intermédiaire / douteux** | Suspect (faible fréquence allélique ou mutation rare) | Récupérer le produit qPCR HRM **purifié** et le séquencer |

## Avantages / Limites

| Avantages | Limites |
|-----------|---------|
| **Simple, rapide** (~ 3 h) | Technique de **criblage** uniquement |
| **Peu coûteuse** | Nécessite **séquençage de confirmation** |
| **Sensible** | Nécessite témoins WT et muté **adaptés** |
| Robuste, peu d’optimisation | **Concurrencée par le NGS** (analyse globale) |
| Réduit le nombre de séquençages (économie) | Limitée aux **mutations rares** dans des hot-spots |
| Compatible plaque **96 puits** | Module HRM nécessaire sur l’appareil de qPCR |

## Augmentation de sensibilité

- **Récupération et séquençage** du produit HRM purifié (au lieu de l’ADN natif)
- Augmente la **fréquence allélique** apparente du variant rare → pic clairement visible en Sanger

## Validation laboratoire

Très bonne **concordance HRM ↔ séquençage** :
- Profils normaux → séquence **WT** confirmée
- Profils mutés → séquençage trouve la mutation
- Profils **intermédiaires** : **mutation rare** dans une minorité des cas, sauvages dans la majorité

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p12_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p12_03.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p14_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-315%20%20Principes%20de%20lHRM/p14_03.png)

## Pièges / Contrôles qualité

- Vérifier la **qualité de la PCR initiale** (CT précoce, pente sigmoïde) avant d’interpréter la courbe de fusion
- Toujours faire passer **témoins WT + muté + cas patient** dans le **même run**
- Profil intermédiaire = **séquencer absolument**
- **Seuils de discrimination** doivent être définis par cible

## Exemple : IDH1 dans les gliomes

- Glioblastomes secondaires et **gliomes de grade 2 et 3**
- Mutation **R132H** sur **exon 4** d’**IDH1**
- HRM = **criblage** efficace, séquençage de confirmation

## 🔑 Points clés à retenir

1. **HRM = High Resolution Melting** = criblage de mutations basé sur l’analyse des **courbes de fusion (melting)**.
2. Système **fermé**, plaque **96 puits**, résultat en **~ 3 h**.
3. Repose sur la **qPCR avec agent intercalant** (**LC480** ou équivalent).
4. Amplicons **< 150 pb** recommandés.
5. Étapes : qPCR → dénaturation 95 °C → **renaturation lente** (favorise hétéroduplex) → courbe de fusion.
6. Deux paramètres : **TM** (pic unique vs variant) et **profil de courbe normalisée**.
7. Témoins **WT** et **muté** indispensables dans chaque run.
8. Trois profils : **normal** (rendu direct), **muté** (séquencer ADN initial), **intermédiaire** (séquencer produit HRM purifié).
9. Avantages : **simple**, **rapide**, **peu coûteux**, **sensible**, économise du séquençage.
10. Limites : **technique de criblage** uniquement → **séquençage de confirmation** obligatoire.
11. Augmentation de sensibilité possible par **purification du produit HRM** avant séquençage.
12. Concurrencée par le **NGS** (plus exhaustif) mais reste pertinente pour mutations **rares dans hot-spots** ciblés (par exemple **IDH1 R132H**).
