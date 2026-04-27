---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_adn
  - bases_de_données
  - COSMIC
  - ClinVar
  - cBioPortal
  - TCGA
  - ICGC
  - Human_Protein_Atlas
  - GeneCards
  - oncologie_moléculaire
  - bio-informatique
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Bases de données génomiques internationales

> Liens : [[16_115 Différents types de séquences du génome humain]] | [[16_510 NGS - Principes et applications]] | [[16_535 Pipeline bio-informatique]] | [[16_830 Puces à ADN dans l'étude de l'expression des gènes (transcriptome) Définition d'une signature]]

## Contexte — explosion des données multiomiques

- Coût des analyses moléculaires (exome, génome, **RNA-seq**) : **diminution majeure**
- Conséquence : taille et **nombre des datasets** ont explosé
- Comparaison historique :
  - Années 2000 : première classification des cancers du sein → **85 tumeurs**, profil de **500 gènes**
  - 2019 : classification des tumeurs pancréatiques → **> 300 tumeurs**, **WGS + RNA-seq + méthylation + réarrangements**

Disponibilité accrue : nombreux journaux **imposent la publication des données brutes** lors de l’acceptation.


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p02_00.jpeg)

## Principaux consortiums internationaux

| Consortium | Données disponibles |
|-----------|---------------------|
| **TCGA** (The Cancer Genome Atlas) | ADN, ARN, méthylation, parfois protéomique, sur de nombreux cancers |
| **ICGC** (International Cancer Genome Consortium) | Idem, échelle internationale |

Portails web modernes : **agrégation** des données + **visualisation interactive** + **analyses simples** (ex : corrélation mutation ↔ survie, mutation ↔ expression).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p07_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p08_00.jpeg)

## Applications cliniques pour le pathologiste

### Annotation d’un variant
- Variant **déjà décrit** ?
- Statut : **pathogène / VUS / bénin** ?
- **Fréquence** dans un type de tumeur particulier ?

### Tumeur de primitif inconnu (CUP)
- Anomalie moléculaire rare (transcrit de fusion, mutation peu commune) → recherche dans les bases pour **orienter vers un primitif** spécifique

### Impact clinique d’une anomalie
- Mutation associée à **meilleur** ou **moins bon pronostic** ?
- Idem pour transcrits de fusion

## Applications recherche

- Corrélation **ARN ↔ méthylation**
- Signature transcriptomique ↔ survie
- Datasets utilisés comme **cohortes de validation** externes
- Bases d’**effets de drogues sur lignées** : associer drogue ↔ statut moléculaire (ex : drogue A efficace si gène X muté)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p09_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p10_00.png)

## Caractéristiques des portails

- **Changeants** : certains ferment, d’autres très dynamiques (revisiter régulièrement)
- 2 types principaux :
  - **Repositories de données brutes** (téléchargement uniquement)
  - **Portails analytiques** (plug-and-play, sans codage)
- Ergonomie variable → consulter les **tutoriels** (sur le portail ou YouTube)

## Liste (non exhaustive) des portails utiles

| Portail | Type | Usage principal |
|---------|------|-----------------|
| **cBioPortal** | Analytique | TCGA + ICGC + autres ; analyses interactives par dataset/gène |
| **COSMIC** | Variants | Catalogue de mutations somatiques en cancer |
| **ClinVar** | Variants | Classification pathogène/bénin/VUS |
| **TCGA / ICGC portals** | Consortia | Analyses simples (mutations, survie, fréquences) |
| **Human Protein Atlas** | ARN + IHC | Expression ARN par tumeur + IHC sur TMA |
| **NCBI GEO**, **ArrayExpress** | Repositories | Téléchargement de datasets bruts (ré-analyse maison) |
| **GeneCards** | Annotation gène | Fonction, noms alternatifs, fournisseurs anticorps/plasmides |

## ⚠ Attention à la qualité des données

- Les annotations **histologiques** ne sont **pas toujours parfaites**
- Discordances possibles entre portails pour **un même dataset**
- Annotations cliniques inégales

### Exemple — TCGA "cancer du pancréas" (185 patients)
- Cohorte non nettoyée : 185 patients ⇒ **incluant** :
  - Lésions **neuro-endocrines**
  - **Carcinomes acineux**
  - Pancréas sain
  - Tumeurs en poulet
  - Patients **pré-traités**
- Cohorte nettoyée : seulement **150 adénocarcinomes ductaux naïfs**

**Impact** : la survie et les gènes associés à la survie sont **complètement différents** entre cohorte non nettoyée et cohorte nettoyée → exemple du gène **TWIST1**, valeur pronostique perdue après nettoyage.

→ **Toujours nettoyer / vérifier** la composition d’une cohorte avant analyse.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p11_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p12_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p13_00.png)

## GeneCards — fiche d’identité d’un gène

- **Pas de données à télécharger**
- Pour un gène : **fonction**, **synonymes** (utile car nomenclature variable), **liens vers fournisseurs** (anticorps, plasmides — à vérifier)
- Idéal pour identifier rapidement la fonction d’un gène inconnu

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p14_00.png)

## ClinVar — variants

- Base **bien maintenue** et mise à jour
- Pour un variant : recherche par notation **protéique** ou **génomique**
- Donne le statut : **pathogène / probablement pathogène / VUS / probablement bénin / bénin**
- Critères associés + publications listées

Exemple : *KRAS* codon 61 → consultable directement.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p15_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p16_00.png)

## COSMIC — variants somatiques en cancer

Très utilisé pour les variants. Pour un gène (ex : **KRAS**) :
- Carte de tous les variants connus (visualisation des **hotspots** : codons 12, 13, **61**)
- Pour chaque mutation : type de variant, classification pathogénique, **distribution dans les types tumoraux**
- Utile pour les **CUP** : voir dans quels organes une mutation rare est rapportée
- Nouveaux outils : **prédiction de l’impact 3D** d’un variant si la protéine est cristallisée (changement conformationnel, site catalytique)

⚠ Discordances possibles entre **COSMIC** et **ClinVar** (sources différentes) → **consulter plusieurs portails**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p17_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p18_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p20_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p21_00.png)

## cBioPortal — portail analytique majeur

Agrège **TCGA + ICGC + datasets de publications**. Outil très riche, fonctions nouvelles régulières.

⚠ **Nettoyage des données pas toujours parfait** (ex : TCGA pancréas → 185 échantillons toujours visibles ; case à cocher pour limiter aux ADK ductaux).

### Navigation
1. **Localisation tumorale** → datasets disponibles
2. Sélection d’un ou plusieurs datasets
3. Choix du mode :
   - **Analyse globale** d’un dataset
   - **Analyse par gène** ou liste de gènes

### Analyse globale
- Survie globale, survie sans progression
- Gènes les plus fréquemment **mutés**
- Transcrits de **fusion**
- Gènes **délétés / amplifiés**
- Sélection d’une anomalie (ex : amplification GATA6) → mise à jour automatique des autres données
- **Customisation** : combiner plusieurs anomalies (ex : amplification GATA6 + mutation TP53)

### Analyse par gène (ex : SMAD4)
- Fréquence des **différents types d’altérations** (43 % dans la cohorte)
- Impact sur survie sans progression / survie globale
- **Distribution des mutations** dans les domaines protéiques (missense, troncantes, in-frame)
- Identification des mutations **classiquement pathogéniques** (icône flamme)
- **Co-expression** : gènes les plus associés (ex : *MAPK10* avec *SMAD4*)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p22_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p23_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p24_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p25_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p26_00.png)

## Human Protein Atlas

Agrège :
- Données **ARN** des consortiums internationaux (TCGA, etc.)
- Données **protéiques par IHC** sur tissu sain, lignées cellulaires, tumeurs (TMA)

⚠ Une partie des données protéiques retirées (mauvaise qualité). Reste utile pour :
- Voir l’**expression ARN** d’un gène par type de tumeur
- Évaluer l’**association ARN ↔ pronostic**
- Visualiser le **pattern** de marquage IHC (membranaire/nucléaire/cytoplasmique)
- **Sélectionner un anticorps** (références fournies, souvent **Abcam**, **Sigma**)

⚠ **Limitations** :
- Anticorps **anciens**, marquage parfois insatisfaisant
- Sélection **TMA** parfois contestable (ex : tumeurs neuro-endocrines mêlées dans TMA pancréas)
- À utiliser avec **circonspection**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p27_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p28_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p29_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-190%20Base%20de%20donn%C3%A9es%20g%C3%A9nomiques%20internationales/p30_00.jpeg)

## Conclusion — bonnes pratiques

| Bonne pratique | Justification |
|----------------|--------------|
| **Croiser les portails** | Discordances possibles, sources différentes |
| **Vérifier la composition** d’une cohorte | Annotations histologiques imparfaites |
| Consulter les **tutoriels** | Fonctions avancées sous-utilisées |
| Utiliser comme **cohortes de validation** | Évite de monter une cohorte externe coûteuse |
| **Croisement multiomique** (ARN/ADN/protéine/méthylation) | Vision intégrée des cancers |

Bases idéales pour :
- **Annotation de variants** (COSMIC, ClinVar)
- **Hypothèses de recherche** : impact d’une mutation sur le transcriptome avant de financer un RNA-seq maison
- **Validation** d’observations dans des cohortes propres

---

## 🔑 Points clés à retenir

1. Effondrement du **coût** des analyses → **explosion des datasets multiomiques** publiés
2. **TCGA** et **ICGC** = principaux consortiums (ADN, ARN, méthylation, ± protéome)
3. **cBioPortal** = portail d’analyse interactive majeur (mutations, survie, co-expression)
4. **COSMIC** = catalogue des mutations somatiques en cancer (hotspots, distribution organes)
5. **ClinVar** = classification pathogène / VUS / bénin avec critères et publications
6. **GeneCards** = fiche d’identité d’un gène (fonction, synonymes, fournisseurs)
7. **Human Protein Atlas** = expression ARN par tumeur + IHC sur TMA (avec précautions)
8. **GEO / ArrayExpress** = repositories de données brutes (analyse maison)
9. ⚠ **Annotations histologiques inégales** : exemple TCGA pancréas (185 vs 150 ADK ductaux nettoyés)
10. Toujours **croiser les portails** (discordances possibles entre sources)
11. Consulter les **tutoriels** (portail, YouTube) pour exploiter les fonctions avancées
12. Usage clinique : annotation de variants ; usage recherche : hypothèses + cohortes de validation
