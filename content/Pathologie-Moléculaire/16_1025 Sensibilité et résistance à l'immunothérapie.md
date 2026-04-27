---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - onco_immunologie
  - PD-1
  - PD-L1
  - CTLA-4
  - checkpoint
  - ICI
  - hot_cold_tumor
  - résistance_primaire
  - résistance_acquise
  - B2M
  - JAK1
  - JAK2
  - HLA
  - TMB
  - MSI
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Sensibilité et résistance à l’immunothérapie

> Liens : [[16_1010 Immunité - Bases de l'onco-immunologie]] | [[16_1015 Cycle de l'immunité anti-tumorale]] | [[16_1020 Rationnel de l'immunothérapie]] | [[16_1035 Statut MSI en onco-immunologie]] | [[16_560 Évaluation de la charge mutationnelle (TMB)]] | [[16_940 IHC multiplex]]

## Principe / Bases immunologiques

La sensibilité à l’immunothérapie dépend de la capacité du système immunitaire à monter une **réponse anti-tumorale efficace** lorsqu’on lève l’inhibition par les **inhibiteurs de checkpoint (ICI)**.

Quatre exigences pour une cytotoxicité efficace :
1. **Reconnaissance** de l’antigène par les LT (TCR ↔ peptide-CMH de la CPA) → activation
2. **Migration** et **infiltration** intra-tumorale
3. **Reconnaissance** de l’antigène présenté par le **CMH des cellules tumorales**
4. **Lyse** : voie mitochondriale (perforine/granzymes) ou voie des récepteurs de mort (Fas-L/Fas)

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p01_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p01_01.jpeg]]

## Rappel — modulation par les checkpoints

L’activation des LT résulte de **3 signaux** :
- **Signal 1** : TCR ↔ CMH-peptide
- **Signal 2** : co-stimulateur (famille **B7** ou TNF-récepteur) — soit **stimulant** (CD28-B7), soit **inhibiteur** (CTLA-4-B7, PD-1-PD-L1)
- **Signal 3** : cytokines polarisantes

| Phase | Localisation | Checkpoint | Mécanisme |
|-------|--------------|------------|-----------|
| **Initiale** | Ganglion lymphoïde | **CTLA-4 ↔ B7 (CD80/CD86)** | Délocalise CD28, inhibe la phase précoce |
| **Effectrice** | Micro-environnement tumoral | **PD-1 ↔ PD-L1 / PD-L2** | Inhibe les LT effecteurs |

Les LT exprimant **CTLA-4, PD-1, TIM-3, LAG-3** deviennent **anergiques / épuisés**.

→ Les **anti-CTLA-4** et **anti-PD-1/PD-L1** lèvent ces inhibitions et restaurent une réponse anti-tumorale efficace.


![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p03_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p03_01.png]]

## Trois types de résistance

| Type | Définition |
|------|-----------|
| **Résistance primaire** | Absence de réponse **dès l’introduction** de l’ICI |
| **Résistance adaptative** | Mécanismes d’immuno-échappement qui diminuent l’efficacité au fil du traitement |
| **Résistance acquise** | Réponse initiale puis **reprogression** sous immunothérapie |

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p04_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p04_01.jpeg]]

## Mécanismes intrinsèques à la tumeur

### 1. Absence d’antigène
- **Charge mutationnelle (TMB) basse** → peu de néo-antigènes
- **Modulation épigénétique** (silencing)
- **Perte d’antigène tumoral** (mutation, délétion)

### 2. Défaut de présentation antigénique
- **Altération du CMH I (HLA)**
- Mutation de la **β2-microglobuline (B2M)** ⚠️ mécanisme classique de **résistance acquise**
- **Délétion des transporteurs TAP** → non reconnaissance par les CD8

### 3. Exclusion des LT (signalisation oncogénique)
- Altération des **voies MAPK / RAS-RAF-MEK**
- **Voie WNT/β-caténine** activée → exclusion lymphocytaire
- **Expression oncogénique de PD-L1** (constitutionnelle, indépendante de l’IFN-γ) → inhibition des LT dès leur arrivée

### 4. Insensibilité aux LT
- Altération de la **voie de signalisation IFN-γ** (récepteur, **JAK1, JAK2, STAT1**) ⚠️ mécanisme classique de **résistance acquise**
- **Diminution de Fas** → résistance à l’apoptose extrinsèque
- **Augmentation de Fas-L** sur cellule tumorale → lyse des LT effecteurs Fas+
- **Surexpression de FLIP** → résistance aux récepteurs de mort

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p05_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p05_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p06_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p06_01.jpeg]]

## Mécanismes extrinsèques à la tumeur

### 1. Défaut d’infiltration
- **Répertoire TCR limité**
- **Immuno-éditing** du TCR peu performant

### 2. Expression de checkpoints inhibiteurs sur les LT
- **CTLA-4, PD-1, TIM-3, LAG-3** sur LT effecteurs → baisse prolifération + activation
- Baisse de sécrétion de cytokines inflammatoires (**IFN-γ, TNF**)
- Baisse de dégranulation des granules lytiques

### 3. Micro-environnement immunosuppresseur
- **Treg FoxP3+, TAM (M2), MDSC**, néo-vaisseaux
- **PNN N2** pro-tumoraux

### 4. Cytokines et molécules suppressives
- **TGF-β, IL-10, IL-35, CCL22**
- **IDO** (indoléamine 2,3-dioxygénase) : catabolise le tryptophane → **kynurénines toxiques** + diminue le tryptophane (nécessaire à la prolifération T)
- **Arginase** : prive le milieu en arginine → perte de la chaîne ζ du CD3 + blocage TCR + baisse IL-2
- **Adénosine** (dégradation ATP/ADP) : inhibe les LT effecteurs

### 5. Recrutement par chimiokines
- **CCL2** → recrute Treg
- **CCL5, CCL7, CXCL18** → recrutent MDSC

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p07_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p07_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p08_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p08_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p08_02.jpeg]]

## Tableau de synthèse — résistance innée/adaptative vs acquise

| Mécanisme | Type |
|-----------|------|
| **Perte CMH/HLA** | Innée / adaptative |
| **Expression constitutive PD-L1** | Innée |
| **Altération transporteur antigénique (TAP)** | Innée / adaptative |
| **Absence d’antigène (mutation/délétion)** | Innée / adaptative |
| **Altération voies de signalisation** (recrutement LT) | Innée / adaptative |
| **Mutation B2M** | **Acquise** |
| **Down-régulation des néo-antigènes** | **Acquise** |
| **Expression PD-L1 induite par IFN-γ** | **Acquise** |



## Concept de tumeurs « chaudes » vs « froides »

| Type | Caractéristiques | Réponse à l’ICI |
|------|------------------|-----------------|
| **Tumeur chaude (hot)** | Infiltrée par **LT cytotoxiques** ; activité immunitaire préexistante ; **TMB élevé** ; PD-L1+ ; **MSI-H** souvent | **Possiblement répondeuse** |
| **Tumeur froide (cold)** | Exclusion des LT effecteurs **OU** silencieuse (invisible) ; faible TMB ; peu de néo-antigènes | **Possiblement non répondeuse** |

Causes du **défaut d’infiltration** dans les tumeurs froides :
- **Intrinsèques** : baisse TMB, altération des voies de signalisation diminuant le recrutement CD8
- **Extrinsèques** : immuno-éditing du TCR non fonctionnel ; environnement immunosuppresseur favorisant l’exclusion lymphocytaire

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p11_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p11_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p11_02.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p12_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p12_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p12_02.jpeg]]

## Stratégies pour transformer une tumeur froide en chaude

- Combinaisons **anti-CTLA-4 + anti-PD-1** (ipilimumab + nivolumab)
- Association **chimiothérapie + ICI** (libère néo-antigènes)
- **Radiothérapie + ICI** (effet abscopal)
- **Vaccins anti-tumoraux**
- Inhibiteurs d’**IDO**, **TGF-β**, **adénosine**
- **CAR-T** (effecteurs prêts à l’emploi)

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p13_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p13_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p14_00.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p14_01.jpeg]]

![[assets/pathologie-moleculaire/onco-immunologie/16-1025 sensibilité-résistance ImT Audio v1/p14_02.jpeg]]

## Pièges / Limites

- **PD-L1 IHC** est un biomarqueur **imparfait** : faux positifs (PD-L1+ non répondeurs) et faux négatifs (PD-L1− répondeurs)
- La **mutation B2M** (résistance acquise) ne peut être détectée qu’en re-biopsiant
- Distinguer **résistance vraie** d’une **pseudo-progression** (radiologie + histologie)
- L’**hétérogénéité tumorale** explique des réponses **mixtes**

---

## 🔑 Points clés à retenir

1. La sensibilité à l’ICI nécessite **4 étapes** : reconnaissance ganglionnaire, infiltration, reconnaissance tumorale, lyse (perforine/granzymes ou Fas-L/TRAIL).
2. L’activation T = **3 signaux** : TCR/CMH, co-stimulation **CD28-B7**, cytokines.
3. **CTLA-4** = checkpoint **précoce** (ganglion) ; **PD-1/PD-L1** = checkpoint **tardif** (tissu/tumeur).
4. **3 types de résistance** : primaire, adaptative, acquise.
5. **Mécanismes intrinsèques** : perte CMH/HLA, **B2M**, **JAK1/2-STAT1**, expression oncogénique PD-L1, perte d’antigène, voie WNT/β-caténine.
6. **Mécanismes extrinsèques** : Treg, TAM-M2, MDSC, **TGF-β, IL-10, IDO**, **arginase**, **adénosine**, chimiokines (CCL2/5/7).
7. **Résistance acquise classique** : mutation **B2M**, down-régulation des néo-antigènes, perte de signalisation **IFN-γ (JAK1/2)**.
8. **Tumeurs chaudes** = TIL+, TMB élevé, PD-L1+, **MSI-H** → bonnes répondeuses.
9. **Tumeurs froides** = exclusion ou invisibilité immunitaire → mauvaises répondeuses ; cibles des combinaisons (chimio/radio + ICI).
10. La compréhension de ces mécanismes guide les **combinaisons thérapeutiques** et le développement de nouveaux biomarqueurs prédictifs.
