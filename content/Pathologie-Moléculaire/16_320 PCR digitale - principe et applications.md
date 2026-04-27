---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - pcr_methodes
  - ddPCR
  - PCR_digitale
  - partition_émulsion
  - sensibilité_allélique
  - loi_Poisson
  - ADN_circulant
  - EGFR_T790M
  - EGFR_C797S
  - CNV
date: 2024
source: DES ACP - Pathologie moléculaire
---

# PCR digitale — principe et applications

> Liens : [[16_310 Principes de la qPCR]] | [[16_315 Principes de la HRM]] | [[16_355 Principes de microdissection tissulaire]] | [[16_365 Validation de la qualité de l’échantillon par qPCR]]

## Principe / Définition

La **PCR digitale (dPCR)** ou **ddPCR** (*Droplet Digital PCR*) est une technique **ultra-sensible** (sensibilité théorique **< 0,01 %**) basée sur la **compartimentalisation** de la réaction PCR en une **multitude de micro-réacteurs individuels**.

Différence avec la **qPCR conventionnelle** :
- **qPCR** : amplification globale de toutes les molécules → **signal moyen**, les séquences rares **masquées** par les abondantes
- **dPCR** : chaque molécule est **isolée** dans un compartiment indépendant → **détection individuelle**

C’est une technique à la fois **qualitative** et **quantitative** (quantification **absolue**).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p01_06.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p02_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p03_00.jpeg)

## Indications / Applications

| Application | Exemple |
|-------------|---------|
| **Détection d’événements rares** | Mutations résistance **EGFR T790M, C797S** sur **ADN circulant** |
| **Quantification absolue** | Concentration d’une séquence d’ADN |
| **CNV** (Copy Number Variation) | Amplification **EGFR**, **HER2** ; délétion **TP53** |
| **ADN tumoral circulant (cfDNA / ctDNA)** | Suivi cancer pulmonaire, mélanome (**BRAF V600E**) |
| **Échantillons FFPE pauvres** | Cytoblocs, humeurs vitrées, blocs presque épuisés |
| **Microbiologie** | Détection ADN viral / bactérien (par exemple *Mycobacterium tuberculosis*) |
| **ADN fœtal** | Diagnostic prénatal non invasif |

## Matériel / Plate-formes

- **Bio-Rad QX200** (technologie Droplet Digital PCR, 2 canaux : **FAM** + **HEX/VIC**)
- **Stilla Naica** (jusqu’à **6 canaux** de fluorescence)
- **Module générateur de gouttelettes** + thermocycleur classique + lecteur de fluorescence

## Réactifs

- **Mix PCR** : amorces (DNA primers), super-mix spécifique, sondes
- **Sondes TaqMan** (sondes d’hydrolyse) :
  - 5’ : **fluorochrome reporter** (FAM, HEX, VIC)
  - 3’ : **quencher** (**BHQ**, **DDQ**)
  - Variantes plus spécifiques : **LNA** ou **MGB**
- **Huile de génération de gouttelettes** spécifique
- **Cartouches microfluidiques** (jusqu’à 8 échantillons par cartouche)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p04_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p05_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p06_00.png)

## Étapes techniques (workflow ddPCR)

### 1. Génération des gouttelettes (partition / émulsion)
- Cartouche microfluidique : ligne du bas = huile, ligne du milieu = échantillon + mix, ligne du haut = collecte
- **Jusqu’à 20 000 gouttelettes** générées par échantillon
- **Distribution randomisée** des molécules d’ADN (**loi de Poisson**)
- Dilution série jusqu’à obtenir **au plus une molécule cible par gouttelette**

### 2. Amplification PCR
- Transfert des gouttelettes sur plaque **96 puits**
- Cycle PCR classique sur thermocycleur
- Amplification dans **chaque** micro-réacteur
- **Gradient de température** lors des mises au point pour optimiser séparation négatif/positif

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p07_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p08_00.png)


### 3. Détection (lecture des gouttelettes)
- Lecture **puits par puits**
- Système optique **2 couleurs** (Bio-Rad) — jusqu’à 6 (Stilla)
- **Comptage** des gouttelettes positives / négatives
- Seuil de fluorescence = signal positif

### 4. Interprétation
- Logiciel dédié (**QuantaSoft** pour Bio-Rad)
- **Minimum 10 000 gouttelettes** par échantillon pour interprétation valide
- Calcul du nombre de copies par **loi de Poisson**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p10_00.png)



| Paramètre | Valeur / Réglage |
|-----------|------------------|
| Gouttelettes générées | **~ 15 000–20 000** par échantillon |
| Minimum pour interprétation | **≥ 10 000** gouttelettes |
| Sensibilité théorique | **< 0,01 %** |
| Canaux fluorescence (Bio-Rad) | **2** (FAM + HEX) |
| Canaux fluorescence (Stilla) | **jusqu’à 6** |

## Représentation des résultats

### 1D (one-dimensional)
- Graphique temporel par puits
- Nuages **positif** vs **négatif** distincts pour chaque sonde

### 2D (two-dimensional, multiplex)
- Quatre clusters de gouttelettes :
  - **Mutées** seules (canal FAM bleu)
  - **Sauvages** (WT) seules (canal HEX vert)
  - **Doubles positives** (orange) — ADN muté + sauvage
  - **Vides / négatives** (noir)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p14_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p15_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p16_00.png)

## Données rendues par échantillon

- **Fraction d’abondance** = équivalent de la **fréquence allélique mutée**
- **Nombre de copies WT** par µL
- **Nombre de copies mutées** par µL
- Exemple concret : mutation à **0,66 %** = **284 copies WT/µL** + **1,9 copie mutée/µL**

## Seuil de positivité — variable par cible

| Mutation | Seuil de positivité |
|----------|--------------------|
| **EGFR L858R** | **0,0087 %** |
| **EGFR T790M** | **0,047 %** (plus de faux positifs) |

⚠️ Le seuil est **spécifique de chaque cible** — déterminé par passage de lignées **WT** connues pour mesurer le bruit de fond (faux positifs).

| Mutation EGFR | Sensibilité ddPCR | Faux positifs |
|---------------|-------------------|----------------|
| **L858R / Del19** | **82–86 %** | **3–4 %** |
| **T790M** | **70 %** | **3 %** |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p18_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p19_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p20_00.png)

## Gamme dynamique — quantité d’ADN critique

- **Trop peu de copies** → ↑ **faux négatifs**
- **Trop de copies** → saturation → ↑ **faux positifs**
- Existence d’une **fourchette optimale** (gamme dynamique)
- Aux extrémités → **incertitude relative** ↑

## Stratégies de multiplexage

### 1. Mêmes fluorochromes, sondes par hot-spot
- Ex : **kit Multiplex KRAS** (codons 12/13) → détecte les **7 mutations activatrices** sans en préciser la nature

### 2. Variation d’intensité de fluorescence
- Une intensité = un type de mutation
- Permet d’identifier la mutation exacte

### 3. Augmentation du nombre de canaux
- 3 à 6 canaux (Stilla Naica)
- Panels de **3 à 4 fluorochromes** simultanés

### Exemple : **kit ID-EGFR**
- **3 mixes différents** = 3 puits par patient
- Couvre exons **18 à 21** EGFR
- **ID-EGFR Sensi** : Del19 (canal HEX), L858R / L861Q (canal FAM), WT (double positif)
- **ID-EGFR Resist** : T790M (canal FAM), C797S (cis = double / trans = canal HEX uniquement)

⚠️ Position **cis** vs **trans** de **C797S** par rapport à T790M = conséquence thérapeutique (combinaison d’anti-EGFR de 2e + 3e génération possible ou non).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p25_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p26_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p27_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p28_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p29_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p31_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-analyses-adn-pcr/16-320%20PCR%20Digitale%20Principe%20et%20applications/p32_00.jpeg)

## Avantages / Limites

| Avantages | Limites |
|-----------|---------|
| **Sensibilité ultra-haute** (**< 0,01 %**) | Nécessite **cible spécifique connue** |
| **Quantification absolue** (loi de Poisson) | Nombre limité de cibles par run |
| Détection d’**événements rares** dans excès de WT | Coût équipement et consommables |
| Détection de **CNV** | Multiplexage limité (2–6 canaux) |
| Compatible **FFPE pauvre** (cytobloc, humeur vitrée) | **Seuil de positivité** à valider par cible |
| Idéal pour **ADN circulant (ctDNA)** | Sensibilité variable selon la cible (T790M < L858R) |
| Multiplexage possible | Gamme dynamique étroite |

## Pièges / Contrôles qualité

- **Blanc PCR** (eau + mix) à chaque run → vérifie l’absence de contamination → ne doit contenir que des **gouttelettes vides**
- **Seuil de positivité validé** pour chaque cible (par lignée WT)
- Vérifier que la **barre d’erreur** de l’échantillon **ne coupe pas** le seuil de positivité (sinon = faux positif)
- Quantité d’ADN dans la **gamme dynamique** (ni trop peu, ni trop)
- **≥ 10 000 gouttelettes** sinon résultat ininterprétable

## Applications phares en oncologie pulmonaire

- Suivi de la **résistance aux anti-EGFR** : **T790M** (1re/2e ligne), **C797S** (3e ligne)
- Évite la **rebiopsie** invasive (analyse plasmatique)
- Détection des **mutations sensibilisantes** EGFR (Del19, L858R, L861Q)
- Suivi de la **maladie résiduelle moléculaire**

## 🔑 Points clés à retenir

1. **PCR digitale (ddPCR)** = **compartimentalisation** de la PCR en **~ 20 000 gouttelettes** indépendantes (partition / émulsion).
2. Sensibilité théorique **< 0,01 %** — détecte l’**aiguille dans la botte de foin**.
3. **Quantification absolue** (loi de **Poisson**) sans gamme étalon.
4. Workflow 4 étapes : **partitionnement → amplification → détection → interprétation**.
5. Sondes **TaqMan** : 5’ reporter (FAM/HEX) + 3’ quencher (BHQ).
6. **≥ 10 000 gouttelettes** par échantillon pour interprétation valide.
7. **Seuil de positivité spécifique de chaque cible** (par exemple EGFR L858R 0,0087 % vs T790M 0,047 %).
8. **Gamme dynamique** : trop peu d’ADN = faux négatifs ; trop = faux positifs.
9. Représentation **2D** : 4 clusters (muté / WT / double positif / vide).
10. Applications majeures : **ADN tumoral circulant (ctDNA)**, mutations résistance **EGFR T790M / C797S**, suivi **BRAF V600E** mélanome, **CNV** (HER2, EGFR).
11. **C797S cis vs trans** par rapport à T790M = impact thérapeutique (combinaison anti-EGFR 2e/3e génération).
12. Multiplexage par : sondes mêmes fluorochromes (KRAS), variation d’intensité ou **multi-canaux** (jusqu’à **6 canaux Stilla Naica**).
