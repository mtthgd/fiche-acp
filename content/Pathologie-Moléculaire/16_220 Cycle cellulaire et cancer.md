---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - connaissances_fondamentales
  - cycle_cellulaire
  - CDK
  - cyclines
  - p16
  - RB
  - palbociclib
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Cycle cellulaire et cancer

> Liens : [[16_210 Oncogènes et gènes suppresseurs de tumeurs]] | [[16_230 Notions de transduction du signal]] | [[16_240 Principales voies de signalisation et dérégulation]] | [[16_260 Réparation des lésions de l'ADN]] | [[16_270 Instabilité génétique]]

## Généralités

En à peine 30 ans, on est passé de la découverte des régulateurs du cycle cellulaire dans des organismes modèles (levures, invertébrés marins) à l’introduction en clinique du premier inhibiteur des CDK : le **palbociclib**.

### Phases du cycle

- **G1** : croissance, préparation à la synthèse d’ADN
- **S** : synthèse d’ADN (réplication)
- **G2** : préparation à la mitose
- **M (mitose)** : division
- **G0** : quiescence

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p01_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p02_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p03_00.jpeg]]

## Historique — découverte des régulateurs

| Modèle | Approche | Découverte |
|--------|----------|------------|
| **Levures** (Hartwell, Nurse) | Mutants conditionnels | **CDC2** (chef d’orchestre du cycle), **CDC25** (activateur), **WEE1** (inhibiteur) |
| **Invertébrés marins** (palourde, étoile de mer) (Hunt) | Fusion / micro-injection cellulaire | **MPF** (M-phase Promoting Factor), **cycline B** (variation cyclique d’abondance) |

À la fin des années 80 : synthèse — CDC2 identifié chez tous les eucaryotes, MPF = **complexe CDC2-cycline B**.

→ Prix Nobel 2001 (Hartwell, Hunt, Nurse).

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p05_00.png]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p06_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p07_00.jpeg]]

## CDK et cyclines

### Les CDK (kinases dépendantes des cyclines)

- Famille de kinases (CDK1 à CDK13+) identifiées par PCR puis par séquençage du génome
- Leur activité est **dépendante de l’association à une cycline**
- Comme toute kinase : transfert d’un phosphate (depuis l’ATP) sur un substrat
- Le changement conformationnel à l’association libère le site catalytique pour l’ATP

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p08_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p09_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p10_00.jpeg]]

### Les cyclines

- Famille d’au moins **25 membres** ; les plus connues : **A, B, D, E**
- Caractéristique majeure : leur **abondance est régulée** au cours du cycle
- Régulation par **ubiquitinylation → dégradation par le protéasome** (APC/C, SCF)

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p11_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p12_00.jpeg]]

### Complexes cycline / CDK et étapes du cycle

| Phase | Complexe | Substrat majeur |
|-------|----------|------------------|
| **G1 (avant point R)** | **CDK4-Cycline D** et **CDK6-Cycline D** | **RB** (phosphorylation) |
| **G1 / S (après point R)** | **CDK2-Cycline E** | RB (hyperphosphorylation) |
| **Phase S** | **CDK2-Cycline A** | Substrats de la réplication |
| **G2 / M (mitose)** | **CDK1-Cycline A** puis **CDK1-Cycline B** | Lamines (désassemblage de l’enveloppe nucléaire), histones, … |

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p13_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p14_00.png]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p15_00.jpeg]]

## Régulation des complexes Cycline-CDK

Trois mécanismes principaux :

| Mécanisme | Description |
|-----------|-------------|
| **Dégradation des cyclines** | Ubiquitinylation → protéasome ; perte de la sous-unité régulatrice |
| **Phosphorylation / déphosphorylation** | Activatrice par **CDC25** (phosphatase) ; inhibitrice par **WEE1** (kinase) |
| **CKI** (CDK Inhibitors) | Petites protéines qui se fixent et dissocient les complexes Cycline-CDK ; familles **INK4** (p16, p15, p18, p19) et **Cip/Kip** (**p21, p27**, p57) |


![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p17_00.jpeg]]

## Points de contrôle (« checkpoints »)

Stations « **stop** » qui assurent la **légitimité de la progression**, évitent l’accumulation de dommages et préservent la **stabilité du génome**.

### Point R (point de restriction) en G1

- Intégration des signaux activateurs / inhibiteurs
- Synthèse de **Cycline D** → complexe **CDK4/6-Cycline D** → phosphorylation initiale de **RB**
- Renforcée par **CDK2-Cycline E** → progression vers la phase S
- **Perte de fonction de RB** = abolition du point R → progression non régulée

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p18_00.jpeg]]


### Réponse aux dommages de l’ADN (DDR)

```
Dommage ADN
   ↓
ATM / ATR
   ↓
CHK1 / CHK2
   ↓
p53 (phosphorylée → stable, accumulée)
   ↓
- p21 (CKI) → blocage Cycline-CDK → arrêt G1/S
- gènes de réparation
- gènes pro-apoptotiques (BAX, PUMA…)
```

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p20_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p21_00.jpeg]]

## Altérations en cancérologie

Schématiquement :

| Type d’altération | Conséquence |
|-------------------|--------------|
| **Suppression des freins** (perte de gènes suppresseurs) | Dérégulation de la prolifération |
| **Suractivation des accélérateurs** (proto-oncogène → oncogène) | Dérégulation de la prolifération |

La **majorité** des altérations touche des régulateurs de la **phase G1**.

### Anomalies fréquentes en oncologie

| Acteur | Type d’altération | Tumeurs |
|--------|--------------------|---------|
| **Cycline D1** (CCND1) | **Surexpression**, t(11;14) IGH-CCND1 | **Lymphome du manteau**, sein, ORL |
| **CDK4** | Amplification | Sarcomes, glioblastomes |
| **CDK6** | Surexpression | Lymphomes |
| **CDKN2A (p16)** | Mutation, **délétion**, **méthylation** | Très nombreux cancers (mélanome, GBM, MPM…) |
| **RB1** | Mutation/délétion | **Rétinoblastome**, ostéosarcome, sein, CBPC |
| **TP53** | Mutation | Très nombreux cancers (~50 % des tumeurs) |
| **MDM2** | Amplification (chromosomes double-minute) | Liposarcome dédifférencié, ostéosarcome |

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p22_00.png]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p23_00.jpeg]]

### Exemple de p16 (CDKN2A) — un CKI clé

- Rôle normal : sa surexpression dissocie le complexe **CDK4-Cycline D** → arrêt en G1
- Inactivation par **mutation, délétion, méthylation du promoteur**
- Une forme mutée (ex. glioblastome) est incapable d’arrêter le cycle (perte de fonction démontrée par transfection)

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p24_00.jpeg]]

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p25_00.jpeg]]

## Ciblage thérapeutique : les inhibiteurs de CDK4/6

### Palbociclib

- Petite molécule **inhibitrice compétitive de l’ATP** au niveau du site catalytique
- **Sélectif** pour **CDK4 et CDK6**
- Effet : arrêt du cycle en **G1** (cytométrie en flux : pic unique de contenu en ADN), perte de phosphorylation de **RB**, perte du marqueur **Ki-67** sur les xénogreffes
- Suppression de la croissance tumorale en modèles précliniques (cancer du sein)

![[assets/pathologie-moleculaire/connaissances-fondamentales/16-220 Cycle cellulaire et Cancer/p26_00.jpeg]]


### Indications cliniques

- **2016** : agrément du palbociclib dans le **cancer du sein métastatique RH+/HER2−** :
  - en association avec **létrozole** (étude **PALOMA**)
  - en association avec **fulvestrant** (étude PALOMA-3)
- Successeurs : **abémaciclib**, **ribociclib**

| Inhibiteur CDK4/6 | Études phares |
|-------------------|----------------|
| **Palbociclib** | PALOMA-1, PALOMA-3 |
| **Ribociclib** | MONALEESA |
| **Abémaciclib** | MONARCH |

## Synthèse

Le cycle cellulaire est régulé par :
1. Des **complexes Cycline-CDK** spécifiques de chaque phase
2. Trois mécanismes de régulation : **dégradation, (dé)phosphorylation, CKI**
3. Des **points de contrôle** (R, DDR G1/S, intra-S, G2/M, fuseau mitotique)

Sa **dérégulation** est centrale dans la cancérogénèse, et son **ciblage** (anti-CDK4/6) est devenu une réalité clinique.

---

## 🔑 Points clés à retenir

1. **CDC2 / MPF / Cycline B** = découvertes fondatrices (levures + invertébrés marins, Nobel 2001)
2. Les **CDK** sont actives uniquement complexées à une **cycline** (sous-unité régulatrice)
3. Phase G1 → **CDK4/6-Cycline D** ; G1/S → **CDK2-Cycline E** ; S → CDK2-Cycline A ; G2/M → **CDK1-Cycline B**
4. Régulation : dégradation des cyclines, phosphorylation (**CDC25**, **WEE1**), **CKI** (INK4 : **p16** ; Cip/Kip : **p21, p27**)
5. **Point R** en G1 dépend de la phosphorylation de **RB** par CDK4/6-Cycline D
6. **Réponse aux dommages ADN** : ATM/ATR → CHK1/2 → **p53** → **p21** → arrêt G1/S
7. La **majorité** des altérations en cancérologie touche les **régulateurs de la phase G1**
8. **CDKN2A (p16)** : inactivé par **mutation, délétion ou méthylation** dans de nombreux cancers
9. **CCND1 (cycline D1)** : surexprimée par **t(11;14)** dans le **lymphome du manteau** ; **MDM2** amplifié dans les liposarcomes
10. **Palbociclib** = inhibiteur sélectif **CDK4/6**, cancer du sein **RH+/HER2−** métastatique (avec létrozole ou fulvestrant)
11. Successeurs : **abémaciclib, ribociclib**
12. La perte de **RB** rend les inhibiteurs CDK4/6 inefficaces (RB nécessaire à leur action)
