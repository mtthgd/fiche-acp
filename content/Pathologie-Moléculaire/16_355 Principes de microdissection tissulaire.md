---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - extraction_ffpe
  - microdissection
  - LCM
  - pourcentage_cellules_tumorales
  - préanalytique
  - INCa
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Principes de microdissection tissulaire

> Liens : [[16_351 Effet de la fixation sur les acides nucléiques]] | [[16_365 Validation de la qualité de l’échantillon par qPCR]] | [[16_310 Principes de la qPCR]] | [[16_320 PCR digitale - principe et applications]]

## Principe / Définition

La **microdissection tissulaire** consiste à échantillonner du matériel prélevé chez un patient (liquide, cellulaire ou tissulaire) afin d’obtenir une **analyse moléculaire** précise et fiable. C’est une étape **préanalytique** **artisanale** mais **cruciale**, à la charnière entre la pathologie morphologique et la biologie moléculaire.

Objectif : éviter tout **faux positif** ou **faux négatif** susceptible d’entraîner une **perte de chance** pour le patient (effet secondaire inutile ou défaut de traitement).

## Indications / Applications

- Toute analyse moléculaire d’aval : recherche de mutation ponctuelle, de variants, de **CNV**, profil d’expression, **caryotype moléculaire**, **MSI**, réarrangements
- Sélection d’une **zone tumorale** sur un fond normal/inflammatoire
- Préparation des échantillons pour **PCR**, **qPCR**, **HRM**, **PCR digitale**, **NGS**

## Cadre réglementaire — INCa

- **Programme d’assurance qualité** mis en œuvre par l’**Institut National du Cancer (INCa)**
- **Guide des bonnes pratiques** défini en concertation avec les pathologistes
- Constat : **97 %** des échantillons correctement analysés ; les erreurs sont majoritairement **préanalytiques**
- Causes principales : **matériel tumoral insuffisant** ou **dégradation de l’ADN tumoral**
- Améliorations continues depuis **2016**


## Questions à se poser avant de microdisséquer

1. Quel **type de prélèvement** est disponible (biopsie, pièce, cytobloc, tissu congelé) ?
2. Quel **composant moléculaire** est ciblé (**ADN, ARN, protéines**) ?
3. Quelle **analyse** est requise (mutation ponctuelle, fusion, MSI, CNV) ?
4. Quelles **techniques** seront utilisées en aval (Sanger, qPCR, ddPCR, NGS) ?

Le choix du tissu dépend du **matériel disponible** et des **technologies utilisées**, avec **hiérarchisation** des examens si matériel précieux.



## Facteurs critiques préanalytiques

| Facteur | Impact |
|---------|--------|
| **Délai d’ischémie froide** | Dégradation ADN/ARN |
| **Type de fixateur** | **Formol tamponné pH neutre** seul recommandé |
| **Délai/durée de fixation** | Cassures, ponts méthylène |
| **Température d’imprégnation paraffine** | Altération acides nucléiques |
| **Traçabilité** | Identification correcte du bloc |
| **Temps d’archivage** | Hydrolyse progressive |



## Cible de l’analyse — choix du tissu

- Tissu **témoin normal** vs **tissu tumoral**
- **Méfiance face aux doubles localisations synchrones** → bien préciser le bloc d’intérêt
- Cible **stroma** vs **épithélium tumoral**
- Type de molécule : **ADN, ARN, protéines**

## Estimation du % de cellules tumorales

**Point sensible** de l’échantillonnage :

- **Ne pas se référer à la surface** mais au **pourcentage de noyaux d’intérêt**
- Comparer aux noyaux des **cellules normales et inflammatoires**
- Permet de **corréler à l’ADN tumoral extrait**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p15_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p15_02.jpeg)


## Techniques de qualification des acides nucléiques

| Technique | Mesure | Limite |
|-----------|--------|--------|
| **Spectrométrie (Nanodrop)** | Quantité + **pureté** (UV) | Pas d’information sur **intégrité** |
| **Fluorométrie (Qubit)** | Quantité **précise**, sensible | Limite **pg/µL** |
| **qPCR** | Sensibilité **1–10 %** | Variants rares non détectés |
| **NGS** | Profil complet | Coût, temps |
| **PCR digitale** | Quantification **absolue**, **< 0,01 %** | Cible spécifique requise |

## Sensibilité des techniques de détection moléculaire

| Technique | Seuil de sensibilité |
|-----------|----------------------|
| Séquençage **Sanger** | **> 10 %** |
| **qPCR** | **1–10 %** |
| **HRM** | **5–10 %** |
| **NGS** | **1–5 %** (panel ciblé) |
| **PCR digitale (ddPCR)** | **< 0,01 %** |

**Aucune technique n’a un pouvoir de détection à 100 %.** Un résultat négatif entraîne la **révision** et non l’**exclusion** du risque initial.


## Qualification ADN pour le NGS

Trois critères :
1. **DIN** = DNA Integrity Number
2. **% de fragments > 10 kb**
3. **Profil électrophorétique** (Bioanalyzer / TapeStation)

Variables additionnelles d’évaluation post-NGS :
- **Profondeur de séquençage**
- **Fréquence allélique** des variants

## Méthodes pratiques de microdissection

| Méthode | Indication |
|---------|------------|
| **Copeaux paraffinés** (coupe entière du bloc) | Tumeur ≥ 70 % cellules |
| **Grattage de coupe** sur lame | Zone tumorale délimitée |
| **Trocart** (carotte du bloc) | Zone précise |
| **Scalpel** sur lame ou bloc | Zone hétérogène |
| **LCM (Laser Capture Microdissection)** | Sur tissu congelé après vérification sur coupes sériées |

⚠️ Pour le tissu congelé : **ne pas interrompre la chaîne du froid**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p18_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p19_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p20_00.jpeg)

## Exemples pratiques d’estimation du % tumoral

| Aspect histologique | % cellules tumorales |
|---------------------|---------------------|
| Tumeur mésenchymateuse pure | **~ 90 %** |
| Riche en cellules tumorales + infiltrat inflammatoire | **~ 70 %** |
| Glandes tumorales + stroma lympho­ïde abondant | **< 30 %** |
| Cellules tumorales dispersées + stroma fibreux inflammatoire | **~ 20 %** |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p21_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p22_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p24_01.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p25_00.jpeg)

## Cas particulier des cytoblocs

- **Épaisseur réduite** → quantité de matériel **plus faible**
- Peut impacter la qualité même avec cellularité tumorale élevée
- Vérifier sur coupes sériées : épaisseur du dépôt + cellularité réelle

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p27_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p28_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p29_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p30_00.jpeg)

## Pièges / Contrôles qualité

- Biopsie avec **trop peu de glandes tumorales** → risque non contributif
- Métastase péritonéale en **stroma myxoïde** pauvre en cellules tumorales + stroma inflammatoire abondant → faux négatifs
- **Vérifier après prélèvement** par coloration standard (HE) si trocart ou scalpel
- Préserver le matériel = **hiérarchiser** les analyses si bloc précieux

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-355%20Principes%20microdissection%20tissulaire/p31_00.jpeg)

## 🔑 Points clés à retenir

1. La microdissection est une **étape préanalytique cruciale** garantissant la fiabilité des analyses moléculaires.
2. **97 %** d’analyses correctes : les erreurs sont **majoritairement préanalytiques** (matériel insuffisant ou ADN dégradé).
3. **Programme INCa** + guide de bonnes pratiques = cadre réglementaire.
4. **% de cellules tumorales** = **noyaux d’intérêt / noyaux totaux** (jamais surface).
5. **Formol tamponné pH neutre** = seul fixateur recommandé.
6. Quatre méthodes de microdissection : **copeaux**, **grattage**, **trocart/scalpel**, **LCM** (sur congelé).
7. Qualification : **Nanodrop** (pureté), **Qubit** (quantité), **qPCR/ddPCR** (intégrité fonctionnelle), **Bioanalyzer** (profil).
8. Sensibilité : **Sanger > 10 %** → **NGS 1–5 %** → **ddPCR < 0,01 %**.
9. NGS : trois critères = **DIN**, **% fragments > 10 kb**, **profil électrophorétique**.
10. Cytoblocs : épaisseur faible → vigilance sur quantité de matériel.
11. **Aucune technique n’a 100 % de sensibilité** : un résultat négatif n’exclut jamais le risque initial.
12. Toujours **confronter** les résultats moléculaires avec la morphologie et **préserver** le matériel pour analyses ultérieures.
