---
tags:
  - anatomopathologie
  - ACP
  - gyneco_sein
  - biologie_moleculaire
  - HPV
  - col_uterin
  - endometre
  - ovaire
  - TCGA
  - POLE
  - MMR
  - MSI
  - p53
  - BRCA
  - inhibiteurs_PARP
  - immunotherapie
date: 2024
source: DES ACP - Cours de gynéco-pathologie
---

# Classifications moléculaires des cancers gynécologiques

> Liens : [[03_Cancers_gynecologiques_familiaux]] | [[04_Macroscopie_prise_en_charge_des_pieces_operatoires_et_des_biopsies_du_col]] | [[05_macroscopie_ovaire_et_trompe1]] | [[02_trompe_tumoral]] | [[01_PERITOINE_gyneco_jcs]]

## Plan

1. HPV et col utérin
2. Adénocarcinome endométrial — classification TCGA
3. Carcinomes ovariens (types I/II et 5 sous-types)
4. Tumeurs des cordons sexuels et stroma

---

# 1. HPV et carcinogenèse cervicale

## Généralités

- Carcinome **épidermoïde** du col **quasi toujours HPV-induit**
- Carcinogenèse **multi-étape** sur **10-15 ans**
- **Raccourcie à 4-5 ans** en cas d’immunodépression (VIH+, transplantation)

## Étapes

| Étape | ADN viral | Histologie |
|-------|-----------|------------|
| Infection initiale | **Épisomal** | Cellules basales infectées |
| Lésion bas grade (LSIL/CIN1) | Épisomal prédominant | Régression dans **80 %** |
| Haut grade (HSIL/CIN2-3) | Intégration progressive | Expansion en hauteur, ↓ virions |
| Carcinome invasif | **Intégré complet** | Pas de production de virion |


## Mécanisme oncogénique : protéines E6 et E7

- Protéines virales **E6 et E7** = clés du phénotype prolifératif
- Lèvent le **double verrou P53-RB**
- **E7** → libère **E2F** → entrée en phase S
- **E6** → dégrade **P53** → bloque l’apoptose

| Protéine virale | Cible | Effet |
|-----------------|-------|-------|
| **E6** | **P53** | Dégradation → pas d’apoptose |
| **E7** | **RB** | Libération E2F → cycle cellulaire |

→ Levée du double verrou → **carcinogenèse**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/gyneco-sein/cours_transversaux/04_11_05%20gyneco%20molec%20DES%20FPL/p05_00.png)


## Conséquences thérapeutiques

| Voie/marqueur | Activation | Cible thérapeutique potentielle |
|---------------|-----------|-------------------------------|
| **PI3K-AKT-mTOR** | 60 % carcinomes épidermoïdes, 74 % ADK | Inhibiteurs mTOR |
| **TGF-β** suppressive de tumeurs | 41 % épidermoïdes, 26 % ADK | — |
| **VEGF** (via E7) | Activé | **Anti-angiogéniques** |
| **PD-L1** / immunothérapie | Tumeurs très immunogènes | **Immunothérapie** |

> **PD-L1 et charge mutationnelle ne sont PAS contributifs** dans le cancer du col → c’est l’immunogénicité virale qui prime.

## Cancers du col **NON HPV**
- Activation préférentielle des voies **Wnt-β-caténine** et **Sonic Hedgehog**
- Cibles thérapeutiques en recherche

## Vaccination
- Vaccination des jeunes filles (et idéalement des jeunes garçons porteurs)
- Stratégie clé d’**éradication primaire**


---

# 2. Adénocarcinome endométrial

## Classification clinico-pathologique historique (Bokhman)

| | Type I | Type II |
|---|--------|---------|
| Fréquence | **80 %** | 20 % |
| Âge | 50-60 ans | Post-ménopause |
| Hormono-dépendance | **Oui** (hyper-œstrogénie) | **Non** |
| Précurseur | **Hyperplasie atypique** | Carcinome endométrial intra-épithélial |
| Histologie | **Endométrioïde**, mucineux | **Séreux**, à cellules claires, mixtes mülleriens, **endométrioïde grade 3** |
| Survie 5 ans | **80 %** | 40 % |
| **PTEN, β-caténine** | Mutés | Non |
| **TP53** | **Wild-type** | **Muté (>90 %)** |
| MSI | 30 % | Non |

## Classification moléculaire TCGA (4 sous-types)

| Sous-type | Fréquence | Mutations | Pronostic (survie 5 ans sans maladie) |
|-----------|-----------|-----------|--------------------------------------|
| **POLE ultra-mutated** | ~ 8 % | **POLE muté** (hyper-mutation), tous grades, mutations PI3K, KRAS, parfois P53 | **Excellent (~93 %)** |
| **MSI / hyper-muté** | ~ 30 % | **MMR déficient** (MSI), tous grades, **P53 wt**, altérations PIK3CA, KRAS | **Excellent (~95 %)** |
| **MSS / Copy Number Low (groupe 3)** | Majoritaire | Endométrioïde grade 1-2, **P53 wt**, **MSS** | Intermédiaire (~52 %) |
| **Copy Number High / serous-like (type II)** | ~ 24 % | **P53 muté > 90 %**, séreux, cellules claires, endométrioïde haut grade | **Mauvais (~42 %)** |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/gyneco-sein/cours_transversaux/04_11_05%20gyneco%20molec%20DES%20FPL/p10_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/gyneco-sein/cours_transversaux/04_11_05%20gyneco%20molec%20DES%20FPL/p11_00.png)

## Algorithme de phénotypage en pratique

```
ADK endomètre
    │
    ├─ Séquençage POLE → si muté = groupe POLE (excellent pronostic)
    │
    ├─ IHC MMR (4 prot : MLH1, PMS2, MSH2, MSH6)
    │      ├─ Perte d’expression → groupe MSI (excellent pronostic)
    │      └─ Expression normale → IHC P53
    │              ├─ P53 muté → groupe Copy Number High (mauvais pronostic)
    │              └─ P53 wt → groupe MSS / Copy Number Low (intermédiaire)
```

## Implications thérapeutiques

| Groupe TCGA | Stratégie thérapeutique |
|-------------|-------------------------|
| **POLE muté** | **Immunothérapie** (tumeur "chaude") |
| **MSI** | **Immunothérapie** + inhibiteurs **PARP** |
| **P53 muté (CN-high)** | **Sels de platine** + **inhibiteurs PARP** |
| **MSS / CN-low (gr. 3)** | **Hormonothérapie** ± autre |



## Dépistage du syndrome de Lynch

- **Dépistage systématique avant 60 ans** par recherche d’**instabilité microsatellitaire** (IHC MMR ± biologie moléculaire de confirmation)

---

# 3. Carcinomes ovariens

## Classification dichotomique type I / type II

| | Type I | Type II |
|---|--------|---------|
| Fréquence | Minoritaire | **Majoritaire** |
| Évolution | Lente, **stade I** | Rapide, **stade avancé au diagnostic** |
| Stabilité génétique | Stable | **Instabilité chromosomique** |
| Mutations | **BRAF, KRAS, PTEN, β-caténine** | **TP53**, BRCA |
| Précurseurs | **Endométriose, tumeurs borderline** | Théoriquement aucun (en réalité **STIC**) |
| Histologies | Endométrioïde, séreux **bas grade**, mucineux primitif, cellules claires | Séreux **haut grade**, indifférenciés, mixtes mülleriens (carcinosarcomes) |

## 5 sous-types de carcinomes ovariens

| Type | Fréquence | Précurseur | Anomalies moléculaires | Sensibilité chimio | Pronostic |
|------|-----------|-----------|------------------------|-------------------|-----------|
| **Séreux haut grade** | Très fréquent | **STIC** (trompe) | **TP53**, **BRCA1/2** | Très élevée | Variable (PARP) |
| **Séreux bas grade** | Rare | Borderline séreux | **BRAF, KRAS** | — | Intermédiaire |
| **Mucineux primitif** | Rare | Borderline mucineux | **KRAS, HER2** | **Mauvaise** | Variable |
| **Endométrioïde** | Modéré | **Endométriose** ; **Lynch** | **PTEN, ARID1A** | Élevée | Variable |
| **Cellules claires** | Modéré | **Endométriose** | **HNF1β, ARID1A, PIK3CA** | **Mauvaise** | Mauvais |



![](https://pub-09a67500e45345d4babec28739403570.r2.dev/gyneco-sein/cours_transversaux/04_11_05%20gyneco%20molec%20DES%20FPL/p19_00.jpeg)

## Théorie tubaire (Crum)

- **60 %** des carcinomes séreux de haut grade sont d’**origine tubaire** via les **STIC**
- Cellules tumorales du STIC migrent du pavillon → s’implantent à la surface ovarienne
- Origine ovarienne primitive : voies endosalpingiose / endométriose / borderline pour les autres types

## Statut BRCA somatique sur cancer ovarien

- Demandé par les cliniciens sur **toutes les tumeurs ovariennes de haut grade**
- Permet l’utilisation des **inhibiteurs de PARP**
- Critères pré-analytiques :
  - Fixation **rapide** sur **pièce ouverte** (pénétration formol)
  - Prélèvements **très cellulaires**, **pas de nécrose**
- Si pièce opératoire : possible
- Si biopsies péritonéales : **minimum 6 biopsies** (faire attention à l’**électrocoagulation** : usage en deuxième temps)



## Cibles thérapeutiques par sous-type

| Type | Cibles thérapeutiques |
|------|----------------------|
| Séreux haut grade BRCA-muté | **Inhibiteurs PARP**, sels de platine |
| Séreux bas grade | Inhibiteurs **MEK** (BRAF/RAS) |
| Mucineux | **HER2** (si amplifié), KRAS |
| Cellules claires | **PI3K, ARID1A**, parfois MSI → immunothérapie |
| Endométrioïde | **PI3K, ARID1A**, MSI (Lynch) → immunothérapie |

---

# 4. Tumeurs des cordons sexuels et stroma

## 3 entités principales avec apport moléculaire

| Tumeur | Mutation diagnostique | Contexte clinique |
|--------|----------------------|-------------------|
| **Tumeur de la granulosa adulte** | **FOXL2 C402G** | Femme âge moyen / post-ménopause, hyper-œstrogénie |
| **Tumeur de la granulosa juvénile** | **AKT1**, **trisomie 12** | Enfant, femme jeune, hyper-œstrogénie |
| **Sertoli-Leydig** | **DICER1** | Femme jeune, hyper-androgénie |

## SCCOHT (carcinome à petites cellules avec hypercalcémie)

- Anciennement *small cell carcinoma of the ovary, hypercalcemic type*
- **Anomalies de SMARCA4** (voie SWI/SNF) → famille des **tumeurs rhabdoïdes malignes**
- IHC : **BRG1 NÉGATIF** ++ (BRG1 normalement positif dans toutes les autres tumeurs ovariennes et lymphocytes)
- Possible **SALL4** focal nucléaire+
- Témoins indispensables car on attend une **négativité** (artefact possible)


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/gyneco-sein/cours_transversaux/04_11_05%20gyneco%20molec%20DES%20FPL/p26_00.jpeg)

---

## Synthèse — rôle du pathologiste

| Étape | Rôle |
|-------|------|
| **Pré-analytique** | Fixation rapide, ouverture des kystes, conservation de matériel cellulaire pour BMol |
| **Analyse HES** | Diagnostic morphologique, évaluation de la cellularité tumorale |
| **IHC** | Confirmer tumeur primitive, éliminer métastase, MMR systématique sur endomètre |
| **BMol** | Théragnostique : **BRCA somatique** (haut grade ovarien), POLE, FOXL2, DICER1 |
| **Conseil thérapeutique** | Adapter la stratégie : PARP, immuno, sels de platine, hormonothérapie |


---

## 🔑 Points clés à retenir

1. **HPV** : carcinogenèse cervicale via **E6 (P53)** et **E7 (RB)** = levée du double verrou
2. PD-L1 et charge mutationnelle **non contributifs** dans le cancer du col → c’est l’immunogénicité virale qui prime
3. **TCGA endomètre** = 4 sous-types : **POLE** (excellent), **MSI** (excellent), **CN-low/MSS** (intermédiaire), **CN-high/P53-muté** (mauvais)
4. **Algorithme pratique** : POLE → IHC MMR → P53
5. Dépistage **Lynch < 60 ans** systématique sur cancer endomètre par IHC MMR
6. Carcinomes ovariens type I (KRAS/BRAF/PTEN, stade I) vs type II (**TP53/BRCA**, stade avancé)
7. **5 sous-types ovariens** : séreux HG (STIC), séreux BG (BRAF/KRAS), mucineux (KRAS/HER2), endométrioïde (PTEN/ARID1A), cellules claires (HNF1β/ARID1A)
8. **BRCA somatique** systématique sur tumeurs ovariennes haut grade → **inhibiteurs PARP**
9. Tumeurs cordons sexuels : **FOXL2** (granulosa adulte), **DICER1** (Sertoli-Leydig), AKT1+trisomie 12 (granulosa juvénile)
10. **SCCOHT** = **BRG1−**, anomalies **SMARCA4**, famille des tumeurs rhabdoïdes
