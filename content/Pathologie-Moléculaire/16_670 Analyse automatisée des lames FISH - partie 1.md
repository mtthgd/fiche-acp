---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - cytogénétique
  - FISH
  - analyse_image
  - traitement_image
  - segmentation
  - HER2
  - convolution
  - histogramme
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Analyse automatisée des lames FISH — partie 1

> Liens : [[16_670 Analyse automatisée des lames FISH - partie 2]] | [[16_650 FISH généralités]] | [[16_630 La FISH appliquée à l'anapath]] | [[16_640 Les sondes utilisées en FISH]]

## Principe / Bases

Cours qui fait suite à la **numérisation des lames de FISH**. Aborde le **traitement et l’analyse automatisée d’images** de FISH avec deux exemples :
- **FISH HER2** (carcinome mammaire) — recherche d’une **amplification génique**
- **FISH MYC break-apart** (lymphome de Burkitt) — recherche d’un **split**

> Ces techniques **ne sont pas validées** ni utilisées en routine en France. À considérer comme une **culture générale** indispensable pour aborder de manière critique les futures publications et outils.

### Vision humaine vs vision machine

| Cerveau humain | Machine |
|----------------|---------|
| Identifie en une fraction de seconde noyaux, amas, artefacts | L’image est une **matrice de nombres** (intensités lumineuses) |
| Tri intuitif (exclusion d’amas) | Identification et classification = **outils mathématiques complexes** |
| Pas d’effort | Algorithmes de traitement et de classification |

### Stockage d’une image digitale

| Concept | Détail |
|---------|--------|
| **Bit** | Unité élémentaire = 0 ou 1 |
| **Octet (byte)** | 8 bits → **256 valeurs possibles** (0-255) |
| **Image niveaux de gris** | 1 octet/pixel : 0 = noir, 255 = blanc |
| **Image RGB couleur** | 3 octets (24 bits) : R, V, B chacun de 0 à 255 |

> Les images de FISH en couleur = **3 images en niveaux de gris superposées** affichées en **fausses couleurs** (bleu DAPI, rouge, vert).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p01_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p01_01.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p02_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p03_00.jpeg)

## Workflow technique — étapes générales

| Étape | But |
|-------|-----|
| **Traitement** | Modifier la matrice de pixels (contraste, flou, contours) |
| **Segmentation** | Délimiter les **objets** (noyaux, signaux) |
| **Classification** | Attribuer chaque objet à une **classe** (analysable, exclu, positif…) |

## Exemple FISH HER2 — Carcinome mammaire

### Étape 1 — Séparation des canaux

Séparation en 3 couches monochromatiques : **canal bleu** (DAPI noyau), **canal rouge** (CEP17), **canal vert** (HER2). Travail initial sur le **DAPI** pour la **segmentation nucléaire**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p04_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p04_01.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p06_00.png)

### Étape 2 — Modification du contraste (contrast stretching)

| Outil | Histogramme |
|-------|-------------|
| Définition | Répartition des pixels pour chaque intensité (0-255) |
| Image initiale | Plus d’**1 million de pixels noirs** (valeur 0) + quelques pixels gris très foncés correspondant aux noyaux |
| **Contrast stretching** | Étalement mathématique de l’histogramme sur toute la gamme tout en conservant les proportions |
| Résultat | Noyaux désormais **bien visibles** |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p07_00.png)


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p08_01.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p09_00.jpeg)

### Étape 3 — Application d’un flou (convolution gaussienne)

#### Pourquoi flouter ?
Lisse la segmentation → **objets plus pertinents** biologiquement (les contours nets sont **crénelés**, le flou les rend lisses).

#### Notion de **convolution**
- Outil mathématique **omniprésent** en traitement d’image
- Utilise un **kernel** (petite grille pondérée — ex. 5×5)
- Le kernel se déplace pixel par pixel et **modifie la valeur du pixel central** en fonction des valeurs des pixels alentours

#### Kernel gaussien
Répartition gaussienne des poids :
- **Centre** : poids élevé (ex. 41)
- **Bord** : poids faibles (ex. 1)
- Chaque pixel sous le kernel est **multiplié par son poids**, somme totale **divisée par le total des poids**
- Plus la zone est claire sous le kernel, plus le résultat est élevé

#### Optimisation
- Méthode longue (passage pixel par pixel) coûteuse
- En pratique : utilisation de la **transformée de Fourier** → flou gaussien en **une demi-seconde**

> Une convolution permet aussi : **augmenter la netteté**, **détecter des contours**, etc.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p10_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p10_01.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p11_00.jpeg)


### Étape 4 — Détection de contours (filtre de Sobel)

| Filtre | Principe |
|--------|----------|
| **Sobel X** | Kernel asymétrique passé **gauche → droite** sur chaque ligne |
| **Sobel Y** | Kernel asymétrique passé **haut → bas** sur chaque colonne |

- **Zones homogènes** : valeurs résultantes peu modifiées
- **Forts changements de contraste** (en X ou Y) : valeur du pixel central modifiée → **contour détecté**

> Outil **rudimentaire** mais résultat **satisfaisant** sur les noyaux suffisamment contrastés.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-670%20%20Analyse%20automatis%C3%A9e%20des%20lames%20de%20FISH%20CF%20CL%20CCB/p13_00.jpeg)



### Étape 5 — Résultat de la segmentation nucléaire

| Étape | Outil | Résultat |
|-------|-------|----------|
| 1. Niveaux de gris | Conversion DAPI | Image monochrome |
| 2. **Contrast stretching** | Modification de l’histogramme | Noyaux visibles |
| 3. **Flou gaussien** | Convolution | Lisse les contours |
| 4. **Détection de contours** | Filtre de Sobel (convolution) | Contours nucléaires |
| 5. Étapes finales | Combinaison + nettoyage | Segmentation **correcte** mais imparfaite |

> **Limites résiduelles** : noyaux fusionnés persistants → ajout de contraintes (taille, **circularité**) pour amélioration. **Sans flou** : segmentation crénelée, moins biologiquement pertinente.

## Lecture / Interprétation

### Trois notions rudimentaires de traitement d’image

| Notion | Rôle |
|--------|------|
| **Histogramme** (et modifications) | Répartition d’intensité, contrast stretching |
| **Convolution** (kernels) | Flou, détection de contours, **omniprésente en traitement d’image** |
| **Seuillage** (vu en partie 2) | Segmentation des signaux brillants sur fond sombre |

## Indications cliniques majeures (analyse automatisée)

| Application | Intérêt |
|-------------|---------|
| **FISH HER2** dans cancer du sein | Quantification **gènes/centromères** par noyau (réservé recherche) |
| **FISH break-apart** (MYC, ALK, EWSR1) | Détection automatisée d’un Split (cf. partie 2) |
| Analyse à grande échelle / TMA | Gain de temps, reproductibilité (sous validation) |

## Avantages / Limites

| Avantages | Limites |
|-----------|---------|
| Reproductibilité théorique | **Non validée en routine** France |
| Quantification fine (signaux par noyau) | **Segmentation nucléaire imparfaite** |
| Possibilité d’analyse en Z-stack | Variabilité des techniques de coloration |
| Peu coûteux en ressources (TF rapides) | Calibration manuelle du seuil parfois nécessaire |

---

## 🔑 Points clés à retenir

1. Une **image digitale** = matrice de pixels codés en niveaux de gris (1 octet : 0-255) ; image RGB couleur = **3 canaux** superposés.
2. Les images de FISH en couleur sont en réalité **3 canaux niveaux de gris** affichés en **fausses couleurs** (DAPI bleu, vert, rouge).
3. Le traitement d’image = **3 étapes** : traitement → segmentation → classification.
4. **Histogramme** : répartition des intensités lumineuses ; **contrast stretching** = étalement de l’histogramme sur 0-255 pour rendre les noyaux visibles.
5. **Convolution** = outil clé : un **kernel** (matrice pondérée) modifie la valeur de chaque pixel selon ses voisins ; permet flou, contours, netteté.
6. **Flou gaussien** : kernel à répartition gaussienne ; lisse la segmentation pour des objets **biologiquement pertinents**.
7. **Filtre de Sobel** (convolution X + Y) : détection de contours par gradient de luminosité.
8. La **transformée de Fourier** rend la convolution très rapide (~½ seconde sur logiciel photo).
9. La **segmentation nucléaire** est l’**étape cruciale** de toute analyse FISH automatisée — encore imparfaite (noyaux fusionnés).
10. Les outils **rudimentaires** (histogramme + convolutions) suffisent à relever une bonne partie du défi de la segmentation nucléaire.
