---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - proteine_ihc
  - IHC
  - multiplex
  - OPAL
  - tyramide
  - IF
  - immunoscore
  - colocalisation
  - analyse_digitale
date: 2024
source: DES ACP - Pathologie moléculaire
---

# IHC multiplex (multiplexée)

> Liens : [[16_935 L'immunohistochimie - outil complémentaire de la biologie moléculaire]] | [[16_1015 Cycle de l'immunité anti-tumorale]] | [[16_1020 Rationnel de l'immunothérapie]] | [[16_1035 Statut MSI en onco-immunologie]] | [[16_630 La FISH appliquée à l'anapath]]

## Principe

L’**IHC multiplexée** = détection **simultanée de plusieurs marqueurs** (protéines via anticorps, ADN/ARN via sondes) sur **un seul support** (une seule lame). Permet :
- d’économiser un **tissu de petite taille** (biopsies, micro-prélèvements)
- d’étudier la **co-expression** et la **colocalisation** de plusieurs marqueurs
- de caractériser des **populations cellulaires** et des **niches** spécifiques (micro-environnement)
- d’explorer les **interactions cellulaires** et la **proximité** (analyse spatiale)





## Exemples d’application diagnostique

| Combinaison | Indication |
|-------------|------------|
| **HER2 (violet) + RA (DAB) + p63 (jaune)** | DD carcinome canalaire **in situ vs infiltrant** |
| **miR-205 (argentique noir) + BCL2 (violet)** | Lien **micro-ARN ↔ protéine cible** oncogénique |
| **CD3 + CD8 + FoxP3** (triplex) | **Immunoscore** (TIL) |
| **CD4 + FoxP3** (duplex) | Identification des **Treg** |




![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p03_00.jpeg]]

# 1. Méthodes de détection

## Deux types de détection

| Détection | Visualisation | Avantages | Limites |
|-----------|---------------|-----------|---------|
| **Chromogénique** | Lumière blanche | Archivage **> 10 ans**, morphologie préservée | **2 marqueurs max**, palette limitée |
| **Fluorescente** | Microscope à fluorescence (spectral si > 4 marqueurs) | Jusqu’à **20 marqueurs**, bibliothèque étendue, colocalisation aisée | Coût élevé, **fading** au cours du temps |

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p03_01.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p03_02.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p03_03.jpeg]]

## Deux types de protocoles

### Méthode conventionnelle (concomitante)

- Application **simultanée** de plusieurs anticorps **primaires directement conjugués**
- **Une seule étape** d’incubation
- **Anticorps obligatoirement d’espèces différentes**
- Amplification limitée
- **Maximum** : 2 marqueurs en chromogénique / 4 marqueurs en fluorescence

### Méthode séquentielle (TSA / OPAL)

- Application **étape par étape** ; les anticorps **peuvent être de la même espèce**
- Amplification du signal par **TSA** (Tyramide Signal Amplification)
- **Étapes de dénaturation** entre chaque anticorps (chaleur micro-ondes)
- **Automatisable**
- **Permet d’augmenter considérablement le nombre de marqueurs** (jusqu’à 20)

#### Principe TSA / OPAL

1. Incubation de l’**anticorps primaire**
2. **Peroxydase HRP** catalyse la **tyramide** en radicaux libres hautement réactifs
3. Liaison **covalente** des radicaux à la **tyrosine près de l’épitope** (signal stable et localisé)
4. **Dénaturation par la chaleur** (élimination de l’anticorps primaire/secondaire mais conservation du signal)
5. **Itération** avec un nouvel anticorps de la même ou autre espèce

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p04_00.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p04_01.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p04_02.jpeg]]






# 2. Comparaison chromogénique vs fluorescence

| Critère | Chromogénique | Fluorescente |
|---------|---------------|--------------|
| Visualisation | Lumière blanche | Microscope fluorescence (spectral si > 4) |
| Archivage | **> 10 ans** | Limité (perte d’intensité) |
| Coût | Plus élevé | Moins coûteux |
| Capacité multiplex | Limitée (≤ 2-3) | **Élevée** (jusqu’à 20) |
| Bibliothèque de couleurs | Limitée | **Étendue** |
| Colocalisation | Difficile | **Facilitée** |
| Morphologie | **Préservée** | Moins lisible |

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p06_00.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p06_01.jpeg]]


![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p07_00.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p07_01.jpeg]]

# 3. Recommandations générales

## Caractérisation des anticorps primaires

- Optimisation d’un **système de détection robuste**, **identique** entre simplex et multiplex
- **Validation individuelle** de chaque marquage **avant** le multiplex
- Vérifier que l’encombrement en série **n’affecte pas le marquage** du second antigène
- Connaître la **localisation subcellulaire** des anticorps pour **éviter l’overlap chromogénique**

## Cartographie des épitopes

- Choix optimal des **contrôles** pour éviter co-expression faux positive ou faux négative
- Anticipation du **signal attendu** (type cellulaire, compartiment, intensité)

## Astuces multiplex séquentiel

- Anticorps **souris ou lapin** sur clones **raffinés**
- **Fluorochromes / chromogènes** : éviter les voisins, choisir des chromogènes superposables avec **≥ 20 nm d’écart**
- **Marquage trop fort** → choisir un fluorochrome plus faible
- Étape **monochrome** préalable : déterminer la **concentration adaptée** de chaque anticorps primaire
- Forte amplification = diminuer la concentration
- Déterminer la **tolérance à la dénaturation** (chaleur micro-ondes / IVR)

## Approche chromogénique

- Cocktail d’anticorps primaires d’**espèces différentes** rare (démasquage enzymatique → **séquentiel**)
- Plus fréquemment : anticorps de **même espèce** en séquentiel
- **DAB en premier** : effet **« parapluie »** = blocage des sites de liaison à proximité immédiate → **diminue les faux positifs**
- Inhibition des peroxydases endogènes : **PBS-IgG**
- Détection : **peroxydase** ou **phosphatase alcaline**



![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p09_00.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p10_00.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p11_00.jpeg]]


# 4. Pré-traitement & démasquage

| Type | Indication | Précaution |
|------|-----------|------------|
| **Démasquage enzymatique** (protéase) | Certaines kératines | Détruit les marquages **membranaires** des lymphocytes → à utiliser **en dernier** |
| **Démasquage par la chaleur** (citrate, EDTA) | La majorité des marqueurs | Vérifier la tolérance des autres épitopes |

→ Anticiper les **co-marquages attendus** avec un outil de **prévisualisation**.

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p13_00.jpeg]]


# 5. Établir un protocole multiplex — étapes

1. **Marquage de référence** : coloration séparée de chaque marqueur pour évaluer le niveau d’expression
2. Test du **double marquage** entre les **deux marqueurs les plus semblables** en localisation/expression
3. Tester **toutes les combinaisons** (4 lames typiquement)
4. **Déterminer la séquence** des chromogènes/fluorochromes

## Exemple — triplex CD3 / CD8 / FoxP3

| Anticorps | Espèce | Localisation |
|-----------|--------|--------------|
| **CD8** | Souris | Membrane (sous-pop CD3+) |
| **CD3** | Lapin | Membrane (pop majeure) |
| **FoxP3** | Souris | **Nucléaire** (sous-pop) |

Tous les CD8+ sont CD3+ ; tous les CD3+ ne sont **pas** CD8+.

### Règle clé : appliquer en premier le marqueur le plus faible

- Si **CD3 (fort) en premier** + CD8 (DAB ou violet) en second → **CD8 caché** par CD3
- Si **CD8 (faible) en premier** + CD3 en second → les **deux marqueurs visibles**
- → On obtient les **meilleurs résultats** lorsque le marqueur le **plus faible** est appliqué en **premier**

Une fois la séquence CD8 → CD3 établie, intercaler le **FoxP3 nucléaire** (visible dans tous les cas).

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p15_00.jpeg]]



![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p18_00.jpeg]]

## Séquence des fluorophores

Mêmes règles : appliquer le **plus faible en premier**.

Exemple duplex CD3 (FITC) + CD8 (rhodamine) :
- CD3-FITC en premier → cache CD8
- CD8 en premier → CD3 visible
- Rhodamine en premier → cache le signal FITC

→ Fluorescence **optimale** pour la **colocalisation** (cellule co-exprimant CD3 + CD8 visible en jaune fusionné).





# 6. Validation de la spécificité

- **Validation des isotypes**
- **Blocage des enzymes endogènes**
- Recherche de **réactions croisées** de l’anticorps primaire (rôle du titrage)
- **Tests de décrochage** (notamment pour la méthode séquentielle)

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p21_00.jpeg]]

![[assets/pathologie-moleculaire/proteine/16-940_IHCmultiplex_Audio/p21_01.jpeg]]

# 7. Analyse digitale

- **Logiciels** d’analyse d’image dédiés (HALO, QuPath, inForm…)
- Permettent : co-marquage, **interaction cellulaire**, identification de sous-populations, analyse de **proximité spatiale**
- Limites : **compatibilité** entre logiciels variable
- Avantages : **partage des résultats**, travail en réseau




# 8. Application phare — Immunoscore

- **Duplex CD3 / CD8** au niveau du **centre** de la tumeur **et** du **front d’invasion**
- **Analyse digitale** quantitative
- Validé comme **facteur prédictif majeur** de l’évolution clinique des **cancers colorectaux**, parfois **supérieur** au TNM
- Application également au **scoring PD-L1** combiné aux **TIL** dans l’évaluation de la réponse à l’immunothérapie




# Indications cliniques / Applications

- **Caractérisation du micro-environnement** tumoral (TIL, Treg, TAM)
- **Scoring PD-L1 + TIL** pour la sélection à l’immunothérapie
- Diagnostic différentiel (ex. **HER2/RA/p63** : in situ vs infiltrant)
- **Recherche translationnelle** : voies de signalisation, communication intercellulaire
- **Immunoscore** validé en CCR

# Pièges / Limites

- **Mise au point fastidieuse** ; coût élevé, surtout en fluorescence
- Effet **parapluie de la DAB** : à utiliser en premier en chromogénique
- **Marqueur faible toujours en premier** (chromogénique ET fluorescence)
- **Démasquage enzymatique** = **dernier** (détruit les marquages membranaires)
- Anticorps **même espèce** ne sont accessibles qu’en **séquentiel** (TSA)
- **Fading** des fluorochromes → archivage limité
- Compatibilité limitée entre **logiciels** d’analyse digitale

---

## 🔑 Points clés à retenir

1. L’IHC **multiplex** détecte **plusieurs marqueurs simultanément** (protéines + sondes ADN/ARN) sur **une seule lame**.
2. **Deux protocoles** : **conventionnel** (concomitant, anticorps d’espèces différentes, ≤ 4 marqueurs) vs **séquentiel** (TSA/OPAL, même espèce possible, jusqu’à 20 marqueurs).
3. **TSA/OPAL** = peroxydase + **tyramide** → liaison **covalente** à la **tyrosine** près de l’épitope ; dénaturation thermique entre étapes.
4. **Fluorescence** : multiplexage élevé, colocalisation aisée, mais **fading** et coût élevé.
5. **Chromogénique** : morphologie préservée, archivage > 10 ans, mais ≤ 2-3 marqueurs.
6. Règle d’or : **appliquer en premier le marqueur le plus faible** pour qu’il soit visible.
7. **DAB en premier** en chromogénique : effet **parapluie** anti faux positifs.
8. Démasquage **enzymatique en dernier** (détruit les marquages membranaires).
9. **Validation individuelle** de chaque anticorps **avant** le multiplex (témoins, isotypes, décrochages).
10. Application phare = **immunoscore CD3/CD8** (centre + front d’invasion) — facteur prédictif majeur en **CCR**, base du scoring **PD-L1 + TIL** en immunothérapie.
