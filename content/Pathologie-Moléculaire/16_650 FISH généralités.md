---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - cytogénétique
  - FISH
  - lecture_FISH
  - fluorescence
  - microscope
  - sondes_break_apart
  - HER2
  - ALK
  - artefacts
date: 2024
source: DES ACP - Pathologie moléculaire
---

# FISH généralités — lecture d’une lame en paraffine

> Liens : [[16_630 La FISH appliquée à l'anapath]] | [[16_640 Les sondes utilisées en FISH]] | [[16_670 Analyse automatisée des lames FISH - partie 1]] | [[16_670 Analyse automatisée des lames FISH - partie 2]]

## Principe / Bases

Cours de rudiments pour la **lecture d’une lame de FISH** (Fluorescence In Situ Hybridization) sur matériel inclus en paraffine. Suppose la connaissance préalable :
- Des principes de la **fluorescence**
- De la technique de FISH sur FFPE
- Des **types de sondes** ([[16_640 Les sondes utilisées en FISH]])
- De l’interprétation du nombre et de la topographie des signaux

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p01_00.jpeg]]

## Acteurs / Sondes / Réactifs

### Microscope à fluorescence — équipement requis

| Élément | Spécifications |
|---------|----------------|
| **Lampe à mercure** | Apprendre allumage/extinction (matériel coûteux, fragile) |
| **Objectifs faibles** ×5, ×10, ×20 | Repérage des zones tumorales/non tumorales |
| **Objectif** ×40 | Vue d’ensemble des signaux |
| **Objectif fort** ×60 sec ou ×100 huile | Analyse fine ; **ouverture numérique > 0,80** |
| **Anneau de correction** | Réglable selon épaisseur de lamelle |
| **Cubes à fluorescence** | Adaptés aux **caractéristiques spectrales des sondes** |

### Préparation à la lecture
1. **Connaître le dossier** : indication, question posée
2. **Accès à la lame HES / IHC** correspondante (repérage zones tumorales)
3. **Relire la fiche technique de la sonde** : couleur du gène et du centromère

> **Piège majeur** : selon les fabricants, **HER2** peut être marqué en vert (CEP17 rouge) **ou inversement**. Une mauvaise identification = diagnostic FISH **complètement erroné**.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p03_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p04_00.jpeg]]

## Workflow technique de lecture

### Étape 1 — Filtre DAPI (contre-coloration nucléaire bleue)

**Faible grossissement** :
- Vue d’ensemble morphologique
- Concordance avec la lame **HES**
- Repérage des zones tumorales (ex. adénocarcinome pulmonaire au centre, parenchyme alvéolaire normal en périphérie)
- Sur biopsies : zone tumorale parfois minime (un amas de 10 cellules) → **HES indispensable**

**Fort grossissement** :
- Apprécier la **qualité de la digestion protéolytique** :
  - Bonne digestion : noyaux **homogènes**, contours réguliers
  - Digestion **excessive** : noyaux **troués** → ne pas interpréter

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p06_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p07_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p08_00.jpeg]]

### Étape 2 — Identifier vrais spots vs artefacts

| Vrai spot d’hybridation | Faux spot / artefact |
|-------------------------|----------------------|
| **Intranucléaire** | Le plus souvent **cytoplasmique** |
| **Rond** | Forme variable |
| Fluorescence **intense** | Intensité parasite |
| **Couleur appropriée** au filtre utilisé | Couleur jaune (multibande) → vérifier en monobande |

> Préférer les **filtres monobandes** plutôt que multibandes pour discriminer les artefacts.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p09_00.png]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p09_02.jpeg]]

### Étape 3 — Acquisition et superposition des canaux

Deux stratégies possibles :

| Stratégie | Procédure | Avantage / Inconvénient |
|-----------|-----------|--------------------------|
| **Acquisition séparée** | DAPI + canal vert + canal rouge → superposition informatique | **Ne JAMAIS remettre au point** entre vert et rouge (faux signaux de séparation) |
| **Filtre multibande** | Acquisition unique | Rapide, dépend de la qualité du filtre |

> En automatisé : **acquisition Z-stack** (plusieurs plans focaux) = idéal.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p10_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p11_00.jpeg]]

## Lecture / Interprétation — Recommandations générales

| Règle | Détail |
|-------|--------|
| **Témoin interne négatif** | Toujours observer le territoire **non tumoral** : profil **attendu** doit être présent (sinon erreur de sonde) |
| **Balayer toute la lame** | Ne pas manquer un **événement sous-clonal** (amplification HER2 sectorielle dans gastrique/sein) |
| **Plusieurs champs tumoraux** | Idée globale de l’anomalie |
| **Cellules tumorales uniquement** | Discriminer du stroma inflammatoire (cellules tumorales = noyaux plus grands) |
| **Critères de positivité** | Variables selon sonde, indication, type tumoral |

### Exemple de mauvaise concordance sonde/contexte
Si on attend une sonde break-apart (ex. **ALK**) et qu’on observe en territoire normal **2 verts + 2 rouges séparés** = **erreur de sonde** (la technicienne a posé une sonde d’énumération type HER2).

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p13_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p14_00.jpeg]]

### Pièges fréquents

| Piège | Mécanisme | CAT |
|-------|-----------|-----|
| **Axe Z** (3D) | On n’analyse qu’une partie du noyau | Faire varier la mise au point ; **Z-stack** |
| **Faux signaux de séparation** | Remise au point entre acquisition vert et rouge sur sonde break-apart | Ne **jamais remettre au point** entre canaux |
| **Autofluorescence** des macrophages/mastocytes | Petits points cytoplasmiques pouvant déborder sur le noyau | Ignorer ces cellules, n’analyser que les cellules tumorales |
| **Artefacts d’écrasement** (biopsies) | Noyaux faussement fusionnés, signaux étirés/espacés | **Ne pas interpréter** ces territoires |
| **Cellules géantes anormales** (chimio néo-adjuvante, haut grade) | Compte aberrant de signaux | Ne pas interpréter si rares et éparses |
| **Superpositions nucléaires** | Spot vert non attribuable à un noyau précis | Chercher territoire mieux étalé |
| **Stroma inflammatoire** abondant | Faux négatif par dilution de la tumeur dans cellules non tumorales | Identifier strictement les cellules tumorales |

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p16_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p17_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p18_00.jpeg]]

## Analyse globale et comptage

- **Anomalies récurrentes** d’un noyau à l’autre = critère essentiel
- Anomalies présentes dans la **majorité** des cellules tumorales
- **Comptage selon recommandations officielles** (nombre minimal de noyaux par indication)
- **L’interprétation doit être formulée AVANT le comptage** — le comptage illustre l’interprétation visuelle
- **Analyser toute la lame**, pas seulement les cellules comptées

### Sondes break-apart — seuil de positivité
- **Seuil habituel : 15 %** des cellules tumorales avec signaux séparés
- **Zone limite : 10-30 %** = méfiance (faux positifs et faux négatifs fréquents)

#### Causes de **faux positifs**
1. **Instabilité chromosomique** des tumeurs (aléas stochastiques)
2. **Artefacts de séparation** (écrasement, coupe trop épaisse, fixation)
3. Toujours regarder le **non-tumoral** pour calibrer

#### Causes de **faux négatifs**
1. **Dilution** par cellules non tumorales (stroma inflammatoire)
2. Mauvaise identification cellule tumorale / non tumorale

### Cas limite
- Multiplier le nombre de cellules analysées
- **Seconde lecture** par observateur indépendant
- Analyser un **autre bloc** si nécessaire

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p21_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p22_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p23_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16.650_FISH_Generalites/p24_00.jpeg]]

## Indications cliniques majeures

| Sonde | Indication | Critère |
|-------|------------|---------|
| **HER2** | Cancer du sein, gastrique | Énumération + ratio HER2/CEP17 |
| **ALK** break-apart | Adénocarcinome pulmonaire | **≥ 15 %** cellules splittées |
| **ROS1** break-apart | Adénocarcinome pulmonaire | **≥ 15 %** |
| **MYC, BCL2, BCL6** break-apart | DLBCL (double/triple-hit) | Selon entité |
| **COL1A1-PDGFB** dual fusion | DFSP (dermatofibrosarcome de Darier-Ferrand) | Diagnostic |
| **EWSR1** break-apart | Sarcome d’Ewing, autres | Diagnostic |

## Compte rendu — items obligatoires

| Item | Détail |
|------|--------|
| **Identification** précise du prélèvement | Patient, bloc, date |
| **Technique** | Type, automate ou manuel |
| **Sonde** utilisée | **Nom commercial obligatoire** |
| **Critères de positivité** | Avec **référence bibliographique** |
| **Qualité technique** | Interprétabilité |
| **Nombre de cellules analysées** | Ex. > 1000 |
| **Nombre de cellules comptées** | Ex. 20 |
| **Résultat** du comptage | Détaillé |
| **Conclusion** | + commentaires éventuels |

## Concordance & archivage

- Toujours confronter le résultat **FISH** au tableau **morphologique, IHC, biologie moléculaire, clinique**
- **Archiver les lames** au congélateur **≥ 1 an**
- Conserver les **captures d’image** sur informatique

## Avantages / Limites de la lecture

| Qualités requises du lecteur | Limites |
|------------------------------|---------|
| **Patience** apprentissage et lecture | Subjectivité partielle |
| **Régularité** (habilitation) | Variabilité interlecteurs |
| **Exhaustivité** (toute la lame) | Temps long |
| **Pragmatisme** dans l’interprétation | Critères évolutifs |
| **Culture bibliographique** récente | – |
| **Curiosité** face aux aspects inhabituels | – |
| **Dialogue multidisciplinaire** | – |

---

## 🔑 Points clés à retenir

1. **Toujours connaître** : indication, question posée, **fiche technique de la sonde** (couleur du gène et du centromère).
2. **Filtre DAPI d’abord** : repérage tumeur via HES, qualité de la digestion (noyaux **troués = digestion excessive**).
3. **Vrai spot** = intranucléaire, rond, fluorescence intense, couleur appropriée — préférer **filtres monobandes**.
4. **Ne JAMAIS remettre au point** entre acquisition vert et rouge (sonde break-apart) → faux signaux de séparation.
5. **Témoin interne négatif** = territoire non tumoral : si profil inattendu = **erreur de sonde**.
6. **Balayer toute la lame** (amplification HER2 hétérogène dans le **gastrique** notamment).
7. Pièges : autofluorescence macrophages/mastocytes, artefacts d’écrasement, cellules géantes anormales, superpositions.
8. **Sondes break-apart** : seuil **≥ 15 %** ; zone limite **10-30 %** = méfiance.
9. **L’interprétation précède le comptage** : le comptage illustre la lecture visuelle ; analyser **toute** la tumeur.
10. **Compte rendu** doit comporter : nom de la sonde, **critères de positivité avec référence**, nombre de cellules analysées et comptées, qualité, conclusion.
