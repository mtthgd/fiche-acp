---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_adn
  - électrophorèse
  - gel_agarose
  - polyacrylamide
  - PCR
  - technique
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Électrophorèse - Partie 1 — Principe et gels classiques

> Liens : [[16_160 Électrophorèse - Partie 2]] | [[16_160 Électrophorèse - Partie 3]] | [[16_180 Qualification et quantification des acides nucléiques]] | [[16_310 PCR quantitative qPCR]]

## Principe et objectifs

L’électrophorèse de l’ADN est essentiellement réalisée pour répondre à **une question principale** : *quelle est la taille des fragments d’ADN étudiés ?*

On fait migrer l’ADN dans un **gel** sous l’effet d’un **champ électrique** ; la **vitesse de migration dépend de la taille** (exprimée en **paires de bases**).

Applications cliniques :
- **ADN dégradé ?**
- **Taille du produit PCR conforme à l’attendue ?**
- **Discriminer des fragments de tailles très proches**


### Pourquoi ça migre

Le **squelette organophosphoré** de l’ADN/ARN est **chargé négativement** → migration vers l’**anode (+)**.

> *« Vive le phosphate ! »* — il permet l’électrophorèse.

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p02_00.jpeg)

## Pouvoir discriminant — types de gel

| Gel | Taille des mailles | Application |
|-----|--------------------|-------------|
| **Agarose** | Larges, modulables par concentration | Discrimination grossière, communément utilisée |
| **Polyacrylamide** | Très fines | Haute résolution, gels de séquence |

Concentrations variables possibles dans les deux types.

## Gel d’agarose

### Substance
- **Agar / agar-agar** extrait d’**algues rouges**
- Forme des polymères constituant des **mailles** dont la taille dépend de la **concentration** (% dans le tampon)

### Migration
- **ADN double brin** = forme repliée → migration influencée par les **repliements** + la taille
- Petits ADN → migrent **plus vite et plus loin** que les grands


### Cuve d’électrophorèse horizontale
- Cuve remplie de **tampon TBE** ou **TAE**
- Gel **immergé** jusqu’à sa surface supérieure
- Bacs aux deux extrémités contenant le tampon (électrodes)


### Recette d’un gel d’agarose
1. Peser **1 g d’agarose** + dissoudre dans **50 mL** du même tampon (**TBE** ou **TAE**)
2. **Porter à ébullition** jusqu’à dissolution complète (liquide clair)
3. Couler dans un **moule** scotché aux 2 extrémités
4. Placer un **peigne** dans le gel encore liquide → formation des **puits**
5. Laisser **refroidir** (gélification)
6. Retirer scotchs et peigne, positionner dans la cuve


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p04_02.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p04_03.png)

### Préparation des échantillons
| Additif | Rôle |
|---------|------|
| **Glycérol** | **Alourdir** l’échantillon → dépôt au fond du puits (sinon fuite hors du puits dans le tampon) |
| **Bleu de bromophénol** | Migre comme un **petit ADN** (front) |
| **Xylène cyanol** | Migre comme un **grand ADN** |

Les colorants permettent de :
- Visualiser le **dépôt**
- Suivre la **progression** de la migration


## Visualisation — agents intercalants

L’ADN étant **invisible à l’œil nu**, on ajoute un **agent intercalant** :

| Agent | Caractéristiques |
|-------|------------------|
| **Bromure d’éthidium (BET)** | S’intercale entre les plans de bases ; visible en **UV orange** ; **mutagène** (gants), UV nocifs (lunettes) |
| Alternatives modernes | Moins toxiques (ex : SYBR Safe, GelRed) |

Le BET peut être incorporé :
- Dans le gel (lors de la cuisson)
- Ou par **immersion post-migration**

Lecture sous **UV** : bandes d’ADN apparentes ; photo Polaroid → image **noir et blanc**.



## Marqueur de poids moléculaire

- Dépôt en parallèle d’un **ladder** de fragments de tailles connues
- Permet d’**estimer la taille** des bandes échantillon par interpolation

## Choix du % d’agarose

| Concentration | Mailles | Discrimine |
|---------------|---------|------------|
| **0,7 %** | Très larges | Grandes tailles bien discriminées, **petits ADN s’échappent** |
| **1 %** | Standard | Usage général |
| **1,5 %** | Plus serrées | Mauvaise séparation des **grandes tailles** (restent ensemble) |
| **5 %** | Très serrées | Petits fragments seulement |

| Taille recherchée | % agarose adapté |
|------------------|------------------|
| 50 → 0,5 kb (gros fragments) | **Faible % (~0,7-1 %)** |
| 1 kb → 0,1 kb (intermédiaires) | **1 - 1,5 %** |
| Très petits (< 100 pb) | Polyacrylamide nécessaire |

⚠ **Limite intrinsèque** des gels d’agarose : ne permet pas de distinguer **des variations de quelques paires de bases**, même à concentration élevée.


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p09_00.jpeg)

## Gel de polyacrylamide

Pour résolution **haute** (mailles **fines, denses**) :

### Sécurité
- **Acrylamide en poudre = dangereux** (neurotoxique, cancérogène)
- Vendu désormais **uniquement en solution** ou en **gel pré-coulé**

### Variantes
| Gel | État de l’ADN | Discrimination |
|-----|---------------|----------------|
| **Polyacrylamide natif** | ADN **double brin** (replié) | Migration dépend de la taille **et** des repliements |
| **Polyacrylamide dénaturant + urée** | ADN **simple brin** dénaturé | Migration **selon la seule taille** ; résolution **à 1 base près** |

### Cuve verticale
- Longueurs de gel plus importantes → cuves **verticales**, dépôt par le haut
- Gel plus fin → dépôt à la **seringue** plutôt qu’au cône
- Électrodes en haut (–) et en bas (+)


![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p09_02.png)

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p10_00.jpeg)

## Synthèse — choix du gel selon la résolution

| Gel | Tailles bien discriminées | Résolution |
|-----|----------------------------|------------|
| **Agarose natif (double brin)** | **0,5 - 50 kb** | Faible |
| **Polyacrylamide natif** | **0,1 - 1 kb** | Moyenne |
| **Polyacrylamide dénaturant** (simple brin) | **300 - 500 pb (et au-delà)** | **À 1 base près** ⇒ gels de **séquence** |

La **longueur de migration** est cruciale : plus on fait migrer, **plus on discrimine**. Possibilité de gels de **30 cm**, mais **fragiles** et difficiles à manipuler → solution = électrophorèse capillaire (cf [[16_160 Électrophorèse - Partie 2]]).

![](https://pub-09a67500e45345d4babec28739403570.r2.dev/pathologie-moleculaire/rappels-adn/16-160%20Electrophor%C3%A8se%20-%20Partie%202%20pdf/p11_00.png)

---

## 🔑 Points clés à retenir

1. **Objectif principal** : déterminer la **taille** des fragments d’ADN
2. ADN **chargé négativement** (squelette **phosphate**) → migration vers l’**anode**
3. Petits fragments → **migrent plus loin et plus vite**
4. **Agarose** : extrait d’algues rouges, mailles modulables par concentration
5. Cuve **horizontale** + tampon **TBE/TAE**
6. Échantillon = **glycérol + bleu de bromophénol + xylène cyanol** (densité + suivi)
7. Visualisation par agents **intercalants** : **BET** (mutagène, UV), alternatives moins toxiques
8. **Marqueur de poids moléculaire** indispensable pour estimer les tailles
9. **Choix du % d’agarose** selon la taille à discriminer (0,7 % pour grands fragments, 1,5 % inadapté aux grands)
10. Agarose **inadapté** pour des variations de quelques pb → **polyacrylamide**
11. **Polyacrylamide dénaturant + urée** = résolution à **1 base près** (essentiel pour le séquençage)
12. Acrylamide **toxique** : manipuler en solution / gels pré-coulés ; cuves **verticales** pour gels longs
