---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - extraction_ffpe
  - formol
  - fixation
  - FFPE
  - artefacts_C_T
  - préanalytique
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Effet de la fixation sur les acides nucléiques

> Liens : [[16_355 Principes de microdissection tissulaire]] | [[16_365 Validation de la qualité de l’échantillon par qPCR]] | [[16_310 Principes de la qPCR]]

## Principe / Définition

La fixation est l’étape **préanalytique** clé qui conditionne la qualité des acides nucléiques extraits des tissus FFPE. Elle introduit inévitablement des **artefacts chimiques** (ponts méthylène, sites apuriniques/apyrimidiques, hydrolyse) qui peuvent générer des **mutations artefactuelles** lors des analyses moléculaires d’aval.

Le compromis fondamental : **morphologie vs biologie moléculaire**.

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p01_03.jpeg]]

## Phases d’un test moléculaire

1. **Phase préanalytique** : fixation, mise en condition du spécimen
2. **Phase analytique** : extraction des acides nucléiques + analyse génétique
3. **Phase post-analytique** : interprétation, validation, diffusion

L’extraction des acides nucléiques (**ADN ou ARN**) se situe à la charnière entre préanalytique et analytique.

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p02_02.jpeg]]

## Historique des fixateurs

- **Solutions alcooliques** d’origine (éthanol, méthanol, voire whisky/gin/rhum/brandy)
- **Ferdinand Blum** (médecin allemand) : découverte fortuite des propriétés fixatives du **formaldéhyde** en traitant un anthrax murin
- **Liquide de Bouin** (Paul Bouin, 1897) : acide picrique + formol + acide acétique → excellent morphologiquement mais **proscrit** car **hydrolyse l’ADN** et altère l’ARN
- **Fixateurs alternatifs** type **RCL2** : peu toxiques, ADN haut PM, mais coûteux et incompatibles avec les anticorps IHC commerciaux validés sur formol

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p03_00.jpeg]]

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p04_00.jpeg]]

## Le formol tamponné — fixateur universel

- **Formaldéhyde** = aldéhyde gazeux dissous dans l’eau (saturation **37–40 %**)
- En pratique : dilution au **1/10** → **formol à 10 %** = **4 % de formaldéhyde** = **idéal**
- **pH neutre tamponné** indispensable

| Avantages | Inconvénients |
|-----------|---------------|
| Bonne pénétration tissulaire | Morphologie moyenne |
| Peu de rétraction/durcissement | **Toxique** et **inflammable** |
| Conservation longue | Considéré **cancérigène** |
| Faible coût | Précipitation possible (**pigments formoliques**) |
| Peu de masquage antigénique | Artefacts moléculaires |

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p05_01.jpeg]]

## Paramètres clés de la fixation

| Paramètre | Valeur recommandée |
|-----------|--------------------|
| Délai préfixation (ischémie) | **< 30 min** (idéalement immédiat sur biopsies) |
| Vitesse de pénétration | **1 mm/h** environ |
| Durée optimale ADN | **3–6 h** |
| Durée habituelle | 24 h (variant de quelques heures à 48 h voire semaines) |
| Tranchage des grosses pièces | Oui (faciliter pénétration) |

**Plus la fixation est longue, plus la taille moyenne de l’ADN extrait diminue.**

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p08_00.jpeg]]

## Mécanismes chimiques d’altération de l’ADN par le formol

Quatre interactions principales formaldéhyde / ADN :

1. **Réaction d’addition** : ajout du formaldéhyde sur la base → groupe **hydroxyméthyl**
2. **Attaque électrophile lente** du composé N-méthylol sur une base aminée → formation d’un **pont méthylène** entre deux groupes aminés (cross-link inter-brins)
3. Génération de **sites AP** (apuriniques / apyrimidiques) par hydrolyse des liaisons N-glycosidiques → résidus de **2-désoxyribose** instables
4. **Hydrolyse lente des liaisons phosphodiester** → courtes chaînes de désoxyribose

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p10_00.png]]



## Artefacts moléculaires majeurs

### Transitions C>T (G>A) artefactuelles
- Liées à des **ponts entre cytosines** des deux brins
- L’ADN polymérase ne reconnaît plus la cytosine → incorpore une **adénine à la place d’une guanine**
- Génère des mutations artefactuelles **G>A** (transitions)
- Mécanisme : **désamination de la cytosine** → uracile

### Cassures de brin
- Les **histones** entourant l’ADN forment des ponts post-fixation
- Cassent l’ADN en **petits fragments**
- Conséquence : utiliser des **amorces courtes** = **80–130 paires de bases**

### Démonstration expérimentale
- Traitement par **uracile-DNA glycosylase (UNG)** d’*E. coli* : élimine l’uracile → site abasique → cassure de brin
- Disparition des transitions artefactuelles G>A après UNG → confirme leur origine par désamination

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p14_00.png]]


![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p17_00.jpeg]]

## Recommandations pratiques (Am J Pathol 2002)

| # | Recommandation |
|---|----------------|
| 1 | **Délai préfixation < 2 h** (ischémie froide/chaude) |
| 2 | Formol **neutre froid à 10 %**, faible concentration en sels |
| 3 | Fixation **à 4 °C** (peu réaliste en routine) |
| 4 | Durée courte : **3–6 h** |
| 5 | Additif **EDTA** |
| 6 | **Éviter pH faible** absolument |
| 7 | Amorces **80–130 pb** |

## Recommandations issues du génotypage KRAS (Lamy 2011)

1. **Microtome dédié**, lame propre **désinfectée** entre blocs (anti-contamination croisée)
2. Utiliser un fixateur **standardisé** = formol tamponné 10 %
3. Examen morphologique systématique du **% de cellules tumorales** par un pathologiste
4. **Conditions de stockage contrôlées** (éviter hydrolyse en milieu humide, temps long)
5. **Amorces courtes** + amplicons réduits + double contrôle des mutations (moins nécessaire depuis l’accréditation **COFRAC ISO 15189**)

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p18_01.jpeg]]

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p19_00.jpeg]]

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p20_00.jpeg]]

## ARN messagers et FFPE

- Longtemps réputés extractibles uniquement à partir de tissu **congelé**
- Aujourd’hui : **RNA-Seq possible sur FFPE**
- Études de profilage d’ARNm tumoral mammaire : majorité des techniques commerciales fonctionnent sur FFPE
- **micro-ARN** : généralement **stables** dans les deux protocoles, varient seulement après ischémie froide **> 12 h**
- Permet la recherche de **transcrits de fusion** sur FFPE

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p22_00.png]]

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p23_00.jpeg]]

![[assets/pathologie-moleculaire/extraction-adn-bloc-ffpe/16-351 Effet de la fixation sur les acides nucléiques NON SONORISE/p25_00.jpeg]]

## Pièges / Contrôles qualité

- **Mutations bizarres non reproductibles** entre runs successifs sur le même échantillon → suspicion d’artefact
- Bases de données de mutations historiques **biaisées** par les artefacts FFPE
- Contrôler chaque mutation suspecte par **2e technique** ou **PCR digitale**
- **Délai d’ischémie froide** = facteur le plus délétère

## 🔑 Points clés à retenir

1. **Formol tamponné 10 %** (= **4 %** de formaldéhyde) est le fixateur **universel** standard.
2. La fixation introduit des **artefacts moléculaires inévitables** : compromis morphologie/biologie moléculaire.
3. Quatre mécanismes : **addition**, **pont méthylène**, **sites AP**, **hydrolyse phosphodiester**.
4. Artefact principal = **transitions C>T / G>A** par désamination de la cytosine.
5. Durée optimale pour ADN : **3–6 h** ; routine 24 h dégrade l’ADN.
6. Amorces courtes = **80–130 pb** obligatoires sur FFPE.
7. **Délai préfixation < 30 min** (idéalement < 2 h).
8. **Liquide de Bouin proscrit** (hydrolyse ADN), **RCL2** marginal (incompatible IHC).
9. Microtome **dédié** + **désinfection** entre blocs pour éviter contaminations.
10. Évaluation systématique du **% de cellules tumorales** par le pathologiste.
11. **ARNm et miRNA** désormais analysables sur FFPE (RNA-Seq, transcrits de fusion).
12. Confirmation des mutations rares par **2e technique** (NGS, ddPCR) ou par accréditation **ISO 15189**.
