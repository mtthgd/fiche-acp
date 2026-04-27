---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - pcr_methodes
  - qPCR
  - SYBR
  - TaqMan
  - sondes_hydrolyse
  - CT
  - efficacité_PCR
  - RT-qPCR
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Principes de la qPCR

> Liens : [[16_320 PCR digitale - principe et applications]] | [[16_315 Principes de la HRM]] | [[16_365 Validation de la qualité de l’échantillon par qPCR]] | [[16_355 Principes de microdissection tissulaire]]

## Principe / Définition

La **qPCR** (PCR quantitative en temps réel ou *real-time PCR*) permet la **détection** et la **quantification** d’un acide nucléique en mesurant la **fluorescence émise à chaque cycle**, et non en point final comme la PCR conventionnelle.

⚠️ Préférer le terme **qPCR** plutôt que **RT-PCR** pour éviter la confusion avec **Reverse Transcription**.


## Composants de la réaction

- **ADN** ou **ADNc** (cDNA) préalablement préparé
- **Amorces** spécifiques du segment cible
- **Désoxynucléotides triphosphates** (dNTP)
- **ADN polymérase** (Taq)
- **Traceur fluorescent** (agent intercalant) ou **sonde**


## Phases de la qPCR

| Phase | Description |
|-------|-------------|
| **Initiation** | Bruit de fond, fluorescence < seuil |
| **Exponentielle** | Doublement quasi parfait, **efficacité ≈ 100 %** |
| **Log-linéaire** | Décroissance progressive de l’efficacité |
| **Plateau** | Saturation, généralement **> 35 cycles** |

Facteur d’amplification théorique = **2ⁿ** (n = nombre de cycles).



## Le CT (Cycle Threshold) ou CP (Crossing Point)

- Cycle où la fluorescence dépasse le **seuil** défini par rapport au **bruit de fond**
- Déterminé pour chaque tube et chaque échantillon
- Plus le CT est **précoce** (par exemple **CT = 22**), plus la quantité initiale d’ADN est **importante**
- Un CT tardif (par exemple **CT = 32** = +10 cycles) = **moins** d’ADN initial

Formule : **X = X₀ × A^N** où A = facteur d’amplification (2 si efficacité 100 %).

![[assets/pathologie-moleculaire/methodes-analyses-adn-pcr/16-310 Principes de la Q PCR/p05_00.png]]


## Efficacité de PCR

| Efficacité (%) | Facteur d’amplification | Interprétation |
|----------------|------------------------|----------------|
| **100 %** | **2,00** | Idéal |
| **90–105 %** | 1,9–2,05 | Plage acceptable |
| **87,5 %** | **1,75** | Sous-optimal |
| < 90 % | < 1,9 | Inhibition / dégradation |

Causes de **chute d’efficacité** :
- **Quantité initiale trop faible** d’ADN
- **ADN dégradé** (FFPE)
- **Inhibiteurs** de PCR

## Recommandation amplicons

- **70–200 paires de bases** = optimal sur FFPE
- Au-delà parfois possible grâce aux progrès de fixation/extraction
- **Jamais > 300 pb** sur FFPE

![[assets/pathologie-moleculaire/methodes-analyses-adn-pcr/16-310 Principes de la Q PCR/p07_00.png]]

## Méthodes de détection

### 1. Agent intercalant (SYBR Green / LC480)
- **Non spécifique de séquence**, s’incorpore à tout **ADN double brin**
- Mesure la fluorescence à chaque cycle pendant la phase d’hybridation
- Avantages : **simple**, **peu coûteux** (pas de sonde)
- Inconvénients : **moins spécifique**, **moins sensible**, **non multiplexable** (un seul fluorochrome)

### 2. Sondes TaqMan (sondes d’hydrolyse)
- **Sonde oligonucléotidique** marquée :
  - En **5’** : fluorochrome **reporter** (FAM, VIC, HEX…)
  - En **3’** : **quencher** (BHQ, DDQ, MGB)
- **Sonde libre en solution** : **pas de fluorescence** (FRET inhibition)
- **Sonde hybridée sur la cible** : la **Taq polymérase** hydrolyse la sonde lors de l’élongation → **libération du reporter** → fluorescence détectable
- Plus **spécifique**, plus **sensible**, **multiplexable**

### 3. Autres chimies
- **Sondes d’hybridation** (FRET entre 2 sondes)
- **Sondes scorpion**
- **Sondes beacon** (épingle à cheveux)


![[assets/pathologie-moleculaire/methodes-analyses-adn-pcr/16-310 Principes de la Q PCR/p12_00.png]]

![[assets/pathologie-moleculaire/methodes-analyses-adn-pcr/16-310 Principes de la Q PCR/p12_01.png]]

## Stratégies pour favoriser l’allèle muté

- Modification chimique en **3’** des amorces (dernier codon)
- **Bloqueurs** de l’allèle sauvage
- **Sondes bloquantes** anti-sauvage
- Kits multiplex commerciaux : **Roche Cobas** (EGFR ADN tissulaire/circulant), **Idylla / Biocartis**

## Contrôles obligatoires

| Type | Rôle |
|------|------|
| **Témoin externe positif** | Validation amplification |
| **Témoin externe négatif** | Détection contamination |
| **Contrôle interne** (gène de référence) | Qualité intrinsèque ADN |
| **Mise au point** | Mesure efficacité, spécificité, absence d’amplification de l’allèle muté en sauvage |

## Quantification — 3 méthodes

### 1. Quantification absolue
- Ratio des facteurs d’amplification A^CT
- Nécessite gamme étalon

### 2. ΔΔCT (méthode comparative)
- S’affranchit des efficacités si elles sont **identiques à 100 %**
- Δ CT échantillon = CT gène X − CT gène référence
- ΔΔCT = Δ CT échantillon − Δ CT calibrateur
- **ΔΔCT = 2** → **2× plus** de copies que le calibrateur
- **ΔΔCT = −2** → **4× moins** de copies

### 3. Méthode du ratio Pfaffl
- Tient compte des **efficacités** réelles de chaque cible

| Paramètre | Critère qualité |
|-----------|-----------------|
| CT exploitable | **< 35** |
| Variation entre réplicats | **< 0,5 cycle** ou Δ CT < 0,25 |

![[assets/pathologie-moleculaire/methodes-analyses-adn-pcr/16-310 Principes de la Q PCR/p16_00.png]]


## Applications en pathologie

| Domaine | Cibles |
|---------|--------|
| **Cancérologie tissulaire** | Mutations **EGFR**, **BRAF**, **KRAS** |
| **ADN circulant (cfDNA)** | Mutations résistance EGFR (T790M, C797S) |
| **Transcrits de fusion** | **NPM-ALK** (lymphome anaplasique), **EWSR1**, **NTRK** |
| **Hématologie** | **BCR-ABL** (LMC, MRD), **JAK2** (syndromes myéloprolifératifs) |
| **Méthylation** | Amorces/sondes spécifiques séquences méthylées vs non méthylées |
| **Microbiologie** | Séquences bactériennes / virales |
| **Quantification gènes** | Selon % cellules tumorales (≥ **10 %** requis pour seuil **5 %**) |

## RT-qPCR (Reverse Transcription qPCR)

**Principe** : extraction ARN → **transcription inverse** en ADNc → qPCR sur gène cible et gène de référence.

- Mesure **variation d’expression** d’un gène cible vs gène contrôle vs calibrateur
- **Gène de référence** : expression stable dans les conditions testées
- Possibilité de combiner **plusieurs gènes de référence**
- Plaques **96 puits** commerciales pour panel de pathway

## Sensibilité

- Seuil de détection en pratique : **≈ 5 %** d’allèle muté (avec ≥ 10 % cellules tumorales)
- Inférieure à la **PCR digitale** (< 0,01 %)
- Pour les faibles fréquences alléliques → contrôler en **ddPCR**

## Avantages / Limites

| Avantages | Limites |
|-----------|---------|
| Compatible **tout type** de prélèvement (FFPE, congelé, cytologie liquide) | Connaissance préalable de la **séquence** requise |
| **Sensible** (1–10 %) | Pas adaptée aux **anomalies de grande taille** (sauf points de cassure connus) |
| **Spécifique** (avec sondes) | **Faux positifs** (amplifications tardives, contamination par sensibilité) |
| Multiplexable (sondes) | **Faux négatifs** (qualité/quantité ADN) |
| Validable en routine | Limitée pour fréquences alléliques **< 5 %** |

## Pièges / Contrôles qualité

- **CT > 35** ou CT > témoin positif **+ 3 lobes ou +10 cycles** → **contrôler**
- **% cellules tumorales** doit être **> 10 %** pour atteindre le seuil **5 %**
- Réplicats : **CV CT < 0,5 cycle**
- Absence d’amplification du gène de référence → **réextraire**

## 🔑 Points clés à retenir

1. **qPCR = PCR en temps réel** avec mesure de fluorescence cycle par cycle.
2. Le **CT (cycle threshold)** est inversement proportionnel à la quantité d’ADN initial.
3. Efficacité optimale : **90–105 %** ; facteur d’amplification **2,0**.
4. **Amplicons 70–200 pb** sur FFPE, jamais > 300 pb.
5. Deux chimies principales : **agent intercalant SYBR** (simple, peu spécifique) vs **sonde TaqMan** (spécifique, multiplexable).
6. Sondes TaqMan = **5’ reporter (FAM/VIC) + 3’ quencher (BHQ)** + hydrolyse par Taq.
7. Quantification : **absolue** (gamme étalon), **ΔΔCT** (calibrateur), **ratio Pfaffl** (efficacités réelles).
8. Applications : **EGFR**, **BRAF**, **KRAS**, **BCR-ABL**, **JAK2**, transcrits de fusion, méthylation, ADNtc.
9. Sensibilité pratique **5 %** avec **≥ 10 %** de cellules tumorales — concurrencée par **PCR digitale** pour fréquences faibles.
10. Toujours inclure témoin **+**, témoin **−**, **contrôle interne** (gène de référence).
11. Critères qualité : **CT < 35**, réplicats **Δ CT < 0,5**.
12. **RT-qPCR** = ARN → ADNc → qPCR pour quantifier l’expression génique (BCR-ABL, MRD).
