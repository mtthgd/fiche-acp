---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_adn
  - électrophorèse_capillaire
  - LOH
  - perte_hétérozygotie
  - microsatellites
  - PCR
  - cartes_FTA
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Électrophorèse - Partie 3 — Analyse de fragments et perte d’hétérozygotie (LOH)

> Liens : [[16_160 Électrophorèse - Partie 1]] | [[16_160 Électrophorèse - Partie 2]] | [[16_115 Différents types de séquences du génome humain]] | [[16_180 Qualification et quantification des acides nucléiques]]

## Analyse de fragments — principe

Le **séquenceur capillaire** ne sert pas qu’au séquençage Sanger : il permet aussi l’**analyse de fragments**, c’est-à-dire la **détermination de la taille des fragments d’ADN à une base près**.

Application principale : la recherche de **perte d’hétérozygotie (LOH)**.


## Perte d’hétérozygotie (LOH) — définitions

**LOH = Loss Of Heterozygosity** = **perte d’un fragment chromosomique**.

Chaque autosome (et chromosomes sexuels) est présent en **2 copies** :
- 1 chromosome **paternel**
- 1 chromosome **maternel**
- Différents allèles permettent de distinguer les deux origines

| Situation | Statut | Commentaire |
|-----------|--------|-------------|
| 2 allèles distincts | **Hétérozygote** | Site **informatif** |
| Perte d’un fragment | "**LOH**" | Devenu **hémizygote** (1 seul allèle) |
| Vrai homozygote | 2 allèles identiques | Différent d’un hémizygote |

> Strictement, "LOH" est un abus de langage : on devrait parler de **perte d’un fragment chromosomique**. Le terme "LOH" se réfère à la **technique** employée pour le démontrer.

## Outil = code-barre allélique → microsatellites

On a besoin d’un "**code-barre**" pour distinguer l’allèle paternel de l’allèle maternel = la **séquence d’ADN**.

On utilise les **séquences microsatellites** :
- Répétitions de **2 à 5 paires de bases**
- La plus fréquente = **binôme CA** → "**CA-repeats**"
- Trouvés en moyenne **tous les ~25 kb**
- Polymorphisme : **nombre variable de répétitions** dans la population
- Réparties le long du chromosome → on peut **choisir** une zone microsatellite par locus à étudier

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p02_00.jpeg)


## Méthodologie pratique

### Étape 1 — Design des amorces PCR
- Amorces de part et d’autre du **CA-repeat**
- Produit final = ~**100-200 pb**
- Au moins une amorce **fluorescente** pour détection en électrophorèse capillaire

### Étape 2 — PCR sur ADN constitutionnel + ADN tumoral
Comparaison **OBLIGATOIRE** : tissu tumoral **vs** tissu normal (sang ou tissu adjacent).

### Étape 3 — Migration en électrophorèse capillaire
- Détection en fluorescence (ex : **SYBR Green** ou amorces marquées)
- Marqueur de taille interne (rouge) → "**spikes**" pour calibrer la taille

### Étape 4 — Lecture (logiciel **GeneScan**)
- Pics correspondent aux fragments PCR
- Calcul des **aires sous la courbe** = quantité d’ADN par taille



## Exemple pédagogique — étude de la zone 1p36.3

- Choix du microsatellite **D1S2795** (zone distale du bras court du chromosome 1)
- Amorces PCR pour fragments ~**200 pb**
- Patient porteur de **2 allèles différents** : **208 pb** et **216 pb** (site informatif)

| Échantillon | Profil capillaire | Interprétation |
|-------------|--------------------|----------------|
| **Sang (normal)** | 2 pics : 208 + 216 pb | **Hétérozygote** confirmé → site **informatif** |
| **Tumeur** | 1 seul pic prédominant + petit pic résiduel | **Perte de l’autre allèle** → **LOH en 1p36.3** |

> L’information ne concerne **que le locus étudié** (D1S2795), pas tout le bras chromosomique.



### Contre-exemple — conservation
Sang et tumeur présentent les **2 mêmes pics** d’intensité comparable → conservation de la zone chromosomique.


## Calcul du ratio — interprétation objective

Pour s’affranchir de la **contamination par tissu normal** (cellules endothéliales, inflammatoires) qui conserve l’allèle perdu dans la tumeur :

| Ratio (aires) | Conclusion |
|---------------|------------|
| **< 0,5** ou **> 1,5** | **LOH** (délétion d’un allèle) |
| Entre 0,5 et 1,5 | Pas de LOH significative |


## Pièges et astuces

### Profils irréguliers ("stutter")
- Sur gel d’agarose → 1 seule bande
- En capillaire → multiples petits pics autour du pic principal si :
  - Mauvaise *Taq polymérase*
  - **Temps d’élongation final** insuffisant
  - Certaines amorces propres au stutter
- Solutions : utiliser une **Taq haute performance** + temps d’élongation suffisant ; éviter les amorces "stuttering"

### Site non informatif
- Hasard : les 2 parents ont transmis le **même allèle** → **un seul pic** au sang = patient **homozygote** → **inutilisable**
- Solution : tester systématiquement **2-3 jeux d’amorces** par locus

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p09_00.jpeg)


## Adaptabilité de la technique

Si une publication identifie une LOH pronostique en (par exemple) **7q12** :
1. Consulter la **banque de données des microsatellites** (NCBI, Marshfield…)
2. Choisir un microsatellite dans la zone d’intérêt
3. **Designer** les amorces PCR
4. Commander des **amorces fluorescentes**
5. Passer les produits PCR en analyse de fragments
6. Analyser avec **GeneScan**

→ étude de LOH **rapide et peu coûteuse**.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p09_02.png)

## Limite incontournable — comparaison avec ADN normal

**Obligation absolue** : disposer du tissu **normal du patient**.

| Source d’ADN normal | Disponibilité |
|---------------------|----------------|
| Tissu normal **adjacent** à la tumeur | Idéal |
| **Sang** | Si pas de tissu normal disponible |
| Cas difficile : **tumeurs cérébrales** | Souvent pas de tissu normal accessible |

## Solution pratique — cartes FTA Whatman

Pour faciliter le **recueil et le transport** de l’ADN constitutionnel ou tumoral :

- **Buvard** spécial sur lequel on dépose :
  - Une **goutte de sang** du patient
  - Ou des **coupes cryostat** de tumeur
- **Emporte-pièces** → petits "**confettis**" (disques)
- **Transport à température ambiante** par la poste
- ADN **conservé plusieurs mois à années**
- PCR réalisée **directement au contact du disque** (sans extraction préalable d’ADN)

Étapes :
1. Dépôt de l’échantillon sur la carte FTA
2. Découpe de petits disques à l’emporte-pièce
3. **Lavage** dans tube Eppendorf
4. **Séchage**
5. **PCR directe** au contact du disque

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p10_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p11_00.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p11_04.png)


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p11_06.png)

---

## 🔑 Points clés à retenir

1. **Analyse de fragments** : variante du séquenceur capillaire pour mesurer la **taille à 1 pb près**
2. Application principale = recherche de **LOH** (perte d’hétérozygotie)
3. **LOH** = perte d’un fragment chromosomique → patient devient **hémizygote** au locus
4. Outil = **microsatellites** (souvent **CA-repeats**, ~tous les 25 kb), polymorphes dans la population
5. Comparaison **OBLIGATOIRE** : ADN **tumoral** vs ADN **constitutionnel**
6. Produits PCR ~ **100-200 pb**, amorces **fluorescentes**, lecture par **GeneScan**
7. **Marqueurs de taille interne (spikes)** → calibration de la taille
8. Calcul de l’**aire sous la courbe** → ratio **< 0,5 ou > 1,5** = LOH
9. **Site non informatif** si patient homozygote au locus → utiliser **2-3 amorces** par locus
10. Profils irréguliers (**stutter**) = problème de Taq, élongation, ou amorce
11. Information **locus-spécifique** (pas tout le chromosome)
12. **Cartes FTA Whatman** : conservation/transport ADN à température ambiante, PCR directe sur le disque
