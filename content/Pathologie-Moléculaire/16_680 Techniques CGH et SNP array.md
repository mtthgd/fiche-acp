---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - methodes_etudes_adn
  - CGH
  - SNP_array
  - CNV
  - LOH
  - microdélétion
  - amplification
  - MDM2
  - EGFR
  - puce
  - microarray
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Techniques CGH-array et SNP-array

> Liens : [[16_620 Principes de cytogénétique]] | [[16_610 Généralités sur les chromosomes]] | [[16_510 Principes du séquençage massif parallèle]] | [[16_270 Instabilité génétique]] | [[16_630 La FISH appliquée à l'anapath]]

## Principe / Bases

### Définitions

**CGH** = **C**omparative **G**enomic **H**ybridization

| Terme | Signification |
|-------|---------------|
| **Hybridation** | Appariement des bases nucléotidiques par complémentarité |
| **Génomique** | Analyse **globale** du génome entier (≠ FISH ciblée) |
| **Comparative** | Comparaison **quantitative** ADN tumoral vs ADN témoin |
| **Array (puce)** | Cible = micro-réseau d’ADN sur lame de verre, milliers de **spots** d’ADN couvrant tout le génome (chr 1 → 22 + X + Y) |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p01_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p02_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p03_00.png)

### Caractéristiques de la CGH-array

| Caractéristique | Détail |
|-----------------|--------|
| **Quantitative** | Détecte les **CNV** (Copy Number Variations) : gains, amplifications, pertes/délétions |
| Ne détecte **PAS** | Mutations ponctuelles, **translocations équilibrées**, inversions équilibrées, **micro-anomalies** |
| **Pangénomique** | Couvre tout le génome (limite = densité des spots) |
| **Comparative et compétitive** | Hybridation compétitive de 2 ADN marqués sur la même puce |

## Acteurs / Sondes / Réactifs

### Étape 1 — Marquage des ADN

| Acteur | Source | Marquage |
|--------|--------|----------|
| **ADN tumoral** | Tissus FFPE ou congelés | **Cyanine 5** (Cy5, rouge) |
| **ADN référence** | Compagnies commerciales | **Cyanine 3** (Cy3, vert) |

Étapes : extraction → fragmentation → incorporation du fluorochrome.



### Étape 2 — Hybridation sur puce

1. Mélange équimolaire des deux ADN marqués
2. **Dénaturation** → ADN simple brin
3. Dépôt sur la puce
4. **Hybridation** dans un four à T° définie pendant plusieurs heures
5. **Lavages**

> Les séquences identiques **rentrent en compétition** pour s’hybrider sur leur spot cible. La séquence la plus représentée a plus de chances de fixer son spot → couleur dominante locale.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p05_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p06_00.jpeg)

### Étape 3 — Détection par numérisation

Le logiciel calcule pour chaque spot le **ratio de fluorescence** ADN tumoral / ADN référence.

| Ratio | Interprétation |
|-------|----------------|
| **Équivalent** | Pas d’anomalie quantitative |
| Tumoral **<** référence | **Perte / délétion** |
| Tumoral **>** référence | **Gain** |
| Tumoral **>>** référence | **Amplification** (généralement > 10 copies excédentaires) |

### Étape 4 — Analyse des données

Conversion en données **logarithmiques** : **log₂ ratio**.

| Log ratio | Signification |
|-----------|---------------|
| **= 0** | Absence d’anomalie |
| **> 0** | Gain |
| **< 0** | Perte |
| **>>> 0** (élevé) | Amplification |

Représentation graphique :
- Abscisse : chromosomes 1 à 22 + X + Y
- Ordonnée : log ratio
- Ligne noire = log ratio ; nuage bleu/rouge = variations non significatives

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p07_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p08_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p09_00.png)

## Workflow technique illustré

### Profil plat (pas d’anomalie)
Log ratio = 0 sur tous les chromosomes.

### Gains et pertes segmentaires — exemple : carcinome rénal à cellules claires
- **Perte 3p** : anomalie **caractéristique** du **CCRCC**
- Gain 5q
- Perte du chromosome 14 entier
- Anomalies secondaires : gain 7q, perte 8p

### Amplifications — exemple : liposarcome dédifférencié
- **Amplification 12q15** comprenant **MDM2** (log ratio = **4,66**)
- Amplification du chromosome 1
- Profil très évocateur dans contexte de **sarcome indifférencié** sur le plan anatomopathologique

### Pronostic — exemple : mélanome uvéal/choroïdien
- **Perte du chromosome 3** = facteur **péjoratif**

### Théragnostique — exemple : glioblastome
- **Gain du chromosome 7** + **perte du chromosome 10** = anomalies typiques
- **Amplification EGFR** (7p11) → éligibilité à thérapie ciblée


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p11_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p12_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p13_00.png)

## Lecture / Interprétation — Limites de la CGH

| Limite | Détail |
|--------|--------|
| **Pertes d’hétérozygotie (LOH)** sans CNV | Non détectées par CGH (besoin de SNP-array) |
| **Anomalies équilibrées** (translocations, inversions) | Non détectées |
| **Mutations ponctuelles** | Non détectées (besoin de NGS) |
| **Anomalies épigénétiques** | Non détectées |
| **Hétérogénéité cellulaire** | Anomalie présente dans une faible proportion → manquée |
| **Résolution de la puce** | Régions absentes de la puce = invisibles |
| **Polymorphismes** (CNV non pathogènes) | Risque d’interprétation erronée |

---

# 2. Technique SNP-array

## Principe / Bases

**SNP** = **S**ingle **N**ucleotide **P**olymorphism (snip).

| Notion | Détail |
|--------|--------|
| **Polymorphisme de séquence** | < **1 %** du génome humain ; pour un locus donné, deux allèles : **A (majeur)** et **B (mineur)** |
| **Fréquence allèle mineur** | Faible mais **> 1 %** dans la population saine |
| ≠ **Mutation pathologique** | Fréquence < 1 % |

> Plusieurs **centaines de milliers** de SNPs identifiés et caractérisés (locus, allèles, fréquences).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p15_00.png)


## Acteurs / Sondes / Réactifs

### Différences avec la CGH-array

| | CGH-array | SNP-array |
|--|-----------|-----------|
| Hybridation | **Compétitive** (2 ADN) | **Non compétitive** (1 seul ADN tumoral) |
| Spots | Séquences génomiques | Spots contenant **soit allèle A, soit allèle B** dans les régions de SNP connues |
| Information | Quantitative uniquement | Quantitative **+** qualitative (LOH) |
| Quantité d’ADN nécessaire | Plus élevée | **Moindre** |

### Workflow SNP-array

1. Marquage de l’ADN tumoral par molécule fluorescente
2. Hybridation **non compétitive** sur puce
3. Numérisation
4. Analyse :
   - **Données quantitatives** → intensité du signal (comme CGH)
   - **Données qualitatives** → hybridation ou non sur les spots A vs B → détection des **LOH**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p18_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p19_00.png)

## Lecture / Interprétation

### Représentation graphique
3 graphiques superposés :
1. **Log ratio de fluorescence** (CNV — comme CGH)
2. **Allele difference** (-1 / 0 / +1)
3. **B-Allele Frequency (BAF)** (0 / 0,5 / 1)

### Détection d’une perte d’hétérozygotie sans anomalie quantitative

| Génotype | Allele difference | BAF |
|----------|:-----------------:|:----:|
| AB (hétérozygote) | 0 | **0,5** |
| AA (homozygote) | +1 | 0 |
| BB (homozygote) | -1 | 1 |

| Chromosome | Profil normal | Profil avec LOH |
|-----------|----------------|------------------|
| Allele difference | **3 valeurs** : -1, 0, +1 | **2 valeurs** : -1, +1 |
| B-Allele Frequency | **3 valeurs** : 0, 0,5, 1 | **2 valeurs** : 0, 1 |
| Génotypes | AA, AB, BB | AA, BB (**AB perdu**) |

> **Mécanisme** : un chromosome est perdu, l’autre (porteur d’une mutation oncogène) est **dupliqué** → pas de CNV apparent mais perte de l’hétérozygotie.

### Exemple — glioblastome
- Profil quantitatif : gain chr 7, perte 9p, perte 16q, gain 19p, perte chr X
- Pas de perte apparente du **chromosome 10** sur la CGH
- **Mais** : LOH du chromosome 10 détectée par SNP-array (BAF à 0/1, allele difference -1/+1) → anomalie classique du glioblastome (perte chr 10) **masquée par duplication compensatrice**


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/methodes-etudes-adn/16-680%20Tecniques%20de%20CGH-SNP-pdf/p21_00.png)

## Indications cliniques majeures

| Tumeur | Anomalie clé | Intérêt |
|--------|--------------|---------|
| **Carcinome rénal à cellules claires** | Perte 3p (+ gain 5q, perte chr 14) | Diagnostique |
| **Liposarcome dédifférencié** | Amplification **MDM2** (12q15) | Diagnostique |
| **Mélanome uvéal/choroïdien** | Perte chr 3 | Pronostique |
| **Glioblastome** | Gain chr 7 + perte chr 10 + amplification **EGFR** | Diagnostique + théragnostique |
| **Neuroblastome** | Gain/perte segmentaires (mauvais pronostic) vs gain chromosomes entiers (bon pronostic) | Pronostique |

## Avantages / Limites comparées

| Critère | CGH-array | SNP-array |
|---------|:---------:|:---------:|
| Quantitatif (CNV) | Oui | Oui |
| Pangénomique | Oui | Oui |
| **LOH sans CNV** | **Non** | **Oui** |
| Mutations ponctuelles | Non | Non |
| Translocations équilibrées | Non | Non |
| Quantité d’ADN | Plus | **Moins** |
| Coût | – | Légèrement supérieur |

> À terme, le SNP-array tend à **remplacer la CGH** (valeur ajoutée LOH + moindre quantité d’ADN).

---

## 🔑 Points clés à retenir

1. **CGH-array** = analyse **quantitative pangénomique compétitive** (ADN tumoral Cy5 vs ADN référence Cy3) ; détecte les **CNV** : gains, amplifications, pertes.
2. **Ne détecte pas** : mutations ponctuelles, **translocations/inversions équilibrées**, micro-anomalies, anomalies épigénétiques, **LOH sans CNV**.
3. Lecture par **log₂ ratio** : 0 = normal, > 0 = gain, < 0 = perte, **>>> 0** = amplification (souvent > 10 copies).
4. Exemples diagnostiques : **perte 3p** (carcinome rénal à cellules claires), **amplification MDM2 12q15** (liposarcome dédifférencié), **perte chr 3** (mélanome uvéal — pronostique).
5. Exemple théragnostique : **gain chr 7 + amplification EGFR** dans le glioblastome (+ perte chr 10).
6. **SNP-array** = même principe + détection des **pertes d’hétérozygotie (LOH)** sans CNV.
7. Hybridation **non compétitive** (1 seul ADN), spots avec allèle **A** ou allèle **B** dans les régions de SNP connues.
8. **3 graphiques** : log ratio (CNV) + **allele difference** + **B-Allele Frequency** ; LOH = perte du génotype **AB**.
9. Exemple SNP : glioblastome avec **LOH chromosome 10** masquée par duplication compensatrice (perte initiale + duplication du chromosome restant porteur d’une mutation pathogène).
10. SNP-array tend à **remplacer la CGH** : valeur ajoutée (LOH) + nécessite **moins d’ADN tumoral** ; reste **complémentaire** au [[16_510 Principes du séquençage massif parallèle|NGS]] (mutations) et à la [[16_630 La FISH appliquée à l'anapath|FISH]] (équilibrées).
