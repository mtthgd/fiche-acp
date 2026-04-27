---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - TMB
  - charge_mutationnelle
  - immunothérapie
  - néoantigènes
  - exome
  - panel
  - MSI
  - PDL1
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Évaluation de la charge mutationnelle (TMB)

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_520 Séquençage 2G - capture et amplicons]] | [[16_535 Le pipeline bioinformatique]] | [[16_1035 Statut MSI en onco-immunologie]] | [[16_1020 Immunothérapie - principes]] | [[16_1025 PDL1 et immunothérapie]]

## Principe général — définition

La **charge mutationnelle tumorale** (**TMB** = **Tumor Mutational Burden**) est définie comme :

> Le **nombre de mutations non synonymes** présentes dans la **région codante** du génome tumoral (**exome**).

Elle inclut :
- les **SNV** (single nucleotide variants) **non synonymes**
- les **insertions / délétions** (indels)

Elle exclut :
- les **polymorphismes connus** (filtrage via **gnomAD, 1000G, ExAC**)
- les mutations **synonymes**

**Unité** : **nombre total de mutations** (sur exome entier) ou **mutations / mégabase (mut/Mb)** lorsqu’on utilise un panel ciblé.

> **Pas de standardisation** à ce jour : faut-il inclure les mutations **driver / oncogènes** ? Question encore débattue.

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p01_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p01_01.jpeg]]


## Rationnel — TMB et immunothérapie

### Données pivots

| Année | Publication | Cancer | Immunothérapie | Résultat |
|---|---|---|---|---|
| **2014** | NEJM, Snyder et al. | **Mélanome** | **Ipilimumab** (anti-CTLA-4) | TMB **>100 mutations/exome** = survie **significativement augmentée** |
| **2015** | Science, Rizvi et al. | **CBNPC** | **Pembrolizumab** (anti-PD-1) | TMB **>200 mutations/exome** = **PFS augmentée** |

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p03_00.png]]

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p03_01.png]]

### Mécanisme — TMB et néo-antigènes

L’ADN muté → ARN muté → **peptides mutés** → **présentés via le CMH** comme **néo-antigènes** → reconnus par les **lymphocytes T CD4+ et CD8+** → **réponse immune anti-tumorale**.

> La TMB est un **reflet (au moins partiel)** de la **néo-antigénicité tumorale**, qui sous-tend la réponse à l’immunothérapie.


![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p04_01.jpeg]]

## Méthodes d’évaluation

### 1. Whole Exome Sequencing (WES) — gold standard
- Séquençage de l’**ensemble des régions codantes** de la tumeur
- Rendu : **nombre total de mutations** par exome
- **Coûteux**, **délai long**, peu adapté à la routine clinique

### 2. RNA-seq
- Mesure des **transcrits mutés**
- Avantage : confirme la **transcription** effective → renforce la probabilité de **traduction en néo-antigène**
- Saute l’étape de la transcription

### 3. Panel ciblé de gènes — **standard pratique**
- Panels de **plusieurs centaines de gènes** couvrant 1-2 Mb
- Rendu : **mut/Mb**

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p05_00.png]]

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p06_00.jpeg]]

### Taille optimale du panel ciblé

| Étude | Année | Conclusion |
|---|---|---|
| Garofalo et al. | 2016 | Comparaison panels 15 / 48 / **300 gènes** → **300 gènes** plus fidèle |
| 2019 (publication ultérieure) | 2019 | Taille optimale = **panel couvrant 1,5 à 3 Mb** pour bien corréler à l’exome |

> **Petits panels (< 1 Mb)** : variabilité trop importante, faible reproductibilité.

## Panels commerciaux disponibles

| Panel | Société | # gènes | Taille (Mb) |
|---|---|---|---|
| **Foundation One** | Foundation Medicine | 324 | ~0,8 |
| **MSK-IMPACT** | Memorial Sloan Kettering | **468** | ~1,2 |
| **TruSight Oncology 500 (TSO500)** | **Illumina** | **523** | **1,94** |
| **Oncomine Tumor Mutation Load** | **Thermo Fisher (Ion Torrent)** | 409 | **1,65** |

> En pratique en France : envoi à un service externe (**Foundation One**), ou utilisation au laboratoire de **TSO500** ou **Oncomine TML** sur séquenceur dédié de grande capacité.

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p07_00.png]]


![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p07_02.png]]

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p07_03.png]]

### 4. Analyse des épitopes néo-antigéniques
Algorithmes prédictifs à partir des mutations + typage HLA → **peu faisable en routine**, plutôt en recherche.

## Variabilité de la TMB selon le type tumoral

Publication de **Nature 2013** : variabilité énorme entre tumeurs (de quelques mutations à **>1000**).

| Tumeurs **fortement mutées** | Tumeurs **faiblement mutées** |
|---|---|
| **Mélanome** (UV) | Tumeurs **pédiatriques** |
| **CBNPC** (tabac) | Tumeurs de bas grade |
| Carcinomes urothéliaux | Hémopathies indolentes |
| MMRD / dMMR (côlon, endomètre) | Sarcomes |

→ **Cause** : tumeurs épithéliales associées à un **dommage de l’ADN par facteurs environnementaux** (UV, tabac, déficit MMR) sont les plus mutées.

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p08_00.png]]

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p09_00.jpeg]]

## Seuils de TMB

**Aucun seuil fixe consensuel** — varie selon :
- le **type tumoral**
- la **méthode de calcul**
- la **drogue** d’immunothérapie

### Seuils proposés (publication 2015 — formation de néo-antigènes)
| Charge | Néo-antigènes |
|---|---|
| **>10 mut/Mb** | **Fréquente** (TMB-high) |
| 1-10 mut/Mb | Régulière |
| <1 mut/Mb | Occasionnelle |

### Publication NEJM 2017 — taux de réponse à l’immunothérapie
Médiane mut/Mb codantes vs taux de réponse objective (ORR) :
- **MMRD colorectaux**, **mélanomes** → fortement mutés et fortement répondeurs
- Tumeurs intermédiaires → réponse hétérogène

![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p10_00.png]]

## TMB combinée à d’autres biomarqueurs

### TMB et **PD-L1** — facteurs **indépendants**
Publication Cancer Cell 2018 (CBNPC traités par **nivolumab** + **ipilimumab**) :
- Patients répondeurs avec **TMB élevée** mais **PDL1 modeste**
- Patients répondeurs avec **PDL1 élevée** mais **TMB modeste**
- → Les deux marqueurs sont **complémentaires**, **non corrélés**

### TMB et **MSI** ([[16_1035 Statut MSI en onco-immunologie]])
Publication Genome Medicine 2017 :
- **97 % des tumeurs MSI** ont une **TMB > 10 mut/Mb**
- Mais **seulement 16 %** des **TMB-high** sont **MSI**
- Coexistence **dépendante du type tumoral** : fréquente dans **adénocarcinomes gastriques, duodénaux, intestin grêle** ; rare dans mélanome, CE, poumon


![[assets/pathologie-moleculaire/ngs/16-560 Evaluation de la charge mutationnelle/p12_00.jpeg]]

## Considérations techniques pratiques

| Élément | Recommandation |
|---|---|
| % cellules tumorales | **≥ 20-30 %** sur la lame H&E avant extraction |
| Quantité ADN | Selon kit (50-100 ng pour TSO500) |
| Type d’ADN | **FFPE acceptable** (artefacts de désamination filtrés bioinformatiquement) |
| **Profondeur** | **>500×** sur les régions du panel |
| Pipeline ([[16_535 Le pipeline bioinformatique]]) | Filtrage strict des **polymorphismes**, **artefacts FFPE** (C>T), **mutations driver** selon convention |
| Séquenceur | Plate-forme à grande capacité (**NovaSeq**, **Ion S5 XL**) |

## Avantages / Limites

| Avantages | Limites |
|---|---|
| **Biomarqueur prédictif** d’immunothérapie validé | **Pas de standardisation** des méthodes/seuils |
| Facile à calculer à partir d’un panel large existant | Dépendant du **type tumoral** |
| Combinable avec **PDL1** et **MSI** (indépendants) | **Faux positifs FFPE** (artefacts désamination C>T) |
| Reflet de la **néo-antigénicité tumorale** | Coût et infrastructure (séquenceur grande capacité, bioinformatique) |
| Pourra remplacer / compléter les indications PDL1 | Petits panels (<1 Mb) peu fiables |

---

## 🔑 Points clés à retenir

1. **TMB** = nombre de **mutations non synonymes** dans l’**exome tumoral** (SNV + indels), polymorphismes exclus.
2. Unité : **mutations totales/exome** (WES) ou **mut/Mb** (panel ciblé).
3. Rationnel : la TMB reflète la **néo-antigénicité** → meilleure **réponse à l’immunothérapie**.
4. Données pivots : **mélanome / ipilimumab (NEJM 2014)**, **CBNPC / pembrolizumab (Science 2015)**.
5. Gold standard : **WES**. En routine : **panel ≥ 1,5-3 Mb** (Foundation One, **TSO500**, **Oncomine TML**).
6. Les **petits panels (<1 Mb)** sont **trop variables** pour estimer fidèlement la TMB.
7. Seuil indicatif : **>10 mut/Mb** = **TMB-high** (formation fréquente de néo-antigènes).
8. Variabilité +++ selon le type tumoral : mélanome (UV), CBNPC (tabac), MMRD = forts ; pédiatriques = faibles.
9. **TMB et PDL1** sont des facteurs **indépendants** ; **97 % MSI sont TMB-high** mais l’inverse est faux (16 %).
10. Pas de **seuil fixe consensuel** — dépend du type tumoral, de la méthode et de la drogue.
