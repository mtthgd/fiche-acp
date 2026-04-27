---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_adn
  - génome_humain
  - exons
  - introns
  - pseudogènes
  - séquences_répétées
  - microsatellites
  - polymorphismes
  - CNV
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Différents types de séquences du génome humain

> Liens : [[16_101 Rappels sur la structure de l'ADN]] | [[16_190 Bases de données génomiques internationales]] | [[16_280 Méthylation de l'ADN]] | [[16_510 NGS - Principes et applications]]

## Génome mitochondrial vs nucléaire

| Caractéristique | ADN mitochondrial | ADN nucléaire |
|-----------------|-------------------|---------------|
| Localisation | Mitochondrie | Noyau (membrane nucléaire) |
| Structure | **Circulaire fermée** | **Linéaire ouverte** |
| Transmission | **Matrilinéaire exclusive** | Bi-parentale |
| Taille | Très petite | **3 milliards** de paires de bases |
| Séquences peu conservées | Très peu | **Majoritaires** |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p02_00.jpeg)

## Génome nucléaire — chiffres clés

- **24 molécules** d’ADN linéaire double brin (24 chromosomes humains : 22 autosomes + X + Y)
- **3 × 10⁹ paires de bases**
- **% GC ≈ 37 %**
- **~25 000 à 26 000 gènes**
- Les gènes humains ne sont **pas des entités distinctes** : leurs transcrits **chevauchent** souvent ceux d’autres gènes (parfois sur les deux brins)

| Composante | Part du génome |
|------------|----------------|
| **Exons** | 2,32 % |
| Bases **codantes** | **1,13 %** |
| Bases dans **introns + UTR** | 38,2 % |
| Variants distinguant 2 individus | ~ **1 million** |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p03_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p03_02.jpeg)

## Séquence consensus — versions du génome

- Génome humain établi à **99 %**
- **Séquence consensus** : à chaque position, la base la plus représentative parmi plusieurs individus
- Mise à jour continue par le **Genome Reference Consortium (GRC)**

| Version actuelle | Alias UCSC |
|------------------|------------|
| **GRCh38** (NCBI) | **HG38** |
| GRCh37 (précédente) | HG19 |

Format de stockage standard = **FASTA** (fichier texte).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p04_00.jpeg)

## Systèmes de coordonnées

| Système | Résolution | Usage |
|---------|-----------|-------|
| **Coordonnées chromosomiques** (sous-bandes) | ~ **2 Mb** | Cytogénétique : caryotype, FISH, **CGH array** (grandes mutations) |
| **Coordonnées génomiques** | **1 base** | Décrit précisément les mutations (ex : substitution C>G en chr1:position) |
| **Coordonnées exoniques** | 1 base, repère gène | **+1** = a du codon ATG initiateur ; **−1, −2…** avant ATG ; **+1\*, +2\*…** après codon stop ; **+1, +2…** au début d’intron |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p06_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p08_00.jpeg)

## Polymorphismes du génome

### SNP (mutations ponctuelles)
- Polymorphismes ponctuels isolés, **généralement sans implication fonctionnelle** (sauf régions codantes/régulatrices)
- Densité : **1 base/2 kb** soit **~1,5 million** par génome haploïde
- Répartition variable, permettent une **cartographie génomique** propre à chaque individu

### CNV (Copy Number Variations)
- **Variations du nombre de copies** d’un ou plusieurs gènes (duplications, insertions, délétions locales)
- **> 12 % du génome humum** concerné, polymorphismes individuels
- Implications pathologiques potentielles : **autisme, schizophrénie, cancer**
- Peuvent être soumises à la **sélection** (modulation de la quantité de protéines)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p09_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p10_00.jpeg)

## Gènes — distribution

- **~25 000 gènes** pour **> 100 000 protéines** (épissage alternatif, modifications post-traductionnelles)
- Taille variable : **1 kb → 2 Mb**
- Gènes occupent **~25 %** du génome nucléaire (pseudogènes inclus), dont seulement **2 %** codant pour des protéines
- Répartition **hétérogène** :
  - Faible densité aux **centromères**
  - **Absents dans l’hétérochromatine**
  - Identifiables par les **îlots CpG**
- Densité moyenne : **12 gènes/Mb** chez l’homme (vs 76-479 chez la levure)


## Types d’ARN issus des gènes

| Type d’ARN | Devenir |
|-----------|---------|
| **ARN codants** (ARNm) | Traduits en protéines |
| **ARN non codants** | Non traduits (régulation, structure…) |

## Architecture des gènes

### Monoblocs vs morcelés
- **Monobloc** : très rare (ex : **histone H4**)
- **Morcelé** : le plus fréquent → **exons + introns**

| Élément | Définition |
|---------|------------|
| **Exon** | Segment transcrit en ARN, exporté, **présent dans l’ARN mature** |
| **Intron** | Segment transcrit puis **éliminé** dans le noyau (peut atteindre **800 kb**) |

- **2 à 200 exons** par gène (moyenne **9**)
- Partie codante = **2 % de la taille du gène**

### Uniques vs répétés
- Majorité **uniques ou potentiellement dupliqués**
- **Histones** = exemple de gènes répétés
- Souvent regroupés en **familles** (mécanismes de duplication)
- Peuvent être **chevauchants** ou **nichés**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p13_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p14_01.jpeg)

### Pseudogènes
- **Copies non fonctionnelles** d’un gène, séquence partiellement/fortement tronquée
- Peuvent provenir de l’**intégration d’un ADN rétro-transcrit** à partir d’un ARNm
- Observés au sein des **familles de gènes**
- Potentiellement transcriptibles (et traduits en protéines aberrantes) s’ils ne possèdent pas de **codon-stop prématuré**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p15_00.jpeg)

## ADN intergénique

- **75 % du génome humain**
- Composé de segments de longueurs très diverses
- Rôle important dans : **plasticité, variation, évolution** du génome

## ADN répété

Plus la complexité de l’organisme augmente, plus la **proportion d’ADN répétitif** augmente.

### ADN moyennement répétitif dispersé — éléments mobiles
Origine : **transposons** capables de se déplacer (gènes "sauteurs"). Très peu encore mobiles aujourd’hui.

| Catégorie | Mécanisme | Part du génome |
|-----------|-----------|----------------|
| **Rétrotransposons** | Recopiage via intermédiaire **ARN** | Mécanisme efficace de **brassage d’exons** |
| Rétrovirus endogènes intégrés | Peu actifs | **16 %** |
| Transcrits sans activité connue | – | **30 %** |
| Séquences répétitives | – | **3 %** |
| **Transposons (ADN)** | "Copier-coller" via **transposase**, sans intermédiaire ARN | **Aucun actif chez l’homme** (vestiges) |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p16_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p17_00.png)

### ADN hautement répété (non codant)

- **10-15 % du génome**, toujours aux **mêmes endroits**
- Hétérochromatique, autour des centromères et télomères

| Type | Description |
|------|-------------|
| **α-satellites, β-satellites, satellites 1/2/3** | ADN **centromérique** |
| **Mini-satellites** | 10 à 100 pb répétées 100-2000 ×, surtout **télomères** |
| **Microsatellites** | **1 à 8 nucléotides** répétés 5-50 × |

**Implications pathologiques** :
- **Maladies à répétition de triplets** (ex : Huntington, X fragile)
- **Cancers** (ex : **syndrome de Lynch** = instabilité microsatellite)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p18_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p20_00.jpeg)

## Séquences uniques conservées

- **Très conservées** (96 % chez les mammifères), **non codantes**
- Souvent près des **régions régulatrices**
- Rôle dans :
  - Régulation de l’**expression des gènes**
  - **Appariement correct des chromatides**

L’**ADN non répété** correspond essentiellement aux **gènes codant pour des protéines**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-115%20Diff%C3%A9rents%20types%20de%20s%C3%A9quences%20du%20g%C3%A9nome%20humain%20NON%20SONORISE/p22_00.png)

---

## 🔑 Points clés à retenir

1. ADN nucléaire **3 × 10⁹ pb**, **24 chromosomes**, **% GC ≈ 37 %**, **~25 000 gènes**
2. Bases **codantes = 1,13 %** ; exons = 2,32 % ; introns + UTR = 38,2 %
3. ADN mitochondrial : **circulaire**, **transmission matrilinéaire**
4. Référence actuelle = **GRCh38 / HG38** (Genome Reference Consortium)
5. **Coordonnées exoniques** : +1 = A du codon ATG ; -1/-2 avant ATG ; +1*/+2* après stop
6. **SNP** : 1/2 kb soit **1,5 million** par génome haploïde ; **CNV > 12 %** du génome
7. Gènes morcelés (**exons + introns** jusqu’à 800 kb) ; partie codante = **2 %** du gène
8. **Pseudogènes** : copies non fonctionnelles, attention en bio-informatique
9. ADN répété dispersé : **rétrotransposons** (16 %, intermédiaire ARN), transposons inactifs chez l’homme
10. **Microsatellites** : impliqués dans maladies à triplets et **syndrome de Lynch**
11. ADN intergénique = **75 %** du génome (plasticité, évolution)
12. Format de stockage standard = **FASTA**
