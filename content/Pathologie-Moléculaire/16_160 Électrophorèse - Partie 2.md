---
tags:
  - anatomopathologie
  - ACP
  - biologie_moléculaire
  - pathologie_moléculaire
  - rappels_adn
  - électrophorèse_capillaire
  - séquenceur_capillaire
  - séquençage_Sanger
  - fluorochrome
  - technique
date: 2024
source: DES ACP - Pathologie moléculaire
---

# Électrophorèse - Partie 2 — Électrophorèse capillaire

> Liens : [[16_160 Électrophorèse - Partie 1]] | [[16_160 Électrophorèse - Partie 3]] | [[16_180 Qualification et quantification des acides nucléiques]] | [[16_510 NGS - Principes et applications]]

## Pourquoi miniaturiser le gel ?

Pour la **résolution maximale** (analyse des produits d’un **séquençage Sanger**), il faut une **résolution à 1 base près** sur **plusieurs centaines de paires de bases** :
- Gel d’**acrylamide dénaturant** (urée → casse les liaisons hydrogène)
- ADN **simple brin**
- Migration sur **20 à 80 cm de long**
- Le gel devient **fragile et difficile à manipuler**

Question : *comment simplifier et optimiser ce séquençage en gel d’acrylamide pour manipuler facilement des longueurs jusqu’à 80 cm ?*


## De la plaque au capillaire

Schématiquement, on peut envisager :
- Un gel d’acrylamide dans un **tube** plutôt qu’une plaque
- Des tubes **très fins = capillaires** → encore plus économique en acrylamide
- **Quelques mm** de capillaire suffisent pour la lecture (zone de détection nanométrique)

Lecture par **fluorescence ultra-sensible** :
- **Caméra CCD** recueille les rayonnements émis
- Excitation par un **laser argon**

À la fin de la migration, juste avant que les fragments ne tombent dans la cuve inférieure, on lit la **fluorescence** ; les fluorochromes différents (un par base) défilent un par un.

![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p02_00.jpeg]]


## Fonctionnement du séquenceur capillaire

### Phase 1 — Chargement de l’échantillon
- Capillaire **déjà rempli d’acrylamide**
- Échantillon dans un tube ou puits d’une **plaque 96 puits**
- Application d’un **champ électrique positif** → l’ADN (négatif) **remonte** dans le capillaire
- **Petite impulsion** pour charger les fragments dans le capillaire

### Phase 2 — Migration
- Capillaire immergé à ses **deux extrémités** dans du **tampon de migration**
- **Différence de potentiel ≈ 12 kV** (≈ **10 ×** supérieure à un gel classique) → migration **beaucoup plus rapide**
- Les fragments d’ADN migrent en fonction de leur **taille** (petits = avant)

### Phase 3 — Lecture
- Juste avant que les fragments tombent dans le tampon final, **lecteur de fluorescence**
- **Identifie le fluorochrome** porté par chaque fragment
- **Fragments légers** (= courts) = **lus en premier**



![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p04_02.png]]

![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p04_03.png]]

## Lecture d’une réaction Sanger — exemple

Réaction de séquence type Sanger : terminateurs di-désoxynucléotides marqués chacun par un **fluorochrome de couleur spécifique**.

Si la séquence à lire est **C-T-A-C…** :
- Fragment le plus court → **C** (fluorochrome **bleu**) → lu en premier
- Fragment +1 base → **T**
- Fragment +1 base → **A** (fluorochrome **vert**)
- Fragment suivant → **C** (bleu) — etc.

Lecture séquentielle des couleurs = **séquence** déduite.

Une migration produisant une lecture s’appelle un **run**.



## Spécificités techniques des séquenceurs capillaires

### Polymères
- On ne parle pas de "gel d’acrylamide" mais de **POP4** ou **POP6**
- Polymères équivalents à **différentes concentrations**

### Capillaires (Applied Biosystems)
- **Longueur** au choix : **22 → 80 cm** selon application
- Appareils lisent **4 à 16 capillaires simultanément**

### Astuces technologiques
- **Coating à la silice** des parois → empêche l’ADN négatif de coller
- **Polymère renouvelé à chaque run** : le polymère est chassé après chaque run, capillaire rincé pour éviter contamination
- Capillaire **réutilisable plusieurs centaines de fois**



## Architecture interne du séquenceur

| Élément | Rôle |
|---------|------|
| **Capillaires** (22-80 cm) | Migration |
| **Four** (18-65 °C) | Maintien de l’ADN simple brin (chaleur) |
| **Seringues** | Réinjection du polymère neuf à chaque run |
| **Dispositif de lecture** | Caméra CCD + laser |
| **Système de pipetage / entrée échantillon** | Partie inférieure de l’appareil |

![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p09_00.jpeg]]


![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p09_02.png]]

## Cycle d’un run — résumé

1. **Rinçage** du capillaire (anti-contamination)
2. **Injection de polymère neuf** (POP4/POP6)
3. **Chargement de l’échantillon** par impulsion électrique
4. **Migration** sous **12 kV**
5. **Lecture** en continu de la fluorescence
6. Évacuation du polymère, prêt pour le run suivant

![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p10_00.jpeg]]

## Applications de l’électrophorèse capillaire en pathologie

| Application | Détail |
|------------|--------|
| **Séquençage Sanger** | Application historique, but premier des appareils |
| **Analyse de fragments** | Mesure de la taille des fragments à 1 pb près (cf [[16_160 Électrophorèse - Partie 3]]) |
| **Recherche de perte d’hétérozygotie (LOH)** | Voir Partie 3 |
| **Analyse de clonalité** (B/T) | Réarrangement Ig / TCR |

![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p11_00.png]]


![[assets/pathologie-moleculaire/rappels-adn/16-160 Electrophorèse - Partie 2 pdf/p11_02.png]]


---

## 🔑 Points clés à retenir

1. **Électrophorèse capillaire** = miniaturisation du gel d’acrylamide dénaturant pour la lecture du séquençage Sanger
2. Lecture par **fluorescence** : caméra **CCD** + laser **argon**
3. Capillaire = **tube fin** (qq µm) rempli de **polymère POP4/POP6**
4. Différence de potentiel **~12 kV** (10 × supérieure au gel classique) → migration rapide
5. **Fragments courts** lus en premier (migrent plus vite)
6. **Séquençage Sanger** : 4 fluorochromes (1 par base ddNTP terminateur)
7. Capillaires de **22-80 cm**, 4 à 16 simultanément
8. Polymère **renouvelé à chaque run** ; capillaire réutilisable des centaines de fois
9. **Coating silice** des parois (anti-adhésion ADN)
10. Four à **18-65 °C** pour maintenir l’ADN simple brin
11. Une **migration = un run**
12. Applications : **séquençage Sanger, analyse de fragments, LOH, clonalité Ig/TCR**
