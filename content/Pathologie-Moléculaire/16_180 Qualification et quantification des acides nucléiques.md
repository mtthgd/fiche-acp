---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_adn
  - quantification
  - qualification
  - NanoDrop
  - Qubit
  - Bioanalyzer
  - spectrophotométrie
  - fluorimétrie
  - DIN
  - RIN
  - FFPE
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Qualification et quantification des acides nucléiques

> Liens : [[16_160 Électrophorèse - Partie 1]] | [[16_160 Électrophorèse - Partie 2]] | [[16_310 PCR quantitative qPCR]] | [[16_365 Validation analyse FFPE]] | [[16_510 NGS - Principes et applications]]

## Pourquoi quantifier et qualifier ?

### Quantification — finalités
- **Standardiser la quantité** d’ADN/ARN à apporter en tube (PCR) ou sur lame (CGH)
- Exemple : "**20 ng** d’ADN dans **4 µL**" → impossible sans connaître la concentration
- Quantification également indispensable **après fragmentation** d’ADN (NGS capture) et **après préparation de librairie**

### Qualification — finalités
- Évaluer l’**intégrité** de l’ADN/ARN
- Garantir une **manipulation acceptable**
- Vérifier la **taille des fragments** (NGS, capture)
- Évaluer la **quantité de fragments à la taille attendue**



## Les 4 méthodes principales

| Méthode | Principe | Quantifie | Qualifie |
|---------|----------|-----------|----------|
| **Spectrophotométrie** | Absorbance UV | Bases azotées (totalité) | Pureté (ratios A260/A280, A260/A230) |
| **Fluorimétrie** | Fluorochrome dans petit sillon ADN db | ADN double brin uniquement | – |
| **Fluorimétrie + électrophorèse capillaire** | Fluorimétrie + migration | Quantité + taille | DIN/RIN, intégrité |
| **qPCR** | Amplification temps réel | Quantité d’ADN amplifiable | Voir [[16_310 PCR quantitative qPCR]] |


## 1. Spectrophotométrie

### Principe
- Les bases azotées sont des **molécules planes** avec **hétérocycles aromatiques** et **liaisons conjuguées**
- Résonance électronique → **absorbance UV à 260 nm**
- Loi de **Beer-Lambert** : A = ε × ℓ × C
  - ε = coefficient d’extinction molaire (spécifique : ADN db, ADN sb, ARN)
  - ℓ = longueur traversée (cm)
  - C = concentration (mol/L)

Rappel composition d’un nucléotide :
- **Acide phosphorique** (mono/di/triphosphate)
- **Sucre pentose**
- **Base azotée** (purines : A, G ; pyrimidines : C, T, U)




### NanoDrop — exemple pratique
- Spectrophotomètre **sans cuvette** : dépôt direct sur **piédestal**, faisceau UV traversant
- Mesure simultanée à **260, 280 et 230 nm**

### Ratios de pureté

| Ratio | Valeur attendue | Interprétation si anormale |
|-------|------------------|----------------------------|
| **A260/A280** | **~1,8** (ADN pur) | **< 1,8** : présence de **protéines** ; **> 1,8** : présence d’**ARN** |
| **A260/A230** | ~2,0-2,2 | < 2 : contamination par solvants/sels (phénol, guanidine, EDTA) |

Profil typique d’un ADN pur : pic à 260 nm, vallée à 230 nm, faible absorbance à 280 nm.





### ⚠ LIMITE MAJEURE
La spectrophotométrie **quantifie toutes les bases azotées sans distinction** : pas de différence entre :
- **ADN intègre double brin** directement amplifiable
- **ADN dégradé**, oligonucléotides, mononucléotides

→ **Surestimation de la quantité d’ADN exploitable**, surtout sur **ADN issus de FFPE**.

## 2. Fluorimétrie

### Principe
- L’ADN forme une double hélice de Watson-Crick avec **petit et grand sillon**
- Un **fluorochrome** s’**incorpore dans le petit sillon** d’un ADN **double brin**
- Sous excitation, le fluorochrome **émet une fluorescence**
- Quantité de fluorescence **directement proportionnelle** à la quantité d’**ADN double brin**

→ Quantifie **uniquement** l’ADN double brin (intègre, exploitable).

### Appareils
- **Qubit** (Invitrogen)
- **Quantus** (Promega)





## Comparaison Spectrophotométrie vs Fluorimétrie sur cas réels

Étude sur ADN extraits de cancers (côlon, gliome, mélanome, poumon) :
- Quantification par **fluorimétrie** + **spectrophotométrie**
- Calcul du **rapport spectro/fluo**
- Mesure du **A260/A280** (pureté)
- Évaluation **NGS** : nombre de variants attendus ~20, % transitions C>T attendu ~25-30 %

| Spectro/Fluo | A260/A280 | NGS — variants | NGS — % transitions C>T | Interprétation |
|--------------|-----------|----------------|--------------------------|----------------|
| **3** | – | ~ acceptable | un peu élevé | Exploitable |
| **8,2** | – | 12 | 16 % | Exploitable |
| **65** | – | **226** | **95 %** | **NON exploitable** : artefacts massifs liés à la dégradation |

**Règle** : plus le **rapport spectro/fluo est élevé**, **plus l’ADN est dégradé** → **risque de surestimer la quantité d’ADN amplifiable** par spectrophotométrie.

→ Pour les manipulations sensibles (NGS, **surtout sur FFPE**), la spectrophotométrie est **à proscrire** comme méthode unique.


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-180%20Qualification%20et%20quantification%20des%20acides%20nucl%C3%A9iques/p08_01.jpeg)



## 3. Fluorimétrie + électrophorèse capillaire

### Principe
Couplage des deux mesures :
- **Fluorescence** dans l’ADN double brin (quantification précise)
- **Migration en électrophorèse capillaire** (taille des fragments)

### Appareils
- **TapeStation** (Agilent)
- **Bioanalyzer 2100** (Agilent)
- **MultiNA**

### Lecture
- Profil = **électrophorégramme** affichant la fluorescence selon la taille
- Mesure de la **taille moyenne** des fragments (ex : **214 pb**)
- Score de qualité : **DIN** (DNA Integrity Number) ou **RIN** (RNA Integrity Number) sur échelle 1-10

### Application
Indispensable lors de la préparation de **librairies NGS par capture** :
- Vérifier la taille des fragments **avant** séquençage
- Quantifier la fraction de fragments à la taille attendue






## 4. qPCR — quantification d’ADN amplifiable

Méthode de référence pour confirmer qu’un ADN est **amplifiable** (notamment lorsque le rapport spectro/fluo est borderline) → cf [[16_310 PCR quantitative qPCR]].



## Synthèse — comparatif des méthodes

| Critère | Spectrophotométrie (NanoDrop) | Fluorimétrie (Qubit) | Fluorimétrie + capillaire (Bioanalyzer) |
|---------|-------------------------------|----------------------|------------------------------------------|
| **Coût** | Faible | Moyen | Élevé |
| **Rapidité** | Très rapide | Rapide | Modérée |
| **Pureté** | **Oui** (A260/A280, A260/A230) | Non | Non |
| **Quantification** | Toutes bases azotées (surestime) | **ADN db uniquement** | ADN db + taille |
| **Distingue ADN dégradé / intègre** | **NON** | Oui (partiellement) | **OUI** |
| **Taille des fragments** | Non | Non | **OUI** |
| **Recommandation FFPE / NGS** | **À proscrire seul** | Bien | **Idéal** |





## Conclusion — adapter la méthode à l’usage

| Technique en aval | Méthode minimale conseillée |
|-------------------|------------------------------|
| **PCR simple, qualitative** | Spectrophotométrie suffit |
| **CGH array** | Fluorimétrie ou couplée |
| **NGS, surtout FFPE** | **Fluorimétrie + Bioanalyzer/TapeStation** + qPCR |
| **Préparation librairies** | Fluorimétrie + capillaire **avant** séquençage |

**Objectif final** : obtenir un ADN/ARN
- **Bonne qualité** (sans inhibiteur, non dégradé, surtout en **FFPE**)
- À la **taille attendue**
- En **concentration suffisante**
- Pour réaliser une analyse **efficace et sensible**

---

## 🔑 Points clés à retenir

1. **Quantifier** = standardiser les apports en tube ; **qualifier** = juger l’intégrité avant manip
2. **Spectrophotométrie** (NanoDrop) : rapide, peu coûteuse, quantifie **toutes les bases** sans distinction → **surestime** sur ADN dégradé
3. **A260/A280 ≈ 1,8** pour ADN pur ; < 1,8 → protéines ; > 1,8 → ARN
4. **A260/A230 ≈ 2** ; bas → solvants/sels (phénol, guanidine)
5. **Fluorimétrie (Qubit)** : fluorochrome dans le **petit sillon**, quantifie **uniquement l’ADN double brin** = ADN exploitable
6. **Rapport spectro/fluo élevé** = ADN dégradé → risque d’**artefacts NGS** majeurs (transitions C>T aberrantes)
7. La spectrophotométrie est **à proscrire seule** sur **FFPE** et avant **NGS**
8. **Bioanalyzer / TapeStation** = fluorimétrie + électrophorèse capillaire → quantité **+ taille** des fragments
9. Score **DIN/RIN** = indice d’intégrité de l’ADN/ARN
10. Quantification/qualification **post-fragmentation** indispensable avant capture NGS
11. **qPCR** = méthode de référence pour estimer la quantité d’ADN **amplifiable**
12. Adapter la méthode à la technique aval (PCR, CGH, NGS) et à la matrice (frais vs FFPE)
