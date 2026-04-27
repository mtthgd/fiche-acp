---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - extraction_ffpe
  - qPCR
  - qualification_ADN
  - HPRT
  - albumine
  - TBP
  - inhibiteurs_PCR
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Validation de la qualité de l’échantillon par qPCR

> Liens : [[16_351 Effet de la fixation sur les acides nucléiques]] | [[16_355 Principes de microdissection tissulaire]] | [[16_310 Principes de la qPCR]] | [[16_320 PCR digitale - principe et applications]]

## Principe / Définition

La **qPCR** (PCR en temps réel quantitative) est la **quatrième méthode** (avec spectrométrie, fluorométrie, électrophorèse capillaire) pour **qualifier** et **quantifier** un acide nucléique.

Elle évalue trois paramètres clés :
1. **Intégrité / état de dégradation** de l’ADN
2. **Quantité / concentration** de la cible
3. **Présence d’inhibiteurs de PCR**


## Rappels sur la qPCR temps réel

- **Thermocycleur** couplé à des canaux de **lecture de fluorescence**
- Suivi en temps réel de l’amplification : trois phases **initiation → exponentielle → plateau**
- À efficacité = 1, des cibles diluées au **1/10** sont distantes de **3,33 cycles** (par exemple 10 000 / 1 000 / 100 / 1 copies)



![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-365 Validation de la qualité de léchantillon par  q PCR/p04_00.jpeg]]

## Évaluation de l’intégrité de l’ADN

### ADN intègre
- Cible non fragmentée → amorces hybrident correctement → amplification normale
- Exemple : 100 copies → CT = **21**

### ADN partiellement dégradé
- Présence de **trous** dans la matrice
- Certaines amorces n’hybrident pas, la polymérase rencontre des trous → **abandon**
- Seules quelques copies amplifient (10 au lieu de 100) → CT décalé : **CT = 25**

### ADN totalement dégradé
- Plus de cible intègre
- Amplification absente ou **non spécifique > CT 36–38**
- Profil **plat**





## Quantification absolue par gamme étalon

- Gamme de cibles à concentrations **connues** (par exemple 1 / 10 / 50 ng/µL d’**HPRT** ou **β-actine**)
- Établissement d’une **courbe étalon** : CT = f(log [ADN])
- Échantillon inconnu : amplifié dans les mêmes conditions → CT mesuré → report sur courbe → concentration



![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-365 Validation de la qualité de léchantillon par  q PCR/p11_00.jpeg]]

## Détection des inhibiteurs de PCR

| Inhibiteur | Origine |
|------------|---------|
| **SDS** | Détergent (purification) |
| **Éthanol / isopropanol** | Lavages d’extraction |
| **EDTA** | Tubes de prélèvement, **chélate Mg²⁺** |
| **Héparine** | Tubes de prélèvement sang |

**Mécanisme** : les inhibiteurs collent au gène ou chélatent le **MgCl₂** (cofacteur de la polymérase) → amplification **décalée** ou **absente**.

**Solution** : **diluer** l’échantillon → dilue aussi les inhibiteurs → CT plus précoce et exploitable.




## Protocole de qualification par 3 amplicons (retour d’expérience)

| Couple d’amorces | Taille amplicon (pb) |
|------------------|----------------------|
| **HPRT** | **63 pb** |
| **Albumine** | **160 pb** |
| **TBP** | **295 pb** |

### Principe
- Run unique avec les **3 cibles** sur :
  - **6 ng** d’ADN génomique de **cellules témoin** standardisées (HT29, intègre, aliquoté laboratoire)
  - **6 ng** d’ADN de l’échantillon à qualifier
- **ADN intègre** → amplification normale des **3 amplicons** (petit, moyen, grand)
- **ADN dégradé** → seul le petit amplicon (HPRT) amplifie ; le grand (TBP) sort très tardivement ou pas du tout



## Calcul du Δ CT (delta CT)

**Δ CT = CT échantillon − CT témoin HT29** pour chaque amplicon.

| Δ CT TBP | Interprétation |
|----------|----------------|
| **< 6** | ADN exploitable en NGS |
| **≥ 6** (par exemple 6,5) | ADN dégradé → **résultats artefactuels en NGS** |

### Indicateurs NGS d’artefact (ADN dégradé)
- Nombre de variants > **20**
- Pourcentage de transitions **C>T** entre **25 et 30 %** (selon le panel utilisé)
- Exemple problématique : **61 variants** + **72 % de transitions C>T** = ininterprétable


## Avantages / Limites de la qPCR de qualification

| Avantages | Limites |
|-----------|---------|
| **Précise** | Reflet d’**une cible** (HPRT, albumine, TBP) — pas l’ensemble de l’ADN |
| Détecte les **inhibiteurs** | Non exhaustive |
| Petits volumes (ng) | Multiplier les cibles pour mieux refléter l’état général |
| Triplet de tailles → indicateur d’**intégrité** | |

## Pièges / Contrôles qualité

- **Toujours** inclure un témoin standardisé (par exemple **HT29**) **aliquoté**
- Comparer en **Δ CT**, pas en CT absolu
- Cohérence entre **3 amplicons croissants** = signature d’intégrité
- En cas d’inhibiteurs suspectés → **dilution sériée** de l’échantillon
- Si Δ CT TBP ≥ 6 → **ne pas lancer le NGS** ou **réextraire**

## 🔑 Points clés à retenir

1. La qPCR est la **4e méthode** de qualification (après spectrométrie, fluorométrie, électrophorèse).
2. Évalue **intégrité**, **quantité** et présence d’**inhibiteurs** d’ADN.
3. Cibles de qualification : **HPRT 63 pb / Albumine 160 pb / TBP 295 pb** (taille croissante).
4. **Δ CT échantillon vs témoin HT29** = indicateur d’intégrité.
5. **Δ CT TBP ≥ 6** → ADN dégradé, **artefacts NGS** majeurs (nb variants ↑, transitions C>T ↑).
6. Gamme étalon **HPRT** ou **β-actine** pour quantification absolue.
7. Inhibiteurs courants : **SDS, éthanol, isopropanol, EDTA, héparine** → solution = **dilution**.
8. ADN totalement dégradé : amplification non spécifique **> CT 36–38** ou profil plat.
9. **Aucune technique unique n’est exhaustive** : combiner Nanodrop + Qubit + qPCR + Bioanalyzer pour décision NGS.
10. Toujours **standardiser** les témoins (aliquots) et exprimer les résultats en **Δ CT**.
