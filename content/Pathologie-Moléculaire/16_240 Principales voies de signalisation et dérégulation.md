---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - connaissances_fondamentales
  - voies_signalisation
  - MAPK
  - PI3K_AKT
  - WNT
  - Hedgehog
  - RAS
  - BRAF
  - EGFR
  - thérapies_ciblées
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Principales voies de signalisation et dérégulation

> Liens : [[16_210 Oncogènes et gènes suppresseurs de tumeurs]] | [[16_220 Cycle cellulaire et cancer]] | [[16_230 Notions de transduction du signal]] | [[16_770 Notions de cancers familiaux]] | [[16_1035 Statut MSI en onco-immunologie]]

## Cadre conceptuel — communication cellulaire et cancer

Un ligand active des récepteurs membranaires qui propagent le signal via des cascades intracellulaires modifiant des protéines existantes ou induisant la transcription de gènes cibles → modification du comportement cellulaire.

### Les 10 « Hallmarks of cancer » (Hanahan & Weinberg)

Toutes ces caractéristiques relèvent d’**anomalies de communication et de transduction** :

1. Autonomie aux signaux de prolifération
2. Insensibilité aux signaux antiprolifératifs
3. Résistance à l’**apoptose**
4. Réplication illimitée (télomères)
5. **Angiogénèse** soutenue
6. **Invasion** et métastase
7. Reprogrammation du **métabolisme** énergétique
8. Échappement à la **destruction immunitaire**
9. **Inflammation** pro-tumorale
10. **Instabilité génomique** et mutations



## Activation oncogénique d’un facteur de signalisation

Un proto-oncogène devient oncogène par mutation **d’un seul allèle** par 3 mécanismes principaux :

| Mécanisme | Conséquence protéique |
|-----------|------------------------|
| **Mutation ponctuelle** activatrice | Quantité normale, **activité suractivée** |
| **Réarrangement chromosomique** | Surexpression (promoteur fort) ou **fusion** activatrice |
| **Amplification** | Quantité **surexprimée**, activité normale |

→ **Addiction oncogénique** : la tumeur devient **dépendante** de l’oncogène activé. Le cibler peut **stopper la croissance**.



## Voie 1 — RAS / RAF / MEK / ERK (MAPK)

Voie majeure déclenchée par les **RTK**, conduisant à des modifications de protéines existantes ou à l’induction de gènes cibles.

### Acteurs et cascade

```
RTK activé (ex. EGFR-P)
   ↓ recrutement de GRB2 (SH2 sur P-tyrosine, SH3 sur proline)
SOS (GEF) recruté
   ↓ échange GDP → GTP sur RAS
RAS-GTP (actif, ancré à la membrane par farnésylation)
   ↓ phosphoryle
RAF (kinase)
   ↓ phosphoryle
MEK (kinase)
   ↓ phosphoryle
ERK (kinase)
   ↓ effecteurs transcriptionnels nucléaires
Croissance, division, migration
```


![[assets/pathologie-moleculaire/connaissances-fondamentales/16-240 Principales voies de signalisation et dérégulation v2/p07_00.jpeg]]



### Dérégulations oncogéniques de la voie MAPK

Chaque facteur peut devenir oncogène et est ciblable.

#### A. RTK : EGFR — exemples paradigmatiques

| Anomalie EGFR | Conséquence | Tumeur | Thérapie ciblée |
|----------------|-------------|--------|------------------|
| **Mutation activatrice** du domaine TK (L858R, exon 19 del) | Conformation modifiée fixant l’ATP en permanence | **Adénocarcinome bronchique** | **ITK** (gefitinib, erlotinib, **osimertinib** 3ᵉ génération) |
| **Amplification** | Surexpression du récepteur | Tumeurs cérébrales | **Dépatuxizumab** (anticorps) |
| **Délétion exons 2-7** (EGFRvIII) | Activation constitutive ligand-indépendante | Glioblastome | Immunothérapie / CAR-T cells |
| Récepteur normal (sans mutation) | — | **Colorectal métastatique RAS sauvage** | Anti-EGFR (**cétuximab**, **panitumumab**) |








#### B. Autres RTK ciblables

| RTK | Anomalie | Tumeur | Cible |
|-----|----------|--------|-------|
| **ALK** | Translocation/fusion | CBNPC | Crizotinib, alectinib, lorlatinib |
| **ROS1** | Translocation | CBNPC | Crizotinib |
| **KIT** | Mutation activatrice | **GIST**, leucémies, mastocytoses | **Imatinib** |
| **HER2** | Amplification | **Sein**, estomac, CBNPC | **Trastuzumab** |
| **NTRK1/2/3** | Fusion | Sarcomes, sécrétoire mammaire | Larotrectinib |
| **RET** | Mutation/fusion | CMT, CBNPC | Selpercatinib |
| **MET** | Amplification, mutation exon 14 | CBNPC | Capmatinib |



#### C. RAS — la GTPase majeure

- À l’état normal, RAS-GTP est hydrolysé par sa **GAP** → RAS-GDP (off)
- **Mutation** (ex. **G12C, G12D, G13D, Q61** sur **KRAS**, **NRAS**, **HRAS**) : **incapable d’hydrolyser le GTP** → **activation permanente**

##### Conséquences cliniques

- En **CCR métastatique** : la mutation **RAS** rend les **anti-EGFR inefficaces** (résistance par activation aval)
- Cibler RAS : longtemps « indrugable »
  - **Sotorasib, adagrasib** : inhibiteurs spécifiques de **KRAS G12C** (CBNPC, CCR)
  - **Inhibiteurs de farnésyltransférase** : empêchent l’ancrage membranaire (essais cliniques)





#### D. BRAF / MEK

- **BRAF V600E** : mutation activatrice classique du **mélanome**, mais aussi cancer thyroïdien papillaire, leucémie à tricholeucocytes, **CBNPC**, CCR
- **Bithérapie ciblée** : inhibiteur de BRAF + inhibiteur de MEK → blocage en deux points de la voie
  - **Vémurafénib + cobimétinib**
  - **Dabrafénib + tramétinib**



## Voie 2 — PI3K / AKT / mTOR

### Acteurs

```
RTK actif → PI3K
   ↓
PIP2 → PIP3 (inhibé par PTEN, anti-oncogène)
   ↓
PDK1 → AKT (phosphorylé)
   ↓
- mTOR → traduction
- inhibition NF-κB → apoptose
- BAD, BAX → bloque l’apoptose
- modulation du cycle cellulaire et du métabolisme
```




### Dérégulations / cibles thérapeutiques

| Acteur | Altération | Indications |
|--------|------------|-------------|
| **PIK3CA** | Mutation activatrice | **Cancer du sein** (essais avec **alpélisib**, buparlisib) |
| **PTEN** | Perte de fonction (anti-oncogène) | Glioblastome, prostate, endomètre |
| **AKT** | Activation | Inhibiteurs AKT (essais) |
| **mTOR** | Activation | **Évérolimus, temsirolimus** (rein, sein, NET) |




## Voie 3 — WNT / β-caténine

### Conditions physiologiques

- WNT est lié à des **inhibiteurs** (DKK, sFRP) → ne se fixe pas sur **Frizzled (FZ)**
- La **β-caténine** cytoplasmique est captée par un **complexe de destruction** (APC + axine + GSK3β + CK1) → ubiquitinylation → dégradation
- → expression normale des gènes du développement et différenciation

### Conditions pathologiques

- WNT se fixe sur **FZ + LRP** → recrutement des composants du complexe de destruction → **β-caténine non dégradée**
- β-caténine **transloque** dans le noyau → fixation à **TCF/LEF** → transcription de gènes (MYC, cycline D1) → tumorigénèse

### Altérations en cancérologie

| Tumeur | Mécanisme |
|--------|-----------|
| **Cancer colorectal** | **APC** muté (FAP, sporadique) +++ |
| Hépatoblastome, hépatocarcinome | **CTNNB1** muté (gain de fonction de la β-caténine) |
| Tumeurs desmoïdes | **CTNNB1** muté |
| Médulloblastome WNT | Activation WNT |
| Cancer endométrial | β-caténine, PIK3CA, PTEN |

### Cibles potentielles

- Anticorps anti-WNT
- Inhibiteurs des porcupine (PORCN)
- Inhibiteurs de tankyrase


![[assets/pathologie-moleculaire/connaissances-fondamentales/16-240 Principales voies de signalisation et dérégulation v2/p33_00.png]]



## Voie 4 — Sonic Hedgehog (Hh)

### Conditions physiologiques

- **PTCH** (récepteur) **non lié** au ligand SHH → exerce un effet **répresseur** sur **SMO** (sur des vésicules intracytoplasmiques)
- Les facteurs de transcription **GLI1/2/3** sont fixés par des protéines → dégradation par le protéasome ou répression transcriptionnelle

### Conditions pathologiques

- **SHH se fixe sur PTCH + co-récepteurs** → lève l’inhibition de **SMO**
- SMO transloque à la membrane → libère GLI1/2 → translocation nucléaire → **transcription** des gènes de prolifération, survie, **angiogénèse**

### Altérations en cancérologie

| Tumeur / pathologie | Mécanisme |
|---------------------|-----------|
| **Carcinomes basocellulaires** | Mutation **PTCH** (perte de fonction) ; activation SMO |
| **Médulloblastome SHH** | Activation de la voie |
| **Syndrome de Gorlin** | Mutation germinale **PTCH1** |
| Spina bifida | Anomalies du développement |
| Glioblastome, mélanome, pancréas, sein, prostate | Implication de la voie |
| Cellules souches tumorales gliales | Auto-renouvellement |

### Cibles thérapeutiques

- Récepteurs solubles anti-Hh
- **Cyclopamine** et **vismodégib** (antagonistes de SMO)
- Inhibiteurs de GLI





## Autres voies impliquées en oncogénèse

| Voie | Implication |
|------|-------------|
| **NOTCH** | Hématologie (LAL-T : NOTCH1), CBNPC, sein triple négatif |
| **HIPPO / YAP-TAZ** | Mésothéliome, schwannome (NF2), HCC |
| **NF-κB** | Lymphomes B, anti-apoptotique |
| **JAK / STAT** | **NMP** (JAK2 V617F), leucémies, lymphomes |
| **TGF-β** | Rôle dual (suppresseur précoce, promoteur tardif) |
| **p38 / JNK MAPK** | Réponse au stress |





## Médecine personnalisée

Les voies sont **interconnectées** : cross-activation possible (intégrines, RCPG…), redondance des cascades, ce qui crée des **mécanismes de résistance** par utilisation de voies alternatives.

→ Importance d’**identifier le mécanisme oncogénique** d’une tumeur pour cibler la bonne addiction. C’est le principe de la **médecine personnalisée**.




## Tableau de synthèse — voies / altérations / thérapies

| Voie | Acteur clé | Altération | Tumeur(s) | Thérapie ciblée |
|------|------------|------------|-----------|------------------|
| MAPK | **EGFR** | Mutation L858R, exon 19 del | CBNPC | Gefitinib, **osimertinib** |
| MAPK | **HER2** | Amplification | Sein, estomac | **Trastuzumab** |
| MAPK | **ALK** | Fusion EML4-ALK | CBNPC | Alectinib |
| MAPK | **KIT** | Mutation | **GIST** | **Imatinib** |
| MAPK | **KRAS G12C** | Mutation | CBNPC, CCR | **Sotorasib** |
| MAPK | **BRAF V600E** | Mutation | Mélanome, CBNPC, LCT | **Dabrafénib + tramétinib** |
| PI3K | **PIK3CA** | Mutation | Sein RH+ | **Alpélisib** |
| PI3K | **mTOR** | Activation | Rein, NET, sein | Évérolimus |
| WNT | **APC** / **CTNNB1** | Mutation | CCR / hépato | (essais) |
| Hh | **PTCH** / **SMO** | Mutation / activation | CBC, médulloblastome | **Vismodégib** |

---

## 🔑 Points clés à retenir

1. **10 hallmarks du cancer** = anomalies de communication et de transduction du signal
2. Un proto-oncogène devient oncogène par **mutation ponctuelle**, **réarrangement** ou **amplification** → notion d’**addiction oncogénique**
3. **Voie MAPK** : RTK → SOS → **RAS-GTP** → RAF → MEK → ERK → transcription
4. **EGFR** muté = adénoK bronchique → **ITK** ; EGFR amplifié → anti-EGFR ; CCR sans mutation RAS → **cétuximab/panitumumab**
5. **KRAS muté** : longtemps « indrugable », maintenant **sotorasib/adagrasib (G12C)** ; rend les anti-EGFR **inefficaces** en CCR
6. **BRAF V600E** mélanome → bithérapie **vémurafénib + cobimétinib** ou **dabrafénib + tramétinib**
7. **Voie PI3K-AKT-mTOR** : **PTEN** = anti-oncogène ; **PIK3CA** muté ciblé par **alpélisib** ; mTOR par **évérolimus**
8. **Voie WNT/β-caténine** : APC muté = CCR (FAP) ; CTNNB1 muté = hépatoCBC, desmoïdes
9. **Voie Hedgehog** : PTCH muté = **CBC** (Gorlin), médulloblastome SHH ; ciblée par **vismodégib**
10. Autres voies majeures : **NOTCH, HIPPO, NF-κB, JAK-STAT (JAK2 V617F), TGF-β**
11. **Cross-talk** entre voies → mécanismes de résistance → bithérapies, switch d’ITK
12. **Médecine personnalisée** = identification du mécanisme oncogénique → choix de la thérapie ciblée
