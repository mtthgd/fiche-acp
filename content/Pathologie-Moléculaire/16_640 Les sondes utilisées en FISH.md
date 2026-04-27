---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - cytogénétique
  - FISH
  - sondes_centromériques
  - sondes_télomériques
  - sondes_locus_spécifique
  - sondes_peinture
  - sondes_fusion
  - sondes_break_apart
  - fluorochromes
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Les sondes utilisées en FISH

> Liens : [[16_630 La FISH appliquée à l'anapath]] | [[16_650 FISH généralités]] | [[16_620 Principes de cytogénétique]] | [[16_670 Analyse automatisée des lames FISH - partie 1]]

## Principe / Bases

Les sondes utilisées en **FISH** (Fluorescence In Situ Hybridization) sont des fragments d’ADN spécifiques d’une cible chromosomique, marqués par un fluorochrome (direct) ou un haptène (indirect). Elles s’hybrident à leur séquence cible dénaturée et sont visualisées en microscopie à fluorescence.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p01_00.jpeg]]

## Acteurs / Sondes / Réactifs — Typologie

| Type de sonde | Cible | Application principale |
|---------------|-------|------------------------|
| **Sondes centromériques (CEP)** | Séquences satellites répétées du centromère | **Contrôle interne**, énumération chromosomique |
| **Sondes télomériques** | Séquences répétées (**TTAGGG**) télomériques | Mesure de longueur des télomères (**Telish**), souvent identiques entre chromosomes |
| **Sondes locus-spécifiques (LSI)** | Locus précis portant un gène | Anomalies **quantitatives ou qualitatives** ciblées |
| **Sondes de peinture chromosomique** | Couvre l’ensemble d’un chromosome | Caryotype multicouleur (**M-FISH, SKY**) |
| **Sondes de bras chromosomique** | Bras court ou long entier | Inversions, perte de bras (déséquilibre) |

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p02_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p02_01.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p03_00.jpeg]]

## Origine et fabrication des sondes

### Sondes commerciales (cas le plus fréquent en pathologie)
- Synthèse d’**oligonucléotides longs** mélangés pour atteindre un signal détectable
- **Production de fragments** clonés dans des vecteurs **BAC** (Bacterial Artificial Chromosome) — banques accessibles
- **Marquage incorporé** par **nick translation** ou conjugaison chimique
- Conservation contrôlée : **durée limite + température adaptée**

### Sondes maison
- Possible mais nécessite gestion du marquage (haptène ou fluorochrome) et contrôle qualité
- Moins utilisée en routine pathologique



## Fluorochromes & filtres

Chaque fluorochrome est caractérisé par :
- Un **spectre d’excitation** (longueur d’onde absorbée)
- Un **spectre d’émission** de longueur d’onde **plus grande** (lumière émise observée)

| Fluorochrome | Couleur émise |
|--------------|---------------|
| **FITC** | Vert |
| **Texas Red** | Rouge |
| **Aqua Blue** | Bleu |
| **DAPI** (contre-coloration) | Bleu intense (ADN total) |

> Vérifier que les **filtres du microscope** correspondent aux fluorochromes commandés en testant sur **tissus contrôles témoins** avant analyse pathologique.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p05_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p05_01.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p06_00.jpeg]]

## Workflow technique

| Étape | But |
|-------|-----|
| **Pré-traitement** | Permettre l’accès des sondes (digestion ménagée) |
| **Déshydratation** | Stabilisation |
| **Application de la sonde + scellement** (colle) | – |
| **Co-dénaturation** sonde + cible | Séparation des brins |
| **Hybridation overnight** | Appariement spécifique |
| **Lavage stringent** (J2) | Élimination de l’excès de sonde |
| **Contre-coloration DAPI** | Visualisation des noyaux + anti-fading |
| **Observation** au microscope à fluorescence | Acquisition d’image (réglementaire) |

> **Observation en filtre double** confirmée par **filtre simple alterné**, acquisition successive en **plusieurs plans Z**.


![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p09_00.jpeg]]

### Détermination du seuil de positivité
- Sur **plusieurs échantillons contrôles non tumoraux** (ex. ganglion réactionnel)
- Calcul : **moyenne + 3 écarts-types** des noyaux anormaux dans le contrôle

## Type de sonde et profils d’interprétation

### 1. Sondes pour anomalies de nombre / amplification

| Profil | Aspect |
|--------|--------|
| **Équilibré** (normal) | 2 verts + 2 rouges, ratio ≈ 1 |
| **Gain** | > 2 copies du gène |
| **Amplification spécifique** | **> 5 copies** + ratio gène/contrôle **> 2** |
| **Polysomie** | Plusieurs copies du chromosome (gène + centromère) |

> **Piège** : > 2 copies peut être un gain spécifique ; **> 5 copies** est une amplification spécifique. Les cellules tumorales sont souvent **polyploïdes** → utiliser une sonde **contrôle centromérique** pour rétablir le **ratio locus/contrôle**.

Exemple **MET** (7q31, sonde verte) + CEP7 (rouge) — profils équilibré / gain / amplifié.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p09_01.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p10_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p10_01.jpeg]]

### 2. Sondes pour délétion

Exemple **9p21** (CDKN2A — code **p16/p14**) dans le **mésothéliome** :
- Sonde verte = locus 9p21
- **Délétion homozygote** : pas de signal vert dans les cellules tumorales
- Cellules normales = témoin interne d’hybridation indispensable

> **Limite** : les **micro-délétions** peuvent échapper à la FISH → biologie moléculaire complémentaire nécessaire.

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p11_00.png]]


### 3. Sondes pour translocation réciproque

#### Sondes **double couleur double fusion** (sondes de fusion)

| Composition | 1 sonde rouge spécifique d’un gène (ex. **BCL2**) + 1 sonde verte spécifique du partenaire (ex. **IGH**) |
|-------------|------|
| **Profil normal** | 1 rouge + 1 vert séparés (×2) |
| **Profil transloqué** (ex. t(14;18)) | **2 fusions** + 1 rouge + 1 vert isolés (allèles non réarrangés) |
| **Avantage** | Identifie le **partenaire** |
| **Limite** | Faux signaux de fusion par superposition |

#### Sondes **break-apart / split / encadrantes**

| Composition | Sonde rouge + sonde verte de part et d’autre du **point de cassure** d’un seul gène |
|-------------|------|
| **Profil normal** | **Fusion (jaune)** ×2 |
| **Profil transloqué** | 1 fusion + **1 rouge isolé + 1 vert isolé** |
| **Avantage** | Adapté aux gènes **polygames** (**ALK, MYC, EWSR1**) |
| **Limite** | N’identifie pas le partenaire |

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p12_00.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p12_01.jpeg]]

![[assets/pathologie-moleculaire/methodes-etudes-adn/16-640 Les sondes utilisées en FISH-Merlio/p12_04.jpeg]]

## Lecture / Interprétation — pièges des sondes break-apart

| Piège | Conséquence |
|-------|-------------|
| **Variant de point de cassure tombant sur la sonde rouge** | **Extra-rouge** (signal supplémentaire) |
| **Variant tombant en dehors de la zone couverte** | **Faux négatif** : persistance de la fusion malgré un réarrangement |
| Inversion paracentrique (ex. **EML4-ALK**) | Spots seulement à 2-3 diamètres → difficile à distinguer du normal |

## Indications cliniques majeures

| Type de sonde | Cible | Indication |
|---------------|-------|------------|
| **CEP** | CEP17 | Contrôle interne pour **HER2** |
| **LSI énumération** | **HER2/CEP17** | Sein, gastrique |
| **Break-apart** | **ALK** (2p23) | Adénocarcinome pulmonaire |
| **Break-apart** | **ROS1** (6q22) | Adénocarcinome pulmonaire |
| **Break-apart** | **MYC** (8q24) | Lymphome de Burkitt, DLBCL |
| **Break-apart** | **EWSR1** (22q12) | Sarcome d’Ewing, sarcome à cellules claires, DSRCT |
| **Dual fusion** | **BCR-ABL** | LMC |
| **Dual fusion** | **MYC-IGH** | Lymphome de Burkitt |
| **Dual fusion** | **BCL2-IGH** | Lymphome folliculaire |
| **LSI délétion** | **9p21** (CDKN2A) | Mésothéliome |
| **LSI** | **MDM2** (12q15) | Liposarcome bien différencié/dédifférencié |

## Avantages / Limites

| Avantages | Limites |
|-----------|---------|
| Visualisation **in situ** ciblée | Détection **micro-délétions** insuffisante |
| Adaptable à divers échantillons | Variants de point de cassure → faux négatifs |
| Faisable sur tissus FFPE | Polyploïdie tumorale → surestimation sans sonde contrôle |
| Multiplexage possible (panel) | Coût des sondes commerciales |

---

## 🔑 Points clés à retenir

1. **5 grandes catégories de sondes** : centromériques (CEP), télomériques, **locus-spécifiques (LSI)**, peinture chromosomique, bras chromosomique.
2. **Sondes commerciales** majoritaires (BAC clonés, oligonucléotides longs) ; marquage par **nick translation** ou conjugaison chimique.
3. **Marquage direct** (fluorochrome : FITC vert, Texas Red rouge, Aqua Blue) ou **indirect** (haptène : digoxygénine, biotine).
4. **DAPI** = contre-coloration nucléaire bleue + anti-fading.
5. Vérifier la **correspondance filtres-fluorochromes** sur tissus contrôles avant analyse — sinon erreur diagnostique majeure.
6. **Seuil de positivité** = moyenne + 3 ET des noyaux anormaux dans contrôles non tumoraux.
7. **Amplification spécifique** : > 5 copies + ratio gène/contrôle **> 2** ; toujours utiliser une sonde **centromérique contrôle** (cellules polyploïdes).
8. **Sondes dual fusion** = partenaires connus (BCL2-IGH, MYC-IGH) ; **break-apart** = gènes polygames (**ALK, MYC, EWSR1**).
9. **Limite des break-apart** : variant de cassure → **extra-rouge** ou **faux négatif** (cassure hors zone couverte).
10. La FISH est **complémentaire** : micro-délétions et translocations à variants atypiques nécessitent biologie moléculaire (NGS, RT-PCR).
