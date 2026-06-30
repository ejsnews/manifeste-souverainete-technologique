---
layout: default
title: "Modélisation Économique - Installation H6 + S-iC et dérivés du Syngas"
---

# Modélisation Économique - Installation H6 + S-iC et dérivés du Syngas

*Modélisation indépendante basée sur les données publiques de Haffner Energy - Éric Jacob, ingénieur (Maths-Sup, DEA)*

> **Avertissement méthodologique** : Ce document est une modélisation indépendante
> basée sur les données publiques disponibles (communiqués de presse, brevets,
> webinaires actionnaires). Les chiffres sont des estimations à confirmer par
> Haffner Energy. Les hypothèses sont explicitées pour chaque calcul.
> Ce document compile par ailleurs des données techniques
> publiques sur le stockage de l'hydrogène. Les chiffres d'efficacité varient
> sensiblement selon les sources — parfois du simple au triple — reflétant un
> débat technique réel et non tranché. Les fourchettes sont présentées
> honnêtement plutôt que lissées.

---

## I. Chimie fondamentale - Les équations du syngas

Le syngas produit par Haffner est un mélange de H₂ et CO. Il est la molécule
plateforme qui permet de synthétiser tous les dérivés :

**Hydrogène vert** (séparation directe) :
$$\text{Syngas} \xrightarrow{\text{séparation}} \text{H}_2 + \text{CO}$$

**Ammoniac** (procédé Haber-Bosch) :
$$3\text{H}_2 + \text{N}_2 \xrightarrow{400-500°C,\ 150-250\ bar} 2\text{NH}_3$$

**Biodiesel/SAF** (synthèse Fischer-Tropsch) :
$$n\text{CO} + (2n+1)\text{H}_2 \xrightarrow{\text{cobalt/Fe}} \text{C}_n\text{H}_{2n+2} + n\text{H}_2\text{O}$$

**Méthanol** :
$$\text{CO} + 2\text{H}_2 \xrightarrow{250°C,\ 50\ bar} \text{CH}_3\text{OH}$$

**Méthane de synthèse / biométhane** (procédé Sabatier — confirmé chez Haffner) :
$$\text{CO} + 3\text{H}_2 \xrightarrow{\text{Ni},\ 300-400°C} \text{CH}_4 + \text{H}_2\text{O}$$

En complément des dérivés déjà identifiés (H₂, NH₃, SAF, méthanol, méthane), Haffner
Energy est ouvert à d'autres molécules d'intérêt issues du syngas :

**Diméthyl éther (DME)** — carburant diesel propre, dérivé du méthanol :
$$2\text{CH}_3\text{OH} \xrightarrow{\text{Al}_2\text{O}_3,\ 250°C} \text{CH}_3\text{OCH}_3 + \text{H}_2\text{O}$$

**Urée** (engrais solide stable, dérivé direct de l'ammoniac) :
$$2\text{NH}_3 + \text{CO}_2 \xrightarrow{180°C,\ 150\ bar} \text{CO(NH}_2)_2 + \text{H}_2\text{O}$$

**Acide nitrique** (voie azotée alternative, engrais NPK, applications civiles) :
$$4\text{NH}_3 + 5\text{O}_2 \xrightarrow{\text{Pt/Rh},\ 800°C} 4\text{NO} + 6\text{H}_2\text{O}$$

**LOHC — Méthylcyclohexane** (stockage liquide à pression atmosphérique) :
$$\text{Toluène} + 3\text{H}_2 \xrightarrow{\text{catalyseur Pt/Pd}} \text{Méthylcyclohexane}$$

---

## II. Pistes à explorer pour le stockage de l'hydrogène

### Le problème de référence : 350-700 bars

Le stockage gazeux comprimé reste la norme industrielle actuelle, mais impose
des réservoirs lourds, coûteux (fibre de carbone), et une densité énergétique
volumique limitée (~1,3 kWh/L à 700 bars, contre ~9,7 kWh/L pour l'essence).

### Voie 1 — Stockage via ammoniac (déjà dans l'écosystème Haffner)

**Synthèse (Haber-Bosch) :**
$$3\text{H}_2 + \text{N}_2 \xrightarrow{400-500°C,\ 150-250\ bar} 2\text{NH}_3 \quad (\eta = 70-75\%)$$

**Craquage (libération H₂) :**
$$2\text{NH}_3 \xrightarrow{\text{catalyseur},\ 400-600°C} 3\text{H}_2 + \text{N}_2$$

**Avantage stockage :** l'ammoniac liquide se stocke à seulement **8-10 bars**
à température ambiante (comme du GPL), contre 700 bars pour l'H₂ pur — un gain
de pression considérable, avec une densité énergétique volumique supérieure
de 40% à l'hydrogène liquide.

**Le débat sur l'efficacité round-trip :**

| Source | Efficacité round-trip annoncée | Contexte |
|:-------|:-------------------------------:|:---------|
| CSIRO (Australie) | 76% craquage seul / pertes 1,41 MWh/tonne | Meilleur cas catalytique optimisé |
| DOE / ESI 2026 | 60-70% (Haber-Bosch + craquage) | Référence thermodynamique H2A v3.2 |
| CleanTechnica (analyse critique) | 20-30% seulement | Inclut compression finale + pile à combustible |
| Kleinman Energy (Penn) | 0,88-1,76 MWh/tonne NH₃ pour craquage | Selon technologie catalytique |

**Pourquoi un tel écart ?** Les chiffres optimistes (60-76%) mesurent
uniquement la synthèse + craquage. Les chiffres pessimistes (20-30%) intègrent
toute la chaîne jusqu'à la roue d'un véhicule à pile à combustible, où les
pertes s'accumulent : Haber-Bosch (25-30% de perte) + craquage (15-40% de
perte) + compression finale + rendement pile à combustible (50-60%).

**Coût additionnel estimé :** 0,50 à 1,00 €/kg H₂ pour la transformation
aller-retour, avant même le CAPEX des installations de craquage.

### Voie 2 — LOHC liquides (Liquid Organic Hydrogen Carriers)

$$\text{Toluène} + 3\text{H}_2 \rightleftharpoons \text{Méthylcyclohexane}$$

**Avantage :** se transporte comme du diesel dans les infrastructures
pétrolières existantes, à pression atmosphérique, stockage longue durée
sans perte (contrairement à l'H₂ liquide qui "boil-off" en continu).

**Inconvénient :** efficacité généralement inférieure à l'ammoniac selon
plusieurs analyses comparatives, et nécessite un recyclage du toluène
(infrastructure de retour du véhicule porteur déshydrogéné).

### Voie 3 — Hydrures métalliques solides

$$\text{Mg} + \text{H}_2 \rightleftharpoons \text{MgH}_2$$

Stockage à pression quasi-nulle, densité volumique élevée, mais nécessite
un apport thermique (~300°C) pour le relargage — pertinent pour stockage
fixe (datacenter, site industriel) plutôt que mobilité.

### Voie 4 — Hypothèse exploratoire : maillage structurel sans transformation chimique

L'idée évoquée — un matériau qui "range" l'hydrogène dans un volume réduit
sous haute pression sans le transformer chimiquement — correspond en réalité
au principe des **MOF (Metal-Organic Frameworks)** : structures cristallines
nanoporeuses qui adsorbent physiquement l'H₂ dans leurs pores (physisorption),
sans réaction chimique, donc sans perte énergétique de conversion.

**Avantage théorique majeur :** pas de Haber-Bosch, pas de craquage, donc
pas de perte des 25-40% inhérentes à la voie ammoniac. L'hydrogène reste
H₂, simplement comprimé dans une structure poreuse à plus basse pression
qu'un réservoir vide.

**Limite actuelle :** les MOF les plus performants atteignent des capacités
de stockage encore insuffisantes à température ambiante pour rivaliser
avec les 700 bars en usage automobile — la recherche est active mais pas
encore mature industriellement. C'est une piste de recherche, pas une
solution disponible aujourd'hui.

*C'est une hypothèse de recherche, pas une technologie déployée. Mais elle
mérite d'être creusée avec des laboratoires spécialisés (CNRS, CEA) si
Haffner souhaite explorer une voie de stockage sans transformation chimique.*

---

## III. Applications par mode de transport — quel vecteur pour quel usage ?

| Usage | Vecteur recommandé | Justification |
|:------|:-------------------|:---------------|
| Véhicule léger (voiture) | H₂ comprimé 700 bars | Infrastructure existante, rapidité plein |
| Poids lourd longue distance | H₂ comprimé ou ammoniac | Selon disponibilité stations sur trajet |
| Navire (cargo, ferry) | **Ammoniac direct** (moteur dédié) | Pas de craquage nécessaire — combustion directe NH₃ possible |
| Avion (SAF) | **SAF liquide** (Fischer-Tropsch) | Densité énergétique massique élevée, infrastructure aéroport existante |
| Stockage stationnaire (datacenter, usine) | Hydrures métalliques ou ammoniac | Pas de contrainte de poids embarqué |
| Réseau électrique (back-up) | Pile à combustible H₂ directe | Meilleur rendement sans étape de conversion |

**Point clé pour les navires :** plusieurs chantiers navals développent déjà
des moteurs à combustion directe de l'ammoniac (sans craquage préalable),
ce qui évite la perte de 25-40% du craquage. C'est la voie la plus mature
pour le transport maritime décarboné à l'horizon 2027-2030.

---

## IV. Synthèse comparative des vecteurs

| Critère | H₂ comprimé 700 bars | Ammoniac (NH₃) | LOHC (méthylcyclohexane) | Hydrure métallique |
|:--------|:---------------------:|:---------------:|:-------------------------:|:-------------------:|
| Pression de stockage | 700 bars | 8-10 bars | Atmosphérique | Quasi-nulle |
| Densité énergétique volumique | Faible | Élevée (+40% vs H₂ liquide) | Moyenne | Élevée |
| Efficacité round-trip | Référence (100%) | 20-76% (débat technique) | 60-70% estimé | 70-85% estimé |
| Infrastructure existante | Stations dédiées | GPL/ammoniac existant | Pétrolière (adaptée) | Aucune (à créer) |
| Coût conversion aller-retour | Nul | 0,50-1,00 €/kg | Variable | Variable |
| Meilleur usage | Mobilité légère | Maritime, stockage longue durée | Transport longue distance | Stationnaire |

---

Il n'existe pas de vecteur hydrogène universellement supérieur — chaque
molécule dérivée du syngas Haffner (H₂ pur, ammoniac, méthane, méthanol,
SAF) a un usage où elle est optimale. La polyvalence de la technologie
Haffner permet précisément de choisir le bon vecteur selon le marché final,
plutôt que d'imposer une seule solution à tous les usages.

La piste des matériaux poreux (MOF) pour un stockage sans transformation
chimique reste la plus prometteuse à long terme pour éliminer les pertes
de conversion — mais elle est encore au stade de la recherche fondamentale.

---

## V. Architecture H6 + S-iC - Hypothèses de modélisation

### Configuration étudiée

L'image économique publiée par Haffner Energy montre une installation couplée
H6 + H4 (S-iC). Voici l'architecture telle que modélisée :

| Composant | Rôle | Production H₂ |
|:----------|:-----|:-------------:|
| H6 | Thermolyse biomasse brute → syngas + biochar | 60 kg H₂/h |
| S-iC (H4 amélioré) | Reçoit le biochar du H6, valorisation avancée | 482 kg H₂/h |
| **Total installation** | | **542 kg H₂/h** |

**Hypothèse sur le ratio H6/S-iC** : le S-iC reçoit du biochar, pas de biomasse
brute. Si un H6 produit ~200-350 kg de biochar/tonne de biomasse, et que le S-iC
traite 482 kg H₂/h, on estime qu'il faut **4 à 5 modules H6** pour alimenter
un S-iC en continu. *À confirmer par Haffner Energy.*

### Disponibilité annuelle

$$\text{Heures opérationnelles} = 8760 \times 85\% = 7446\ \text{h/an}$$

$$\text{Production annuelle H}_2 = 542\ \text{kg/h} \times 7446\ \text{h} = 4\ 035\ 732\ \text{kg H}_2\text{/an}$$

---

## VI. Scénario A - Production d'hydrogène vert (référence)

C'est le scénario de base de l'image économique publiée par Haffner :

| Paramètre | Valeur |
|:----------|:------:|
| Production annuelle H₂ | 4 035 732 kg |
| Prix de vente minimum | 6,50 €/kg |
| **Chiffre d'affaires annuel** | **26 232 258 €** |
| OPEX total (H6 + S-iC + maintenance) | 2 600 888 € |
| **Gain net annuel** | **23 631 370 €** |
| CAPEX estimé | 5 000 000 € |
| **Amortissement** | **< 3 mois** |

---

## VII. Scénario B - Production d'ammoniac vert (engrais)

### Données scientifiques

- Procédé Haber-Bosch : 3 mol H₂ + 1 mol N₂ → 2 mol NH₃
- Rapport massique : **1 kg H₂ → 5,65 kg NH₃**
- Énergie requise : 14-15 kWh/kg NH₃ (fournie par le syngas lui-même)
- Efficacité de conversion H₂ → NH₃ : 76%

### Calcul sur installation H6 + S-iC

$$\text{H}_2\ \text{disponible} = 4\ 035\ 732\ \text{kg/an}$$

$$\text{NH}_3\ \text{produit} = 4\ 035\ 732 \times 0{,}76 \times 5{,}65 = 17\ 321\ 073\ \text{kg NH}_3\text{/an}$$

| Paramètre | Valeur |
|:----------|:------:|
| Production annuelle NH₃ | ~17 300 tonnes |
| Prix marché NH₃ vert | 400-600 €/tonne |
| **Chiffre d'affaires annuel** | **6,9 – 10,4 M€** |
| Équivalent engrais (urée) | ~22 000 tonnes urée |
| Surface agricole couverte | ~15 000 ha de céréales |

> **Note** : le CA ammoniac est inférieur à l'hydrogène pur (6,50 €/kg),
> mais l'ammoniac est plus facile à stocker et transporter. Le choix entre
> les deux dépend du marché local.

---

## VIII. Scénario C - Production de biodiesel/SAF (Fischer-Tropsch)

### Données scientifiques

- Rendement biomasse → FT liquides : **15-28% en masse** selon la littérature
- 1 tonne de biomasse à 30% humidité → **159 litres de biodiesel** (ScienceDirect)
- Pouvoir calorifique FT-diesel : 43-45 MJ/kg (supérieur au diesel fossile)
- Rendement global FT : 40-51% de l'énergie initiale de la biomasse

### Calcul sur installation H6 (seul, sans S-iC)

En mode Fischer-Tropsch, le syngas est orienté vers la synthèse FT plutôt
que vers la séparation H₂. On modélise sur le H6 seul (60 kg H₂/h) :

$$\text{Biomasse traitée H6} \approx 1\ \text{tonne/h} \times 7446\ \text{h} = 7446\ \text{t/an}$$

$$\text{Biodiesel produit} = 7446 \times 159\ \text{L} = 1\ 183\ 914\ \text{L/an}$$

| Paramètre | Valeur |
|:----------|:------:|
| Production annuelle biodiesel | ~1 184 000 litres |
| Prix biodiesel/SAF marché | 1,20-1,80 €/L |
| **Chiffre d'affaires annuel (H6 seul)** | **1,4 – 2,1 M€** |
| Équivalent kérosène substitué | ~950 tonnes |
| Réduction CO₂ vs kérosène fossile | ~2 500 tCO₂/an |

---

## IX. Comparaison des scénarios - Tableau de synthèse

| Scénario | Produit | CA annuel estimé | Marché prioritaire |
|:---------|:--------|:----------------:|:-------------------|
| A | Hydrogène vert | 23,6 M€ net | Datacenters, mobilité H₂ |
| B | Ammoniac vert | 6,9 – 10,4 M€ | Agriculture, engrais |
| C (H6 seul) | Biodiesel/SAF | 1,4 – 2,1 M€ | Aviation, transport lourd |
| A+B mixte | H₂ + NH₃ | Variable selon ratio | Territoire multi-usages |

> **Observation** : Le scénario A (hydrogène pur) est le plus rentable à court
> terme. Le scénario B (ammoniac) est le plus souverain (engrais locaux).
> Le scénario C (SAF) est le plus pertinent pour l'aviation. Un module Haffner
> peut basculer d'un mode à l'autre selon la demande locale.

---

## X. Démonstration mobilité - H₂ vs Essence

Basé sur la BMW iX5 Hydrogen (750 km / 7 kg H₂) avec H₂ Haffner à 1,50 €/kg :

| Paramètre | Véhicule Essence | BMW iX5 (H₂ Haffner) |
|:----------|:----------------:|:--------------------:|
| Densité énergétique carburant | 12,2 kWh/kg | **33,3 kWh/kg** |
| Rendement moteur | 30-35% | **50-60%** (pile) + >90% (moteur) |
| Consommation/100 km | 6,5 L | **0,93 kg H₂** |
| Prix carburant | 1,70 €/L | **1,50 €/kg** (Haffner local) |
| **Coût réel/100 km** | **~11,05 €** | **~1,40 €** |
| **Facteur d'économie** | référence | **×7,9 moins cher** |

$$\text{Économie annuelle (20 000 km)} = (11{,}05 - 1{,}40) \times 200 = 1\ 930\ €\text{/an/véhicule}$$

---

## XI. Impact macroéconomique France - Modélisation à grande échelle

Si 10 000 installations H6+S-iC étaient déployées en France (scénario à 10 ans) :

| Indicateur | Valeur estimée |
|:-----------|:--------------:|
| H₂ produit | 40 millions t/an |
| CA généré | 260 milliards €/an |
| Réduction imports fossiles | -40 à -60 Mds€/an |
| Emplois directs créés | 200 000 – 400 000 |
| CO₂ séquestré (biochar) | 50-80 millions tCO₂/an |

> **Note** : Ces chiffres sont une extrapolation linéaire à titre illustratif.
> Le déploiement réel dépend des ressources en biomasse disponibles, estimées
> à plusieurs centaines de millions de tonnes en France (résidus agricoles,
> forestiers et urbains).

---

## Conclusion

Le modèle économique Haffner est remarquable par sa polyvalence : une même
plateforme technologique peut produire, selon les besoins locaux, de l'hydrogène,
de l'ammoniac, du biodiesel ou du SAF - sans modifier le cœur de la technologie.

Cette flexibilité est unique au monde. Elle permet à chaque territoire de choisir
le produit qui correspond à ses besoins prioritaires : mobilité, agriculture,
aviation ou énergie - avec un retour sur investissement dans tous les cas
inférieur à 3 mois pour une installation H6+S-iC.

---

*Manifeste complet : [https://ejsnews.github.io/manifeste-souverainete-technologique/](https://ejsnews.github.io/manifeste-souverainete-technologique/)*
