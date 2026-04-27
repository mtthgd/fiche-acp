---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - connaissances_fondamentales
  - méthylation_ADN
  - bisulfite
  - pyroséquençage
  - MGMT
  - puces_méthylation
  - nanopore
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Techniques d’analyse de la méthylation de l’ADN

> Liens : [[16_280 Modifications épigénétiques - Méthylation de l'ADN et histones]] | [[16_260 Réparation des lésions de l'ADN]] | [[16_270 Instabilité génétique]] | [[16_320 PCR digitale - principe et applications]] | [[16_510 Principes du séquençage massif parallèle]]

## Objectifs

- Comprendre le principe de la **conversion bisulfite**
- Connaître les techniques principales : **pyroséquençage**, **MS-PCR**, **puces de méthylation**, **NGS nanopore**
- Application clinique paradigmatique : **méthylation du promoteur MGMT** dans le glioblastome

## Principe : du changement épigénétique au changement de séquence

> Étudier la méthylation de l’ADN = étudier si les **cytosines** dans les dinucléotides **CpG** sont méthylées ou pas.

L’**astuce** repose sur une **chimie** qui transforme un changement épigénétique (qui ne se voit pas par séquençage) en un véritable **changement de séquence** (détectable par n’importe quelle technique de séquençage).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p01_00.jpeg)

## Application clinique majeure : MGMT et glioblastome

### Contexte clinique

- **MGMT** = **O⁶-Méthylguanine-ADN-Méthyltransférase** : gène de réparation de l’ADN
- **Étude annexe du protocole STUPP** (radiothérapie + témozolomide dans le glioblastome) :
  - **Promoteur MGMT méthylé** → survie médiane de **21 mois**
  - **Promoteur MGMT non méthylé** → survie médiane de **15 mois**
- → Recherche systématique du statut MGMT, en particulier chez les **patients âgés**

### Mécanisme d’action — hypothèses

- **Témozolomide** = agent **alkylant** (méthylant) : ajoute des radicaux **CH3** sur les **guanines** (surtout en N7, accessoirement en O6)
- → mésalliance G-T → blocage de la réplication → mort cellulaire
- **MGMT** retire les CH3 des **guanines en O6** → résistance au témozolomide
- **Hypothèse classique** : promoteur MGMT méthylé → MGMT peu exprimée → meilleure sensibilité aux alkylants
- **Nuance** : le bénéfice de survie persiste **même sans témozolomide** → la méthylation MGMT est probablement aussi un **marqueur d’un phénotype hyperméthylé global** (CIMP-like) plutôt qu’un strict marqueur de sensibilité au témozolomide

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p02_00.png)


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p06_00.png)

## Étape clé : la conversion bisulfite

### Principe biochimique

- Le **bisulfite de sodium** (Na₂S₂O₅, additif alimentaire **E222** des effaceurs d’encre) :
  - **Désamine** les **cytosines non méthylées** → transformées en **uraciles**
  - Les **5-méthylcytosines sont protégées** (le radical CH3 fait office de « casque »)
- Après PCR : l’uracile est répliqué en **thymine** → **changement de séquence** détectable
  - **C non méthylée** → **U** → **T** (après PCR)
  - **C méthylée** → reste **C** (après PCR)

### Limites de la bisulfitation

| Problème | Conséquence |
|----------|--------------|
| **Action trop longue / agressive** | Le radical CH3 ne suffit plus à protéger → la C méthylée est aussi convertie → **faux négatifs** |
| **Action insuffisante** | Les C non méthylées ne sont pas converties → **faux positifs** |
| **Dégradation de l’ADN** | ~90 % de l’ADN dégradé en 4 h à 55 °C (agent agressif) |

> Étape **délicate à contrôler** ; nombreux **kits** commerciaux pour la standardiser.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p07_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p08_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p10_00.png)

## Techniques d’analyse après bisulfitation

### Tableau comparatif

| Technique | Principe | Quantitatif ? | Avantages | Limites |
|-----------|----------|:-------------:|-----------|---------|
| **MS-PCR** (Methylation-Specific PCR) | Amorces spécifiques C ou T (méthylé / non méthylé) | Semi-quantitatif | Simple, peu coûteux | Qualitatif, biais d’amorce |
| **Pyroséquençage** | Séquençage par incorporation et émission de lumière | **Quantitatif +++** | **Référence pour MGMT** | Coût, équipement |
| **MethyLight** | qPCR avec sonde TaqMan | Quantitatif | Sensible | Étude limitée à quelques sites |
| **Puces d’hybridation** (450K, 850K, EPIC) | Sondes oligonucléotidiques sur billes de silice | Quantitatif | **Pangénomique** | Coût élevé |
| **NGS bisulfite** (WGBS, RRBS) | Séquençage massif après conversion | Quantitatif | Pangénomique précis | Coût, complexité |
| **NGS nanopore** | Détection directe sans bisulfitation | Quantitatif | **Sans bisulfitation** | Technologie émergente |

## Technique de référence pour MGMT : le pyroséquençage

### Étapes

1. **Bisulfitation** de l’ADN génomique
2. **PCR** d’amplification de la zone du promoteur contenant les îlots CpG d’intérêt
3. Le kit utilisé permet l’analyse de **5 sites CpG** dans l’**exon 1** de MGMT (qui contient le promoteur ; la séquence codante commence après)
4. **Pyroséquençage** : à chaque îlot CG potentiellement variable → on note **Y** (= **C ou T**) ; le pyroséquenceur propose successivement T puis C → mesure du signal lumineux émis (**quantitatif**)
5. Logiciel = moyenne des 5 CpG → pourcentage de méthylation

### Lecture

- Pic de **T** dominant → cytosine **non méthylée** (transformée en T)
- Pic de **C** dominant → cytosine **méthylée** (protégée)
- Le pyroséquenceur **quantifie** le signal → ex. « **2 % de cytosine méthylée** » à un CpG donné
- Moyenne des 5 CpG → résultat global

### Seuil

- **8 % de méthylation** = seuil validé sur cohortes de patients pour ségréger les bons et les mauvais répondeurs
- **Variable continue** : plus le glioblastome est méthylé, meilleur le pronostic (surtout > 35 %)
- **Hétérogénéité tumorale** : le pourcentage **varie selon la zone** prélevée (centre vs périphérie) → résultats parfois discordants




![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p19_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p20_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p21_00.png)

> ⚠ Selon le **kit utilisé**, ce ne sont pas les mêmes CpG du promoteur MGMT qui sont étudiés. Vérifier qu’une **cohorte clinique** a validé les CpG analysés.

## Puces d’hybridation pangénomiques (Illumina Infinium)

### Évolution

| Génération | Nombre de CpG analysés |
|-------------|--------------------------|
| **HumanMethylation450K** | ~450 000 CpG |
| **EPIC (850K)** | ~850 000 CpG |
| EPIC v2 | > 900 000 CpG |

> **Pas besoin** d’interroger les 28 millions de CpG du génome : 450 K-850 K bien choisis dans des promoteurs de gènes d’intérêt **suffisent** à très bien classifier les tumeurs.

### Principe technique

- **Billes de silice** enchâssées dans des micro-puits
- Chaque bille = recouverte d’**oligonucléotides** reconnaissant la séquence juste avant le CpG d’intérêt
- Hybridation des fragments d’ADN bisulfité
- **Extension d’une paire de bases** par une polymérase avec des nucléotides marqués (vert ou rouge selon C ou T)
- **Quantification** des allèles via l’intensité fluorescente

### Applications

- **Classification des tumeurs cérébrales** par méthylome (DKFZ classifier — voir [[16_280 Modifications épigénétiques - Méthylation de l'ADN et histones]])
- Détection du **phénotype hyperméthylateur (CIMP)**
- **Résultats CGH-like** simultanés (gains/pertes de copies)
- Identification de **nouvelles entités tumorales**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p23_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p24_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p25_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p26_00.png)

## NGS de troisième génération — séquençage par nanopore

### Principe

- Brin d’ADN **simple-brin** entraîné dans un **nanopore** protéique
- Le passage des bases perturbe le **flux ionique** transmembranaire → signal électrique caractéristique de chaque base
- **5-méthylcytosine** envoie un signal **différent** de la cytosine non méthylée

### Avantages majeurs

- **Pas besoin de bisulfitation** (étape délicate évitée)
- **Détection directe** de la 5-méthylcytosine
- Lecture de **longs fragments** d’ADN (kb à Mb)
- Permet d’étudier d’autres modifications (5-hydroxyméthylcytosine, 6-méthyladénine)

### Limites

- Technologie encore peu répandue dans les laboratoires de routine
- Coût des consommables, expertise bio-informatique

> **Technologie d’avenir** pour l’étude du méthylome.


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p30_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p32_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p33_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-285%20Techniques%20danalyse%20de%20la%20methylation%20de%20lADN/p34_00.jpeg)


## Tableau de synthèse

| Étape | Détail |
|-------|--------|
| **Conversion bisulfite** | C non méthylée → U → T (PCR) ; C méthylée → C |
| **MS-PCR** | Amorces spécifiques M / U ; qualitatif |
| **Pyroséquençage** | **Quantitatif**, gold standard pour **MGMT** (5 CpG, seuil 8 %) |
| **MethyLight (qPCR)** | qPCR + sonde TaqMan, sensible |
| **Puces 450K / EPIC 850K** | **Pangénomique**, classification des **tumeurs cérébrales** |
| **NGS bisulfite (WGBS, RRBS)** | Pangénomique précis |
| **NGS nanopore** | **Sans bisulfitation**, détection directe — technologie d’avenir |

## Implications cliniques actuelles

| Indication | Technique recommandée |
|------------|------------------------|
| **MGMT en glioblastome** | **Pyroséquençage** (référence) |
| **Classification des tumeurs cérébrales** | **Puces de méthylation EPIC** (DKFZ classifier) |
| **MLH1** dans CCR sporadique MSI | MS-PCR ou pyroséquençage |
| **Méthylome global** (recherche) | Puces ou **NGS bisulfite** |
| **Méthylome + variants longs** (avenir) | **NGS nanopore** |

---

## 🔑 Points clés à retenir

1. **Conversion bisulfite** = **astuce chimique** transformant la méthylation en changement de séquence : **C non méthylée → U → T** ; **C méthylée → C**
2. Étape **délicate** : trop d’action = faux négatifs ; pas assez = faux positifs ; ~90 % d’ADN dégradé en 4 h
3. **MGMT** méthylé en glioblastome = **survie 21 mois** vs 15 mois sous protocole STUPP
4. La méthylation MGMT est probablement un marqueur de **phénotype hyperméthylateur global** plus qu’un strict marqueur de sensibilité au témozolomide
5. **Pyroséquençage** = **référence** pour MGMT : **5 CpG** dans l’exon 1, **seuil 8 %** de méthylation, **variable continue**
6. **Hétérogénéité spatiale** des glioblastomes → résultats variables selon la zone prélevée
7. Selon le **kit**, les CpG analysés diffèrent → vérifier la **validation clinique**
8. **Puces Illumina 450K/850K (EPIC)** : pangénomique, classification des tumeurs cérébrales (**DKFZ**), résultats **CGH-like** simultanés
9. Représentation **t-SNE** pour visualiser le clustering des méthylomes
10. **NGS nanopore** = technologie d’avenir : **détection directe** de la **5-méthylcytosine** **sans bisulfitation**, lecture de longs fragments
