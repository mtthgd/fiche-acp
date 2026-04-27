---
tags:
  - anatomopathologie
  - ACP
  - neurologie
  - methylome
  - epigenetique
  - DKFZ
  - classifier_Heidelberg
  - MGMT
  - CpG
  - classification_moleculaire
date: 2024
source: DES ACP - Cours de Neurologie
---

# Méthylome en neuropathologie

> Liens : [[40_Classification OMS des tumeurs du SNC]] | [[50_Gliomes de l'adulte]] | [[51_Gliomes pédiatriques]] | [[55_Épendymomes]] | [[60_Tumeurs germinales intracrâniennes]] | [[65_Métastases cérébrales]]

## Généralités — Qu'est-ce que l'épigénétique ?

L'**épigénétique** = ensemble de processus biologiques qui **modifient la lecture des gènes SANS modifier la séquence de l'ADN**.

- Mécanismes : biochimiques (méthylation, acétylation, phosphorylation, ubiquitination), conformationnels, micro-ARN
- Modifications **temporaires ou non**, **transmissibles ou non** entre générations de cellules ou d'individus
- Exemples physiologiques : détermination sexuelle chez la tortue (température), reine vs ouvrière chez l'abeille, différenciation embryonnaire

## La méthylation

**Méthylation** = addition d'un groupement **méthyl (-CH3)** :
1. Sur la **queue des histones** (une des 4 modifications post-traductionnelles avec acétylation, phosphorylation, ubiquitination)
2. Sur l'**ADN** — plus précisément sur le **carbone 5 des cytosines** → **5-méthylcytosine**

### Sites CpG (clé chez les mammifères)

- Chez les mammifères, les cytosines méthylées appartiennent quasi exclusivement à un **dinucléotide CpG** (= cytosine liée par une liaison phosphate à une guanine en 3')
- **NB** : un site CpG = 2 nucléotides sur **un même brin** (à distinguer d'une C et G "à part" sur brins complémentaires)
- Répartition hétérogène : enrichissement dans les **régions promotrices** et les **séquences répétées (LINE, SINE)**

### Impact fonctionnel

| Région | État | Effet |
|--------|------|-------|
| **Promoteur hyperméthylé** | Condensation chromatinienne | **Diminution de la transcription** (empêche l'ARN polymérase) |
| Promoteur hypométhylé | Ouverture | Transcription active |
| Régions répétées LINE/SINE hyperméthylées | Stabilité | ↓ rétrotransposition, ↓ translocations |
| Régions répétées hypométhylées | Instabilité | Risque oncogénique |

L'état de méthylation est **réversible** (enzymes de méthylation / déméthylation).

## Bases historiques du méthylome tumoral

| Année | Avancée |
|-------|---------|
| **2001** (Esteller) | Le profil de méthylation de **12 gènes** permet de discriminer **15 types tumoraux** → naissance de l'idée d'une classification par méthylome |
| **2003** | Le profil de méthylation de 3 gènes suppresseurs (9p21) permet de distinguer les **épendymomes** selon leur compartiment anatomique et l'âge |
| **2018** | "Success story" allemande : classification des tumeurs cérébrales par **classes de méthylation** — application clinique courante |
| **2021** | L'OMS intègre la localisation et l'âge dans la classification des épendymomes |

## Le classifier du DKFZ (Heidelberg)

- **176 classes de méthylation** décrites à ce jour
- Image "planisphère" (t-SNE sur ~3 000 tumeurs) : chaque tumeur = un point, les tumeurs de profil similaire se regroupent en **"pays" = classes de méthylation**
- L'**océan** entre les pays = classes à découvrir (depuis 2018, de nouveaux territoires ont émergé)

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p05_01.jpeg]]

### Trois situations par rapport à l'histologie

| Relation classe de méthylation / diagnostic OMS | Exemple |
|-------------------------------------------------|---------|
| **Superposable** | Épendymome myxopapillaire |
| **Dissociante** (plusieurs classes dans une entité histologique) | **Glioblastome IDH sauvage** → **6 classes** distinctes alors que l'histologie ne reconnaît qu'un type |
| **Seul moyen d'asseoir le diagnostic** | **Neuroblastome avec activation de FOXR2** (défini uniquement par la classe de méthylation) |

## Méthodologie (technique Illumina)

### Étapes du workflow

1. **Extraction d'ADN tumoral** (blocs paraffine) + contrôle qualité
2. **Traitement au bisulfite de sodium** (ADN monocaténaire) :
   - **Cytosines non méthylées → désaminées → uraciles** → remplacées par des thymines dans le brin synthétisé
   - **Cytosines méthylées → protégées → restent cytosines**
3. **Hybridation sur puce Illumina EPIC** (850 000 CpG analysés) → fichiers **IDAT** (format image)
4. **Analyse bioinformatique** sur le pipeline du **DKFZ** (en ligne, accès communautaire) — seule méthode donnant un **score de classe de méthylation**

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p14_01.png]]

### Principe du classifier : forêts d'arbres décisionnels (random forest)

- Sur les 850 000 CpG, **10 000 sélectionnés** pour l'analyse
- **~ 10 000 arbres décisionnels** combinés (random forest)
- Chaque arbre pose des **questions binaires** (ce CpG est-il méthylé ou non ?)
- Propagation à travers l'arbre → aboutit à une **classe de méthylation + score de probabilité**

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p16_01.jpeg]]

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p17_01.png]]

## Output du pipeline DKFZ (en pratique)

Après soumission du fichier IDAT, on obtient :

| Élément | Utilité |
|---------|---------|
| **Classe de méthylation proposée** (V11 + V12.5) | Diagnostic intégré |
| **Score de calibration** (0 à 1) | Probabilité d'appartenance à une classe |
| **CGH déduite** (profil de CNV) | Amplifications/délétions spécifiques (ex : C19MC pour ETMR, gain 1q pour médulloblastome…) |
| **Statut de méthylation MGMT** | Prédictif de réponse au témozolomide |

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p18_01.png]]

### Interprétation du score de calibration

| Score | Interprétation |
|-------|----------------|
| **≥ 0,9** | **Match** — classe de méthylation **certaine** (à valider par histologie + CGH + moléculaire) |
| 0,3 – 0,9 | Incertain — poursuite de l'analyse intégrée |
| < 0,3 | **Non significatif** — non classé |

### Versions du classifier

| Version | Apport |
|---------|--------|
| **V11** | Historique ; CGH + MGMT inclus |
| **V12.5** | Nouvelles classes, **meilleure gestion du tissu sain et de la réaction inflammatoire**, classes repositionnées dans le cadre **OMS** |

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p20_01.jpeg]]

## MGMT (méthylation du promoteur)

- Gène méthylé = **non transcrit** (cf. principes généraux)
- **MGMT méthylé** = activité de réparation de l'ADN bloquée → **bonne réponse au témozolomide** (dont le but est d'induire des altérations de l'ADN)
- Intégré dans les critères thérapeutiques du **glioblastome** (association radio-témozolomide)

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p21_02.jpeg]]

## CGH déduite (copy number variation)

- Profil "plat" le plus souvent
- Amplifications/délétions spécifiques aident à consolider le diagnostic

Exemples classiques :

| CNV | Tumeur |
|-----|--------|
| **Amplification C19MC** (chr 19) | **ETMR** (embryonal tumor with multilayered rosettes) |
| Amplification MYCN | Médulloblastome groupe 3, neuroblastome |
| Perte 1p/19q codélétée | Oligodendrogliome (IDH muté) |
| Chromothripsis | Glioblastome pédiatrique |

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p13_03.png]]

## Indications cliniques du méthylome

**Quand faire appel à une analyse par profil de méthylation ?**

1. **Présomption diagnostique ne reposant QUE sur la classe de méthylation**
   - Ex : neuroblastome à activation **FOXR2**, DGONC, HGNET-BCOR, CNS NB with FOXR2, etc.
2. **Tumeur ne répondant pas aux critères OMS** (histologie atypique, conflit entre marqueurs)
3. **Anticipation de multiples examens de biologie moléculaire** :
   - Le méthylome remplace **une recherche de fusions** + **mutations** + **CNV (CGH)** en un seul examen → économie de matériel, temps, argent
4. **Plateau de biologie moléculaire insuffisant** sur place

## Limites et perspectives

| Limite | Commentaire |
|--------|-------------|
| Cas **inclassés** | Classe non existante dans le classifier (ex : tumeurs très rares comme le leptomeningioma), **ADN de départ de qualité insuffisante**, raisons inconnues |
| **Tumeurs rares non apprises** | Ne se classe que ce qu'il connaît |
| Sensibilité à la contamination par tissu sain / inflammation | Moins critique en V12.5 mais réel |
| Classification considérée comme **expérimentale** par les Allemands | Application clinique routine malgré tout |
| **Extension à d'autres pathologies** | **Sarcomes** (classifier déjà fonctionnel), publications croissantes dans d'autres domaines |

## Place du pathologiste

- Le méthylome = **outil additionnel dans la panoplie du neuropathologiste**
- **Ne remplace pas** l'intégration morphologique et moléculaire : stratégie d'**intégration des données**
- Valide ou réfute une hypothèse histologique
- Les **images restent partielles** : le pathologiste interprète

## Exemple intégré (cas DKFZ)

**Tumeur 21G 033 95** :
- **CGH** : profil plat sauf **amplification du C19MC** + amplification chromosome 2
- **Classe de méthylation** : ETMR (*embryonal tumor with multilayered rosettes*)
- **Concordance CGH – classe de méthylation** → diagnostic consolidé

![[assets/neurologie/tumeurs_snc/2022-10 Methylome/p22_01.png]]

---

## 🔑 Points clés à retenir

1. **Méthylome** = profil de méthylation de l'**ADN sur sites CpG** (5-méthylcytosine) → signature épigénétique tumorale
2. Technique **Illumina EPIC** (850 000 CpG) après traitement au **bisulfite de sodium** + analyse par **random forest (10 000 arbres décisionnels)**
3. Pipeline **DKFZ (Heidelberg)** : accès en ligne, actuellement **176 classes de méthylation**, versions **V11** (CGH + MGMT) et **V12.5** (plus puissante, alignée OMS)
4. **Score de calibration** : **≥ 0,9 = match**, 0,3-0,9 = incertain, < 0,3 = non significatif
5. Trois relations avec l'histologie : **superposable** (ex : épendymome myxopapillaire), **dissociante** (glioblastome IDH-WT = **6 classes**), **seul moyen** (neuroblastome **FOXR2**)
6. Output = **classe de méthylation + CGH déduite + statut MGMT**
7. **MGMT méthylé** = bonne réponse au **témozolomide** (glioblastome)
8. Amplifications spécifiques visibles sur la CGH (ex : **C19MC pour ETMR**, MYCN, 1p/19q)
9. Indications : **diagnostic dépendant de la classe**, tumeurs **hors cadre OMS**, économie de matériel, plateau moléculaire limité
10. **Outil additionnel** — ne remplace pas le pathologiste, s'intègre à la stratégie diagnostique (morphologie + IHC + moléculaire + méthylome)
