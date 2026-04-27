---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - connaissances_fondamentales
  - réparation_ADN
  - mismatch_repair
  - BRCA
  - PARP
  - létalité_synthétique
  - HRD
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Réparation des lésions de l’ADN

> Liens : [[16_210 Oncogènes et gènes suppresseurs de tumeurs]] | [[16_220 Cycle cellulaire et cancer]] | [[16_270 Instabilité génétique]] | [[16_280 Modifications épigénétiques - Méthylation de l'ADN et histones]] | [[16_770 Notions de cancers familiaux]] | [[16_1035 Statut MSI en onco-immunologie]]

## Objectifs

- Connaître les **types de lésions** de l’ADN
- Connaître les **systèmes de réparation** correspondants
- Comprendre l’**implication dans le cycle cellulaire**
- Connaître les **anomalies des systèmes de réparation** dans les tumeurs et leurs conséquences thérapeutiques

## Rappels — structure de l’ADN

L’ADN est constitué de **nucléotides** = désoxyribose + phosphate + base azotée (**A, T, C, G**).
- Liaisons **covalentes** entre désoxyribose et phosphate (squelette)
- Liaisons **hydrogène** entre les bases : **A=T** (2 liaisons), **C≡G** (3 liaisons)
- Forme la double hélice



## Sources de dommages de l’ADN

| Origine | Exemples |
|---------|----------|
| **Endogène** | **Espèces réactives de l’oxygène (ROS)** issues de la respiration, métabolites, **erreurs de réplication** par les polymérases |
| **Exogène** | **UV**, fumée de cigarette, agents chimiques, agents alkylants |
| **Thérapeutique** | **Chimiothérapie**, **radiothérapie** (action volontaire pour induire des dommages) |

> Jusqu’à **10¹⁸ lésions de l’ADN par jour** en physiologie → nécessité de systèmes de réparation efficaces.



## Types de lésions et systèmes de réparation correspondants

> Notion clé : **un même agent peut entraîner plusieurs types de lésions**, qui sollicitent chacun le système de réparation adapté.

| Type de lésion | Agent causal | Système de réparation |
|-----------------|--------------|------------------------|
| **Bases oxydées**, sites abasiques | Irradiations, agents alkylants, ROS | **BER** (Base Excision Repair) — réversion directe |
| **Adduits volumineux** (dimères de thymine, photoproduits) | **UV** | **NER** (Nucleotide Excision Repair) |
| **Mésappariements**, insertions/délétions courtes | Erreurs de réplication | **MMR** (Mismatch Repair) |
| **Cassures double brin** | Irradiations, agents pontants | **HR** (Recombinaison Homologue) ou **NHEJ** (Non-Homologous End Joining) |
| **Adduits inter-brins** | Agents pontants (cisplatine, mitomycine) | HR + NER + Fanconi |

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-260%20%20R%C3%A9paration%20des%20l%C3%A9sions%20de%20lADN/p05_00.jpeg)


## 1. Réparation par excision de base (BER)

Cible : **bases oxydées** ou anormales (ex. cytosine désaminée → uracile, qui ne peut pas s’apparier avec G).

### Étapes

1. **Glycosylase** spécifique → enlève la base anormale (création d’un site abasique)
2. **AP-endonucléase** (APE1) → coupe le squelette phosphodiester
3. **PARP1** : détecte les cassures, recrute les acteurs
4. **ADN polymérase β** → synthèse du nucléotide manquant
5. **ADN ligase** → relie les brins

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-260%20%20R%C3%A9paration%20des%20l%C3%A9sions%20de%20lADN/p07_00.jpeg)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-260%20%20R%C3%A9paration%20des%20l%C3%A9sions%20de%20lADN/p08_00.jpeg)

## 2. Réparation par excision de nucléotides (NER)

Cible : **adduits volumineux** (dimères de thymines induits par les UV → distorsion de la molécule d’ADN).

### Étapes

1. **Reconnaissance** de la distorsion (XPC-RAD23B, XPA…)
2. **Nucléases** (XPF-ERCC1, XPG) → excision d’un fragment de 24-32 nucléotides
3. **ADN polymérase δ/ε** → synthèse d’un nouveau brin
4. **ADN ligase** → ligature

> Déficit = **Xeroderma pigmentosum**, **syndrome de Cockayne**, trichothiodystrophie.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-260%20%20R%C3%A9paration%20des%20l%C3%A9sions%20de%20lADN/p09_00.jpeg)


## 3. Réparation des mésappariements (Mismatch Repair, MMR)

Cible : **mésappariements de base** (ex. G:T) et **boucles** d’insertion/délétion (séquences microsatellitaires).

### Acteurs et étapes

1. Reconnaissance du mésappariement par l’hétérodimère **MSH2 / MSH6** (ou **MSH2 / MSH3** pour les boucles)
2. Recrutement de **MLH1 / PMS2**
3. Le tétramère active une **endonucléase** à distance → digestion du brin contenant l’erreur
4. **RPA** recouvre le simple-brin
5. **ADN polymérase δ** → synthèse
6. **ADN ligase** → restauration de la continuité

### Conséquences cliniques

- Déficit MMR (**dMMR**) → **instabilité microsatellitaire (MSI)**
- **Syndrome de Lynch** (HNPCC) : mutation germinale d’**MLH1, MSH2, MSH6, PMS2** ou délétion **EPCAM**
- Cancers colorectaux MSI **sporadiques** : par **méthylation du promoteur de MLH1** (souvent associée à **BRAF V600E** muté)
- **Charge mutationnelle élevée** → **excellente réponse à l’immunothérapie** (anti-PD1/PD-L1)



## 4. Réparation des cassures double brin (DSB)

Lésions **les plus létales** pour la cellule. Causes : **irradiations**, agents pontants, effondrement de fourches de réplication.

### Deux mécanismes

| Système | Fidélité | Phase du cycle | Principe |
|---------|----------|----------------|----------|
| **NHEJ** (Non-Homologous End Joining) | **Infidèle** (perte/insertion de bases) | **Tout le cycle** | Ligature directe des extrémités |
| **HR** (Recombinaison Homologue) | **Fidèle** | **S et G2 uniquement** | Utilise la chromatide sœur comme matrice |

> La cellule **préfère NHEJ** (plus rapide, disponible à toute phase).

### A. NHEJ — étapes

1. Hétérodimère **Ku70-Ku80** se lie aux extrémités
2. Recrutement d’**Artemis** (préparation des extrémités)
3. **DNA-PKcs** activé
4. Recrutement du complexe **XRCC4 + ADN ligase IV**
5. Ligature

### B. Recombinaison homologue (HR) — étapes

1. **Résection** d’un brin par le complexe **MRN (MRE11-RAD50-NBS1) + BRCA1 + CTIP**
2. Extension par **EXO1** → extrémités sortantes simple-brin
3. **RPA** recouvre le simple-brin
4. **BRCA2** déplace **RPA** et charge **RAD51**
5. **Filament de RAD51** → invasion du brin lésé dans la séquence homologue intacte
6. Synthèse d’un nouveau brin par polymérase
7. Résolution → conversion génique ± **crossing-over**

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-260%20%20R%C3%A9paration%20des%20l%C3%A9sions%20de%20lADN/p13_00.jpeg)


## Coordination réparation / cycle cellulaire — DDR

```
Lésion ADN
   ↓
Senseurs : MRN, ATM, ATR
   ↓
Transducteurs : CHK1, CHK2
   ↓
Effecteurs : CDC25, p53
   ↓
Décision selon l'intensité :
  - Arrêt du cycle (G1/S, intra-S, G2/M)
  - Réparation
  - Apoptose (si dommages excessifs)
```


## Implications cliniques

### A. Cancer du côlon — déficit MMR

- **Syndrome de Lynch** : recherche systématique du **statut MMR** par **IHC** (MLH1, MSH2, MSH6, PMS2) ± **PCR Pentaplex** (BAT26, BAT25, NR21, NR24, NR27)
- **dMMR / MSI** → **forte charge mutationnelle** → **immunothérapie** (anti-PD1 : pembrolizumab, nivolumab) très efficace
- Voir [[16_1035 Statut MSI en onco-immunologie]]

### B. Cancer du sein / ovaire — létalité synthétique

#### Concept de létalité synthétique

Deux gènes/voies sont en **redondance** : la perte d’**un seul** est tolérée, la perte des **deux** est létale.

#### Application : BRCA + PARP

| Cellule | BER (PARP1) | HR (BRCA) | Réparation |
|---------|:-----------:|:---------:|:----------:|
| **Normale** | OK | OK | ADN réparé |
| **BRCA muté** | OK | KO | ADN réparé (par BER) |
| **Inhibiteur de PARP** | KO | OK | ADN réparé (par HR) |
| **BRCA muté + inhibiteur PARP** | **KO** | **KO** | **MORT cellulaire** |

Les inhibiteurs de PARP (**olaparib, niraparib, rucaparib**) sont actifs dans les tumeurs avec **mutation BRCA1/2** ou **déficit de la recombinaison homologue (HRD)** :

- **Cancer ovarien** (BRCA muté germinal/somatique, HRD)
- **Cancer du sein triple négatif BRCA muté**
- **Cancer de la prostate** métastatique castro-résistant
- **Adénocarcinome pancréatique** BRCA muté

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/connaissances-fondamentales/16-260%20%20R%C3%A9paration%20des%20l%C3%A9sions%20de%20lADN/p16_00.jpeg)

## Syndromes héréditaires liés à des défauts de réparation

| Syndrome | Gène(s) | Cancers principaux |
|----------|---------|---------------------|
| **Lynch (HNPCC)** | **MLH1, MSH2, MSH6, PMS2, EPCAM** | Colon, endomètre, voies urinaires, ovaire, gastrique |
| **HBOC** (sein/ovaire familial) | **BRCA1, BRCA2** | Sein, ovaire, prostate, pancréas |
| **Xeroderma pigmentosum** | XPA-XPG, ERCC | Cancers cutanés UV-induits |
| **Anémie de Fanconi** | FANC (15+ gènes) | Leucémies, ORL, gynéco |
| **Ataxie-télangiectasie** | **ATM** | Lymphomes, sein |
| **Syndrome de Bloom** | BLM | Leucémies, lymphomes |
| **Syndrome de Li-Fraumeni** | TP53 | Spectre large (sarcomes, sein, surrénale, cerveau) |
| **MUTYH-associated polyposis** | MUTYH (BER) | Colon |

## Synthèse

| Lésion | Système | Acteurs majeurs | Pathologie associée |
|--------|---------|-----------------|----------------------|
| Base oxydée | **BER** | Glycosylase, **PARP**, ADN pol β | MAP (MUTYH) |
| Adduit UV | **NER** | XP-A à XP-G, ERCC | Xeroderma |
| Mésappariement | **MMR** | **MSH2, MSH6, MLH1, PMS2** | **Lynch** |
| DSB | **NHEJ** (infidèle) | Ku70/80, DNA-PK, XRCC4, lig IV | SCID, lymphomes |
| DSB | **HR** (fidèle, S/G2) | **MRN, BRCA1/2, RAD51** | **HBOC** |

---

## 🔑 Points clés à retenir

1. **10¹⁸ lésions ADN/jour** en physiologie ; un même agent peut induire plusieurs types de lésions
2. **5 systèmes** de réparation : **BER, NER, MMR, NHEJ, HR**
3. **BER** : bases oxydées, dépend de **PARP1** et ADN pol β
4. **NER** : adduits volumineux (UV) ; déficit = **Xeroderma pigmentosum**
5. **MMR** : mésappariements ; acteurs = **MSH2/MSH6 + MLH1/PMS2** ; déficit = **Lynch / MSI**
6. **NHEJ** : infidèle, tout au long du cycle ; **Ku70/Ku80, DNA-PK, XRCC4, ligase IV**
7. **HR** : fidèle, en **phase S/G2** ; nécessite chromatide sœur ; acteurs = **MRN, BRCA1, BRCA2, RAD51**
8. La **DDR** coordonne réparation et cycle cellulaire via **ATM/ATR → CHK1/2 → p53/CDC25**
9. Tumeurs **MSI / dMMR** = **forte charge mutationnelle** → excellente réponse à l’**immunothérapie**
10. **Létalité synthétique BRCA + inhibiteur PARP** : **olaparib, niraparib, rucaparib** dans cancers BRCA-mutés (ovaire, sein, prostate, pancréas)
11. Indications PARP étendues aux tumeurs **HRD** (déficit de la recombinaison homologue) au-delà de BRCA
12. Plusieurs **syndromes héréditaires** par défaut de réparation : Lynch, HBOC, Fanconi, Xeroderma, AT, Li-Fraumeni
