---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 2G_séquençage
  - capture
  - amplicon
  - panel
  - profondeur
  - couverture
  - exome
  - PCR_multiplex
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Séquençage 2G — capture et amplicons (préparation des librairies ciblées)

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_515 Séquençage 2G - points communs]] | [[16_518 Séquençage Illumina]] | [[16_535 Le pipeline bioinformatique]] | [[16_560 Évaluation de la charge mutationnelle (TMB)]] | [[16_680 Techniques CGH et SNP array]]

## Principe général

Pour **optimiser la puissance** d’un séquenceur (et donc le coût/échantillon), on **cible** des régions d’intérêt plutôt que de séquencer le génome entier. Deux stratégies de **préparation de librairie ciblée** existent :
- **Amplicons** (PCR multiplex) — amplification des cibles
- **Capture** (sondes biotinylées) — pêche des cibles

Cette étape s’insère **après la quantification de la librairie** dans le workflow standard de [[16_515 Séquençage 2G - points communs]].


## Couverture vs profondeur — concepts fondamentaux

| Concept | Définition | Image |
|---|---|---|
| **Couverture** (coverage) | Nombre de **bases** séquencées sur le génome (étendue **horizontale**) | Largeur explorée |
| **Profondeur** (depth) | Nombre de **reads** disponibles **pour une position donnée** (axe **vertical**) | Lectures empilées sur un locus |

> Erreur de langage fréquente : « cette zone est mal couverte » → on devrait dire « cette zone a une **profondeur limitée** ».

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p03_00.png]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p04_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p05_00.jpeg]]

### Profondeurs habituelles selon l’indication

| Application | Profondeur conseillée |
|---|---|
| **Exome germline** | **≥ 50× minimum** |
| **Génome (WGS) germline** | 30× |
| **Panel ciblé somatique en oncologie** | **500× à plusieurs milliers ×** |
| Détection de **clones rares** (TMB, MRD, ctDNA) | **>1000×, parfois >10 000×** |
| Hétérogénéité tumorale | Plusieurs milliers × |

> Au-delà d’un certain seuil, **augmenter la profondeur n’apporte plus rien** (saturation diagnostique). Il faut équilibrer profondeur vs étendue selon l’objectif.

### Exploitation quantitative de la profondeur

Si une zone a 2× moins de reads qu’une autre → **2× moins de matrices initiales** → **délétion** suspectée. Inversement → **amplification**. Avec un retraitement bioinformatique, le NGS peut **remplacer la CGH-array** pour la détection des **CNV** (cf [[16_680 Techniques CGH et SNP array]]).

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p11_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p11_01.png]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p11_02.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p11_03.png]]


![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p11_05.png]]

## Calcul de répartition (exemple)

Sur une puce de **1 Gb** (1 milliard de bases), pour des reads de 200 pb :
- **5 millions de reads** disponibles
- À répartir entre **couverture** et **profondeur**

| Stratégie | Cibles | Profondeur |
|---|---|---|
| Très ciblé (1 zone de 200 pb) | **1** | 5 000 000× (inutile) |
| **Panel intermédiaire** | 100 000 zones de 200 pb | **50×** |
| **Compromis somatique** | 10 000 zones de 200 pb | **500×** |

## Cibler — pourquoi et comment

| Stratégie | % du génome | Rentabilité |
|---|---|---|
| **WGS** (génome entier) | 100 % | Coût élevé, recherche / cas complexes |
| **Exome (WES)** | ~2 % | Routine génétique constitutionnelle |
| **Exome élargi** | ~3-5 % (+ régulateurs) | Compromis recherche |
| **Panel ciblé** (cancérologie) | < 0,01 % | Routine somatique, **profondeur ↑↑** |

Seuil : si le **panel** dépasse **200 kb** de cibles, autant faire un **exome** entier.

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p12_00.png]]


![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p12_02.jpeg]]


## Méthode 1 — Amplicons (PCR multiplex)

### Principe
**Designer des amorces** spécifiques de chaque cible et **amplifier par PCR** uniquement les régions d’intérêt avant séquençage.

### En pratique
- **PCR multiplex** : plusieurs amorces dans le même tube
- Souvent **plusieurs tubes** par panel (ex. 150 cibles → ~3 tubes) pour :
  - éviter l’**hybridation entre primers**
  - homogénéiser les **températures d’annealing**
  - gérer les **% GC** disparates

### Exemples
- **Ion AmpliSeq** (Thermo Fisher), **TruSeq Amplicon** (Illumina), **Oncomine** focus


![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p12_05.png]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p12_06.png]]

## Méthode 2 — Capture (hybridation par sondes)

### Principe
Des **sondes biotinylées** complémentaires des cibles s’hybrident à l’ADN fragmenté. Les hybrides sont capturés par des **billes magnétiques streptavidine** (la **streptavidine** capte la **biotine**) → seules les séquences d’intérêt vont au séquenceur.

### Workflow
1. Librairie standard
2. **Hybridation** des sondes biotinylées
3. **Capture** sur billes magnétiques streptavidine
4. Lavages, élution, **2ᵉ amplification PCR**
5. Séquençage

### Exemples
- **SureSelect** (Agilent), **Nextera Capture / Twist Bioscience**, **TruSight Oncology 500** (Illumina, cf [[16_560 Évaluation de la charge mutationnelle (TMB)]])

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p13_00.jpeg]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p13_01.png]]

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p13_02.png]]


## Comparaison Capture vs Amplicons

| Critère | Capture | Amplicons (PCR multiplex) |
|---|---|---|
| **Taille du panel** | **Grande** (exome possible) | Petite-moyenne (jusqu’à quelques centaines de gènes) |
| **ADN initial requis** | Plus important (≥ 100 ng) | Faible (10-50 ng, **adapté FFPE**) |
| **Temps de préparation** | **Long** (1-2 jours) | **Rapide** (quelques heures) |
| **Biais d’amplification** | Faible | Important (régions GC riches) |
| **Détection CNV** | **Bonne** | Difficile (PCR détruit l’info quantitative) |
| **Détection fusions** | Bonne (sondes adaptées) | Limité aux fusions connues |
| **Coût/échantillon** | Plus élevé | Modeste |
| **Faux positifs hot-spots** | Faibles | Plus fréquents (PCR errors → **UMI** recommandés) |

![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p14_00.png]]


![[assets/pathologie-moleculaire/ngs/16-520 Le séquençage de deuxième génération, capture et amplicons audio pdf/p14_02.jpeg]]


## Indications cliniques

| Stratégie | Indication |
|---|---|
| **Petit panel amplicons** (5-50 gènes) | Routine théranostique (CBNPC EGFR, mélanome BRAF, GIST KIT/PDGFRA) |
| **Panel large capture** (>200 gènes) | Tumor profiling, **TMB**, screening complet |
| **Exome capture** | Génétique constitutionnelle, syndromes de prédisposition |
| **WGS** | Cas complexes, recherche, hémopathies (panels rare) |

## Avantages / Limites globales du ciblage

| Avantages | Limites |
|---|---|
| **Profondeur ↑↑** sur les zones d’intérêt → sensibilité ↑↑ | Peut **manquer** des cibles non incluses dans le panel |
| **Coût/échantillon ↓** | Designer les amorces / sondes = expertise |
| Multiplexage massif | Pas de détection de variants hors-panel |
| **Adaptable au FFPE** (amplicons) | Mises au point parfois longues |

---

## 🔑 Points clés à retenir

1. **Couverture = horizontal** (étendue de bases) ; **profondeur = vertical** (nombre de reads par base).
2. Profondeur conseillée : **exome ≥ 50×**, **panel somatique ≥ 500×**, **clones rares > 1000×**.
3. La profondeur exploite la **lecture quantitative** : NGS peut **remplacer la CGH-array** pour la détection de CNV.
4. Cibler évite de séquencer 100 % du génome → seuil pratique : **panel < 200 kb** sinon préférer l’**exome**.
5. **Amplicons (PCR multiplex)** = rapide, peu d’ADN, idéal **FFPE**, mais biais et faux positifs.
6. **Capture (sondes biotinylées + billes streptavidine)** = panels larges, exome, meilleur pour CNV.
7. PCR multiplex souvent **fractionnée en plusieurs tubes** (problèmes de Tm et hybridation primer-primer).
8. Choix capture vs amplicons dépend : **taille du panel, qualité ADN, CNV recherchés, budget**.
9. Au-delà d’un seuil, **augmenter la profondeur** n’apporte rien — équilibrer avec l’étendue.
10. Le ciblage s’insère **après la librairie**, avant le séquençage — étape clé d’optimisation coût/sensibilité.
