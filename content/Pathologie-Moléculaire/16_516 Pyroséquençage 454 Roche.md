---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - ngs
  - 2G_séquençage
  - pyroséquençage_454
  - emPCR
  - bille
  - PPi
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Pyroséquençage 454 Roche

> Liens : [[16_510 Principes du séquençage massif parallèle]] | [[16_515 Séquençage 2G - points communs]] | [[16_517 Séquençage Ion Torrent]] | [[16_518 Séquençage Illumina]] | [[16_520 Séquençage 2G - capture et amplicons]]

## Principe général

Première plate-forme de **séquençage de 2ᵉ génération** historiquement (commercialisée par **Roche/454 Life Sciences**, arrêt commercial 2016). Elle fut le **premier exemple d’amplification clonale sur bille par PCR en émulsion (emPCR)** suivie d’une détection par **chimioluminescence**.

Détection : la libération de **pyrophosphate (PPi)** lors de l’incorporation d’un nucléotide est convertie en **flash lumineux** par une cascade enzymatique **sulfurylase + luciférase**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p02_00.jpeg)

## Étapes techniques

### Étape 1 — Préparation de la librairie
- Échantillon de départ : **ADN génomique, cDNA, sscDNA** ou **produit de PCR**
- **Fragmentation** de l’ADN (~700 pb)
- **Ligation** d’**adaptateurs A et B distincts** à chaque extrémité

### Étape 2 — Fixation sur bille (emPCR)
- Billes recouvertes d’oligos complémentaires de l’**adaptateur A**
- **Dilution stœchiométrique** : **1 fragment d’ADN par bille**
- **Émulsion eau-dans-huile** (« vinaigrette ») : chaque bille + 1 fragment encapsulés dans une **microgoutte aqueuse** contenant Taq polymérase, amorces, dNTP
- **PCR en émulsion** : amplification clonale dans la microgoutte → bille « **cheveux longs** » couverte de **milliers de copies identiques** d’une seule molécule de départ

### Étape 3 — Distribution dans les puits
- Casser l’émulsion, déposer les billes sur une **plaque de fibre optique** (plate **PicoTiterPlate**)
- **Une bille par puits** (alvéole)
- Ajout de **billes secondaires d’emballage** contenant **sulfurylase + luciférase**

### Étape 4 — Cycle de séquençage
À chaque cycle, **un seul nucléotide** (A, puis T, puis C, puis G…) est introduit successivement dans tous les puits :
- Si la polymérase l’incorpore → **PPi libéré** → **sulfurylase** convertit PPi + APS en **ATP** → **luciférase + luciférine** → **émission de lumière**
- Caméra haute résolution lit **simultanément** tous les puits → cartographie XY des flashs
- Si non incorporé → pas de lumière → l’opérateur sait que le nucléotide n’est pas en position

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p04_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p06_00.png)

| Étape | Détail | Outil/Plate-forme |
|---|---|---|
| Fragmentation | ~700 pb | Sonication |
| Adaptateurs | A et B distincts | Ligation |
| Amplification | **1 bille = 1 fragment**, **emPCR** | Émulsion huile/eau |
| Distribution | 1 bille / puits + billes packing | **PicoTiterPlate** |
| Détection | **Lumière** (PPi → ATP → luciférase) | Caméra haute définition |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/ngs/16-516%20517%20518%20%20NGS%202eme%20generation%20au%20coeur%20des%20machines/p07_00.jpeg)

## Spécifications / Métriques

| Métrique | Valeur 454 |
|---|---|
| Longueur de read | **~700 pb** (la plus longue parmi les 2G) |
| Reads par run | ~1 million |
| Débit total | ~700 Mb / run |
| Précision | ~99 % sur bases isolées |
| Temps d’un run | ~10-23 h |
| Format de sortie | **SFF** puis converti en **FASTQ** |

## Indications / Applications

- **Métagénomique** (longs reads pour identifier des espèces bactériennes)
- **Études de variants rares** sur amplicons
- **Re-séquençage** ciblé HLA, immunoglobulines
- Plate-forme **historique** — désormais supplantée par **Illumina** et **Ion Torrent**

## Avantages / Limites

| Avantages | Limites |
|---|---|
| **Reads les plus longs** des plates-formes 2G (~700 pb) | **Erreur sur les homopolymères** (≥ 6 bases identiques) — comme Ion Torrent |
| Chimie naturelle (nucléotides non modifiés) | Coût élevé par base |
| 1ʳᵉ technologie 2G commercialisée (preuve de concept emPCR) | **Arrêt commercial Roche en 2016** |
| Détection digitale fiable (lumière) | Préparation emPCR longue et délicate |

---

## 🔑 Points clés à retenir

1. **454 Roche** = 1ʳᵉ plate-forme **NGS 2G** historique, **arrêt commercial 2016**.
2. Détection par **pyrophosphate (PPi) → sulfurylase + luciférase → lumière**.
3. Amplification clonale par **PCR en émulsion (emPCR)** : 1 bille = 1 fragment dans 1 microgoutte huile/eau.
4. Distribution **1 bille / 1 puits** sur **PicoTiterPlate** (plaque fibre optique).
5. Cycle séquentiel **A → T → C → G**, présentés un à un.
6. **Reads ~700 pb** : les plus longs parmi les 2G.
7. Caméra **haute définition** lit tous les puits simultanément (XY).
8. **Limite majeure** : erreur sur les **homopolymères** (≥ 6 bases identiques).
9. Chimie **naturelle** (pas de nucléotides fluorescents).
10. Aujourd’hui supplanté par **Illumina** (fluorescence) et **Ion Torrent** (H+).
