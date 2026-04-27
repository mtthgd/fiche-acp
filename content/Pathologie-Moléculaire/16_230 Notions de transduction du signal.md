---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - connaissances_fondamentales
  - transduction_signal
  - récepteurs
  - second_messager
  - GTPase
  - kinase
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Notions de transduction du signal

> Liens : [[16_210 Oncogènes et gènes suppresseurs de tumeurs]] | [[16_220 Cycle cellulaire et cancer]] | [[16_240 Principales voies de signalisation et dérégulation]]

## Objectifs

Acquérir les notions de **communication cellulaire** et de **transduction du signal** : connaître les principaux **ligands**, **récepteurs**, **seconds messagers** et **effecteurs transcriptionnels**.

## Communication cellulaire — généralités

Chaque cellule est programmée pour répondre à des combinaisons spécifiques de molécules extracellulaires (signaux). Selon le contexte, elle reçoit des ordres de :

- **Survie / maintenance**
- **Croissance / division**
- **Différenciation**
- **Migration**
- **Mort cellulaire (apoptose)**

Principe général : **signal → récepteur → cascade de transduction → réponse cellulaire**.



## Types de signaux extracellulaires

### Nature chimique

| Catégorie | Exemples |
|-----------|----------|
| **Protéines** | Facteurs de croissance, cytokines, neurotransmetteurs |
| **Petits peptides** | TRH, vasopressine |
| **Lipides** (dérivés du cholestérol) | Hormones stéroïdes (testostérone, œstradiol), prostaglandines |
| **Petites molécules** | **NO** (monoxyde d’azote) |

### Mode d’action

| Mode | Description |
|------|-------------|
| **Autocrine** | La cellule s’auto-stimule |
| **Paracrine** | Stimulation des cellules voisines |
| **Endocrine** | Stimulation à longue distance (hormones) |
| **Synaptique / neurocrine** | Communication neuronale |
| **Signaux de contact** | Nécessitent un contact cellule-cellule |



## Mécanismes de transmission du signal

### Interactions par domaines spécifiques

| Domaine | Spécificité |
|---------|-------------|
| **SH2** | Phospho**tyrosines** |
| **SH3** | Régions riches en **prolines** |
| **PH (Pleckstrin Homology)** | **Phospholipides membranaires** |

### Modifications post-traductionnelles

- **Phosphorylation** (la plus fréquente)
- **Liaison de nucléotides guanyliques (GTP / GDP)**
- **Farnésylation** (ex. RAS) → ancrage membranaire
- **Hydroxylation**
- **Ubiquitinylation** → dégradation
- **Acétylation**

### Modifications conformationnelles

- Dimérisation
- Changement de conformation
- Ouverture de canaux ioniques



## Commutateurs moléculaires (« switches »)

Deux mécanismes principaux pour passer d’un état **éteint** (inactif) à un état **allumé** (actif) :

### 1. Phosphorylation / déphosphorylation

```
Protéine OFF + ATP → [Kinase] → Protéine-P (ON)
Protéine-P (ON) → [Phosphatase] → Protéine OFF
```

### 2. Liaison de nucléotides guanyliques (GTPases)

```
Protéine-GDP (OFF) → [GEF, échange GDP→GTP] → Protéine-GTP (ON)
Protéine-GTP (ON) → [hydrolyse via GAP] → Protéine-GDP (OFF)
```



## Trois grandes classes de récepteurs

### 1. Récepteurs canaux (ionotropes)

- Conformation **fermée** au repos
- Fixation du ligand → ouverture → entrée/sortie d’**ions** → effet sur protéines cibles
- Exemples : récepteur nicotinique, GABA-A, NMDA



### 2. Récepteurs couplés aux protéines G (RCPG / GPCR)

- 7 domaines transmembranaires
- Couplés à une **protéine G hétérotrimérique** (sous-unités **α, β, γ**)
- Fixation du ligand → relargage du GDP → fixation du GTP sur **Gα** → Gα se détache et active un **effecteur** (enzyme ou canal)
- L’effecteur active ou produit un **second messager** → action sur protéines cibles

#### Sous-types de protéines Gα

| Sous-type | Effet sur l’adénylate cyclase | Second messager |
|-----------|--------------------------------|------------------|
| **Gαs** | **↑** activation | ↑ AMPc |
| **Gαi** | **↓** inhibition | ↓ AMPc |
| **Gαq** | Active **PLCβ** | **IP3 + DAG** |
| **Gα12/13** | RhoGEF | Cytosquelette |

#### Voie AMPc – PKA – CREB

```
Ligand → RCPG → Gαs → adénylate cyclase
   → AMPc → PKA (sous-unités catalytiques se détachent)
   → noyau → phosphorylation de CREB
   → fixation sur séquence CRE → transcription génique
```

Exemple : **TSH → thyroïde → sécrétion de thyroxine** via cette cascade.

#### Voie IP3 / DAG / Ca²⁺

```
Ligand → RCPG (Gαq) → PLCβ
   → PIP2 → IP3 + DAG
   IP3 → récepteur RE → libération de Ca²⁺
   Ca²⁺ + DAG → PKC → phosphorylation de substrats
```







### 3. Récepteurs à activité enzymatique (RTK +++)

#### Structure

| Domaine | Localisation / fonction |
|---------|--------------------------|
| **Extracellulaire** | Site de fixation du ligand + dimérisation |
| **Transmembranaire** | Ancrage |
| **Intracellulaire** | Activité enzymatique (souvent **tyrosine kinase**) |

#### Principe d’activation

1. Fixation du ligand → **dimérisation** du récepteur
2. **Trans-autophosphorylation** des sous-unités sur tyrosines
3. Recrutement de **protéines adaptatrices SH2/SH3**
4. Activation des cascades en aval (**MAPK**, **PI3K-AKT**, JAK-STAT…)

#### Exemples de RTK

- **EGFR / HER2 / HER3 / HER4** (famille ErbB)
- **IGF-1R**
- **PDGFR**
- **VEGFR**
- **FGFR**
- **KIT, FLT3, RET, MET, ALK, ROS1, NTRK1/2/3**

→ Implique survie, croissance, prolifération, invasion en condition tumorale.





## Effets sur la réponse cellulaire

Les voies de transduction modulent in fine :

| Cible | Effet |
|-------|-------|
| Protéines de **transport** | Modification des transports ioniques |
| Enzymes **métaboliques** | Altération du métabolisme |
| **Facteurs de transcription** | Modification de l’expression génique |
| **Cytosquelette** | Forme cellulaire, migration |
| Protéines du **cycle cellulaire** | Croissance, division |

## Complexité et intégration

Les voies de signalisation ne sont pas linéaires :

- **Amplifications** d’un signal (cascade enzymatique)
- **Intégrations** multiples (cross-talk entre voies)
- **Voies parallèles** activées par un même signal
- **Modulations** par protéines d’ancrage (scaffolds), inhibiteurs
- **Modulation transcriptionnelle** finement régulée







## Implications en pathologie

La communication cellulaire est :
- **Très régulée** en physiologie
- **Dérégulée** en pathologie : **cancers** (cf. [[16_240 Principales voies de signalisation et dérégulation]]), maladies neurodégénératives, diabète, maladies métaboliques


---

## 🔑 Points clés à retenir

1. **Communication cellulaire** : signal → récepteur → transduction → réponse (survie, prolifération, différenciation, migration, mort)
2. **Modes de signalisation** : autocrine, paracrine, endocrine, synaptique, contact
3. **Commutateurs moléculaires** : phosphorylation (kinase / phosphatase) et liaison nucléotidique (**GTPases** : GEF active, GAP inactive)
4. Domaines d’interaction : **SH2** (phosphotyrosines), **SH3** (prolines), **PH** (phospholipides)
5. **3 classes de récepteurs** : canaux ioniques, RCPG (7-TM), récepteurs à activité enzymatique (RTK +++)
6. **RCPG / Gαs → adénylate cyclase → AMPc → PKA → CREB** (ex. TSH/thyroxine)
7. **RCPG / Gαq → PLCβ → IP3 + DAG → Ca²⁺ + PKC**
8. **RTK** : dimérisation → autophosphorylation tyrosine → recrutement adaptateurs SH2/SH3 → MAPK et PI3K-AKT
9. Exemples cliniques de RTK : **EGFR, HER2, KIT, ALK, ROS1, NTRK, FGFR, MET, RET**
10. Les voies sont intégrées (cross-talk, amplification, voies parallèles) — leur dérégulation est centrale dans le cancer
