---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - cytogénétique
  - FISH
  - analyse_image
  - seuillage
  - classification
  - machine_learning
  - deep_learning
  - MYC
  - HER2
  - lymphome_Burkitt
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Analyse automatisée des lames FISH — partie 2

> Liens : [[16_670 Analyse automatisée des lames FISH - partie 1]] | [[16_650 FISH généralités]] | [[16_630 La FISH appliquée à l'anapath]] | [[16_640 Les sondes utilisées en FISH]]

## Principe / Bases

Suite directe de la [[16_670 Analyse automatisée des lames FISH - partie 1|partie 1]]. Aborde :
- La **segmentation des signaux** par seuillage
- La **labellisation** des objets
- La **classification** (règles + machine learning)
- L’interprétation prudente des résultats

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p16_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p18_00.jpeg]]

## Workflow technique

### Segmentation des signaux par **seuillage**

Les signaux FISH sont **brillants sur fond sombre** = situation **idéale** pour le seuillage.

| Principe | Détail |
|----------|--------|
| Définition | Transformation d’une image en niveaux de gris en image **noir/blanc** stricte (pixel = 0 ou 1) |
| Seuil | Valeur d’intensité au-delà de laquelle pixel = 1 (blanc), en deçà pixel = 0 (noir) |
| Exemple | Carré clair sur fond gris : seuil à 100 → carré segmenté |

#### Application aux signaux HER2 / CEP17
- Canaux rouge et vert (fausses couleurs) → travail en **niveaux de gris**
- Définition manuelle du seuil par **tâtonnement** (souvent ~8 pour Texas Red, ~35 pour FITC)

> **Limite du seuillage** : seuil **variable** d’une lame à l’autre, d’une numérisation à l’autre, voire d’une région à l’autre. Méfiance avec les outils de segmentation reposant uniquement sur du seuillage (souvent peu satisfaisants en immunohistochimie).

> Pour les **signaux FISH lumineux sur fond sombre** : **simple et efficace**.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p19_00.png]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p20_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p21_00.jpeg]]

### Labellisation des objets

| Concept | Application |
|---------|-------------|
| Détourage individuel | Chaque objet (noyau, signal) est **identifié indépendamment** |
| Stockage | Position, surface, intensité enregistrées |
| Utilité | Compter les **spots verts/rouges par noyau**, calcul automatisé du **ratio HER2/CEP17** |

## Lecture / Interprétation

### Classification — définition de **règles du jeu**

Approche conventionnelle : on définit explicitement les classes et leurs critères.

| Classe | Critère |
|--------|---------|
| **Noyau superposé** | Surface élevée + forme anormale |
| **Noyau trop petit** | Surface < seuil |
| **Noyau analysable** | Tous les autres |

Sous-classes basées sur le **nombre de spots** par noyau :
- 2 verts + 2 rouges = profil normal
- 2 verts + 3 rouges = polysomie/gain
- Cluster vert = amplification

> Calcul possible du **nombre moyen de copies HER2** et du **ratio HER2/CEP17** → rendu d’un statut HER2.

### Limites en pratique
- Méthodes encore **peu pertinentes en routine** pour les sondes d’**amplification** (HER2) — segmentation nucléaire approximative
- Validation et contrôle qualité strict requis avant utilisation en routine

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p22_00.png]]

## Exemple FISH break-apart MYC — Lymphome de Burkitt

### Rappel mécanique
- Sondes **rouge** (3’) et **verte** (5’) hybrident **MYC** sur le **chromosome 8**
- **Cellule diploïde sans réarrangement** : 2 couples vert/rouge proches
- **t(8;14)** (Burkitt) : MYC sous contrôle du promoteur **IGH** → **séparation** des signaux rouge et vert

### Spécificités de la segmentation
- **Lymphocytes** : noyaux **proches**, peu de cytoplasme → superpositions fréquentes
- Segmentation nucléaire plus **difficile** que dans les carcinomes
- Utilisation d’un **logiciel commercial** plus poussé (algorithmes avancés)

### Classification dans le lymphome de Burkitt

| Catégorie | Critère | Couleur de bordure |
|-----------|---------|---------------------|
| **Non analysable** | Noyau exclu (taille, forme, superposition) | Gris / blanc |
| **Analysable non splitté** | 2 couples vert/rouge | **Vert** |
| **Analysable splitté** | 1 couple + 1 vert isolé + 1 rouge isolé (ou variantes) | **Rouge** |

> **Couple vert/rouge** = signal vert et signal rouge à **distance < seuil défini** (paramètre du logiciel).

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p24_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p25_00.jpeg]]


### **Piège majeur** d’interprétation

Camembert de résultat : **66 % de cellules splittées**, 34 % non splittées.

| Conclusion correcte | Conclusion erronée |
|---------------------|---------------------|
| « Confirme la suspicion diagnostique de lymphome de Burkitt » | « Lymphome de Burkitt avec **66 %** de cellules réarrangées MYC » |

> **Biologiquement**, dans le Burkitt (prolifération **clonale** dont la t(8;14) est l’événement **driver**), **100 %** des cellules tumorales sont réarrangées.

#### Origine des **34 % de faux négatifs**
1. **Erreur de segmentation** (noyau mal délimité)
2. Quelques cellules **non tumorales** dispersées
3. **Signaux par projection** (en Z) artificiellement proches malgré le réarrangement
4. **Distance de fusion** réglée trop large dans le logiciel

#### Faux positifs dans une lame **sans** réarrangement
- Inexistants ou très rares (~**1,5 %**)
- Causes : effets de coupe, défauts d’hybridation

> Pour les **sondes break-apart**, l’analyse automatisée est **largement envisageable** ; pour l’**amplification**, elle reste fragile.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p27_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-670  Analyse automatisée des lames de FISH CF CL CCB/p28_00.jpeg]]

## Méthodes avancées de classification : **machine learning**

### Apprentissage machine conventionnel

| Approche | Détail |
|----------|--------|
| Régression logistique, arbres de décision, SVM, random forest… | On désigne à la machine de **nombreux exemples** annotés |
| Entrée | Pour chaque objet : **caractéristiques pertinentes** (surface, grand diamètre, texture, forme, **circularité**…) |
| Sortie | La machine **pondère elle-même** ces caractéristiques et définit des seuils pour classer un nouvel objet |
| Compréhensibilité | **Algorithme transparent** (on comprend les critères) |

### **Deep learning** — réseaux de neurones artificiels

| Caractéristique | Détail |
|-----------------|--------|
| Données | **Très grand nombre** d’exemples annotés (milliers d’amas, milliers de noyaux analysables…) |
| Apprentissage | La machine **invente seule** les caractéristiques discriminantes |
| Performances | Généralement **meilleures** que les méthodes conventionnelles |
| **Inconvénient** | **Boîte noire** — méthode d’apprentissage opaque |
| **Sous le capot** | Beaucoup de **convolutions** (cf. partie 1) parallélisées sur d’énormes volumes de données |

### Difficultés en anatomopathologie

| Problème | Conséquence |
|----------|-------------|
| **Variabilité des images** (techniques, coloration, acquisition) | Difficile à généraliser |
| **Annotation lourde** | Beaucoup moins disponible qu’en radiologie |
| Validation lente | Difficulté à atteindre le standard de routine |


## Indications cliniques majeures

| Sonde | Routine actuelle | Recherche / avenir |
|-------|------------------|---------------------|
| **HER2** (sein) | **Lecture humaine** validée | Analyse automatisée fragile (segmentation imparfaite) |
| **MYC, ALK, EWSR1** break-apart | **Lecture humaine** validée | **Analyse automatisée envisageable** (faux positifs faibles) |
| Cohortes / TMA | – | Outils prometteurs pour études à grande échelle |

## Avantages / Limites de l’analyse automatisée

| Avantages | Limites |
|-----------|---------|
| **Reproductibilité** théorique | **Non validée en routine** France |
| Comptage exhaustif | Segmentation nucléaire imparfaite (amplification) |
| Possibilité de **deep learning** | Annotation chronophage |
| Adapté aux études à grande échelle | Variabilité interlaboratoire |
| Faux positifs faibles (break-apart) | **Boîte noire** des réseaux de neurones |

---

## 🔑 Points clés à retenir

1. **Seuillage** : transformation d’une image en niveaux de gris en **noir/blanc** par seuil d’intensité ; idéal pour les signaux FISH (**brillants sur fond sombre**).
2. **Méfiance** des outils basés uniquement sur seuillage en IHC ; en FISH, **simple et efficace**.
3. **Labellisation** = identification individuelle de chaque objet (position, surface) → permet le **comptage automatique** des spots par noyau.
4. **Classification conventionnelle** : règles définies par l’utilisateur (surface, forme, nombre de spots) → classes (analysable / superposé / trop petit / amplifié…).
5. **Pour l’amplification HER2** : analyse automatisée encore **fragile** (segmentation nucléaire imparfaite).
6. **Pour les break-apart (MYC, ALK)** : analyse automatisée **largement envisageable** (faux positifs ~ **1,5 %**).
7. **Piège d’interprétation** : un **66 % de splits** dans un Burkitt n’est PAS « 66 % de cellules réarrangées » — un Burkitt clonal a **100 %** de réarrangement, le déficit = **faux négatifs** (segmentation, projections, distance de fusion).
8. **Machine learning** conventionnel : la machine **pondère** des caractéristiques fournies (surface, forme, texture).
9. **Deep learning** = **boîte noire** ; sous le capot, beaucoup de **convolutions** ; annotation lourde requise.
10. **Toujours interroger les chiffres** d’une analyse automatisée à la lumière de la **biologie tumorale** ; ne pas surinterpréter une représentation graphique.
