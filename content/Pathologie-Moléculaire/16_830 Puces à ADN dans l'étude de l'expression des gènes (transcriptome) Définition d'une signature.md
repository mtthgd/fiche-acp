---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_arn
  - microarray
  - puces_ADN
  - transcriptome
  - signature_génique
  - RNA-seq
  - cancer_du_sein
  - PAM50
  - DLBCL
  - clustering_hiérarchique
  - Nanostring
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Puces à ADN dans l’étude de l’expression des gènes (transcriptome) — Définition d’une signature

> Liens : [[16_510 NGS - Principes et applications]] | [[16_240 Voies de signalisation en oncologie]] | [[16_220 Signatures pronostiques en pathologie tumorale]] | [[16_115 Différents types de séquences du génome humain]] | [[16_190 Bases de données génomiques internationales]]

## Définitions

| Terme | Définition |
|-------|------------|
| **ARN codants (ARNm)** | Traduits en protéines = **2 %** des ARN totaux |
| **ARN non codants** | Non traduits → maturation des ARNm, **régulation post-transcriptionnelle**, etc. |
| **Transcriptome** | Ensemble des ARN présents dans une **population de cellules** dans des conditions données (souvent réservé aux **ARNm**) |


![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p02_00.png]]

## Pourquoi étudier le transcriptome ?

| Application | Apports |
|-------------|---------|
| **Classifications moléculaires des cancers** | Découverte de nouvelles entités, voies de signalisation, cellule d’origine |
| **Pronostic** | Identification de signatures pronostiques |
| **Prédiction de réponse au traitement** | Signatures prédictives |
| **Découverte de cibles thérapeutiques** | Nouvelles approches |

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p02_01.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p03_00.png]]

## Comment étudier le transcriptome — techniques haut débit

### Évolution des techniques
1. Puces à **ADN** (cDNA arrays) — origine
2. Puces à **oligonucléotides** (Affymetrix, Agilent, Illumina)
3. **Séquençage haut débit** des ARN = **RNA-seq** (technique actuelle)

### Principe général
À partir de plusieurs tumeurs/conditions :
1. Caractérisation moléculaire **globale**
2. Comparaison des profils
3. Émergence d’une **signature moléculaire** caractéristique
4. Validation sur **cohorte indépendante**
5. Validation **prospective** patient par patient (médecine personnalisée)

→ Nécessite des **grandes cohortes** pour s’assurer que le différentiel d’expression est **robuste, non lié au hasard**.

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p03_02.png]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p03_04.jpeg]]

## Microarray vs RNA-seq

| Critère | Microarray (Affymetrix, Agilent, Illumina) | RNA-seq |
|---------|---------------------------------------------|---------|
| **Détection** | Seulement ce qui est présent comme **sonde** sur la puce | Tous les ARN présents |
| **Sensibilité** | Constante | Variable selon **profondeur de séquençage** |
| **Sensibilité aux ARN faiblement exprimés** | Moyenne | **Excellente** |
| **Détection de nouveaux transcrits / transcrits alternatifs** | Limitée | **Possible** |
| **Détection de polymorphismes** | Non (sauf puces SNP dédiées) | **Oui** |
| **Coût** | Moindre | **Plus élevé** |
| **Banques de données** | Très **abondantes** | Moins abondantes |
| **Temps d’analyse** | Court | **Long** |


![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p09_01.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p10_00.jpeg]]

## Workflow d’une puce ADN (Affymetrix)

1. **Extraction** des ARN du tissu
2. **Préparation des cibles** : ARN marqués (fluorochrome)
3. **Hybridation** des cibles sur les **sondes** spotées sur la puce
4. **Acquisition** des données (scanner)
5. Conversion en **données d’expression**
6. **Filtrage du bruit de fond** + **normalisation**
7. **Interprétation**

L’**intensité de fluorescence** émise est **proportionnelle à la quantité d’ARNm** cible hybridé sur la sonde.

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p11_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p11_01.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p11_02.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p12_00.jpeg]]

## Visualisation — Heatmap et clustering hiérarchique

| Élément | Signification |
|---------|---------------|
| **Ligne** | Une **sonde** (= niveau d’expression d’un gène à travers toute la cohorte) |
| **Colonne** | Une **tumeur** (= niveau d’expression de tous les gènes de la puce) |
| **Vert** | Gène **faiblement exprimé** |
| **Rouge** | Gène **fortement exprimé** |

Le **clustering hiérarchique** rapproche les échantillons à profils d’expression similaires (dendrogramme).

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p13_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p13_01.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p14_00.jpeg]]

## Évolution historique du domaine

- Début des techniques de microarray : **années 2000**
- Croissance exponentielle des publications PubMed sur "*cancer gene expression signature*"

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p14_03.png]]

## Approche non supervisée (class discovery)

Définit des classes de tumeurs sur la base de la **seule similitude** de leur profil d’expression, **indépendamment** de toute donnée histo/clinique.

### Première preuve de concept — Golub 1999 (Leucémies aiguës)
- 11 LAM + 27 LAL
- Étude de **transcriptome sans a priori**
- Les LAL et LAM s’organisent en **deux clusters distincts** : panel de gènes surexprimés en LAL, autre panel en LAM
- → première démonstration de la capacité du transcriptome à classer des tumeurs

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p15_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p16_00.jpeg]]

### Étude clé — Nature 2000 : sous-groupes des DLBCL
- Lymphomes B diffus à grandes cellules (DLBCL) auparavant **groupés en 1 entité**
- Analyse non supervisée → **2 sous-groupes moléculaires distincts** :
  - **DLBCL de type GC** : profil proche des cellules **B normales du centre germinatif**
  - **DLBCL de type ABC (activated B-cell)** : profil proche des **cellules B activées**

→ Origine de l’**algorithme de Hans** utilisé en IHC par tous les hématopathologistes pour classer **GC vs non-GC**.

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p17_00.jpeg]]



## Approche supervisée (class prediction)

On définit **a priori** 2 groupes (ex : tumeurs métastatiques vs non-métastatiques, tumeur vs normal) et on cherche les gènes **discriminants**.

Permet :
- Identification de **voies de signalisation** impliquées
- Orientation vers une **origine cellulaire**
- Aide au **diagnostic différentiel**

### Exemple — origine TFH des lymphomes T angio-immunoblastiques (AITL)
Comparaison du transcriptome de cellules T tumorales triées d’AITL vs sous-types de cellules T normales :
- Cellules tumorales d’AITL = profil moléculaire très proche des cellules **TFH (T folliculaire helper)**
- Démonstration par l’équipe de Créteil (Philippe Gaulard, Laurence de Leval)

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p20_00.png]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p21_00.png]]

## Application emblématique — Cancer du sein (Pérou, années 2000)

À partir d’une série de cancers du sein localement avancés, **5 sous-types moléculaires** définis :

| Sous-type | Profil | Pronostic |
|-----------|--------|-----------|
| **Luminal A** (RE+) | Cellules épithéliales **luminales** | Bon |
| **Luminal B** (RE+) | Cellules luminales | Intermédiaire |
| **HER2-enriched** (ERBB2+) | Surexpression *ERBB2* | Mauvais (avant trastuzumab) |
| **Basal-like** (RE−) | Cellules épithéliales **basales** | **Mauvais** (métastases précoces) |
| **Normal-like** (RE−) | Profil du tissu mammaire normal | Variable |

→ Les sous-types diffèrent en pronostic : métastases plus fréquentes dans **basal** et **HER2+**.

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p24_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p25_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p26_00.jpeg]]

## Définition d’une signature génique

Les analyses **non supervisées** séparent **rarement d’emblée** les classes pronostiques.

→ On utilise des **analyses supervisées** pour identifier les gènes discriminant 2 classes d’évolution différente.

**Objectif** : définir un **modèle multigénique** prédisant l’appartenance d’un échantillon à une classe = **class prediction**.

### Exemples de signatures dans le cancer du sein

| Signature | Nb de gènes | Indication |
|-----------|-------------|-----------|
| **MammaPrint** | 70 | Risque métastatique |
| **Oncotype DX** | 21 | Récidive sous tamoxifène |
| **PAM50** | **50** | Sous-type intrinsèque + risque récidive |
| **EndoPredict** | 12 | Risque récidive RH+ |

→ Le test choisi dépend du **contexte** : risque métastatique, statut ganglionnaire, traitement hormonal.

→ Permet d’**éviter le sur-traitement** chez certaines patientes.

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p27_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p28_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p29_00.jpeg]]

## PAM50 — exemple détaillé

### Mise au point
- Étude de transcriptome sur **~200 cancers du sein** par puce
- Signature initiale de **1 900 gènes** discriminant les 5 sous-types
- Réduction à **50 gènes** (10 gènes les plus discriminants par catégorie)

### Validation et routine
- Validation sur **cohortes indépendantes**
- Mesure en routine par techniques **bas débit** :
  - **RT-qPCR** TaqMan
  - **Nanostring** : technique d’**hybridation sans amplification**, avec **code-barre coloré**, peut quantifier **jusqu’à 800 gènes** simultanément en comptant des molécules d’ARN

### Résultat clinique
- Score combiné à la **taille tumorale** + statut ganglionnaire
- Donne un **risque** de récidive : **faible / intermédiaire / élevé**
- Aide à la décision : **traitement adjuvant** ou non
- Étude clinique lancée à l’**Institut Curie** ; pratiqué dans plusieurs centres en France

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p29_01.jpeg]]


![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p32_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p32_01.jpeg]]

## Au-delà du sein — autres applications

| Signature | Origine / Application |
|-----------|----------------------|
| **CINSARC** | Initialement **sarcomes** (signature proliférative) — applicable à d’autres cancers |
| Signatures **immune profile** | Réponse immunothérapie |
| Signatures **épigénétiques** | Méthylome (cf [[16_280 Méthylation de l'ADN]]) |

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p33_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p33_02.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p35_00.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p35_01.jpeg]]

## Limites et exigences

| Critère | Microarray | RNA-seq |
|---------|-----------|---------|
| **Qualité ARN** | Très bonne **indispensable** | Très bonne **indispensable** |
| **Quantité ARN** | Importante | Moins importante |
| **Effectifs** | Grands effectifs nécessaires | Idem |
| **Reproductibilité inter-plateformes** | Oui | Oui |
| **Niveau de preuve** | Suffisant pour application clinique | En cours |

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p35_02.jpeg]]

![[assets/pathologie-moleculaire/arn/16-830 Puces à ADN dans létude de lexpression des gènes (transcriptome) Déf dune signature/p35_03.jpeg]]

---

## 🔑 Points clés à retenir

1. **Transcriptome** = ensemble des ARN (souvent réservé aux ARNm) ; ARNm = **2 %** des ARN totaux
2. Techniques haut débit : **microarray** (Affymetrix, Agilent, Illumina) → **RNA-seq** (actuel)
3. Microarray = "**on ne trouve que ce qu’on cherche**" (limité aux sondes présentes)
4. RNA-seq : meilleur sur ARN faiblement exprimés, transcrits alternatifs et SNP, plus coûteux et long
5. Visualisation en **heatmap** : **lignes = sondes**, **colonnes = tumeurs** ; **vert** = bas, **rouge** = haut
6. **Clustering hiérarchique** = approche **non supervisée** (class discovery)
7. **Golub 1999** : première classification (LAM vs LAL) par transcriptome
8. **DLBCL** GC vs ABC (Nature 2000) → **algorithme de Hans** en IHC
9. **5 sous-types moléculaires du cancer du sein** (Pérou) : **Luminal A/B, HER2, Basal, Normal-like**
10. **Signature génique** = modèle multigénique discriminant 2 classes (analyse **supervisée**)
11. **PAM50** : 50 gènes, risque de récidive ; mesure en routine par **RT-qPCR** ou **Nanostring**
12. Validation **prospective** + **cohortes indépendantes** indispensable avant usage clinique
