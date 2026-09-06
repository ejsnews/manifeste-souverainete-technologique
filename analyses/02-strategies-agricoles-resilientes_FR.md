---
layout: default
lang: fr
author: eric_jacob
title: "Agriculteurs — stratégies agricoles résilientes"
description: "Protocole quantitatif pour classer les associations agricoles selon leur revenu minimum sous sécheresse, canicule et pluie extrême, avec thermolyse HYNOCA et retour du biochar au sol."
license: Creative Commons Attribution-NoDerivatives 4.0 International (CC BY-ND 4.0)
---

# Agriculteurs — stratégies agricoles résilientes

## Mission

Construire une base quantitative **France → Europe → Monde** permettant d'identifier, pour chaque territoire, sol, climat et système de culture, les associations agricoles capables de maintenir le meilleur revenu lorsque les conditions climatiques deviennent défavorables.

L'objectif n'est donc pas de rechercher uniquement le rendement maximal dans une année normale.

$$\boxed{A^*=\arg\max_A\min_{s\in S}R(A,s)}$$

Le système optimal est celui qui maximise le **revenu minimum** sur l'ensemble des scénarios climatiques étudiés.

---

# 1. Scénarios climatiques

L'agent doit évaluer chaque stratégie sur six scénarios :

| Code | Scénario | Effet recherché dans le modèle |
|---|---|---|
| N | Année normale | référence économique |
| D | Sécheresse | déficit hydrique prolongé |
| C | Canicule | températures extrêmes |
| DC | Sécheresse + canicule | stress thermique et hydrique combiné |
| P | Pluie extrême / inondation | excès d'eau, ruissellement, érosion |
| DP | Sécheresse puis pluie extrême | succession de deux stress opposés |

On définit :

$$S=\{N,D,C,DC,P,DP\}$$

Le scénario **DP** est important : une culture peut résister à la sécheresse mais être vulnérable à une pluie extrême sur un sol dégradé ou compacté.

---

# 2. Définition d'une stratégie agricole

Pour chaque culture principale, l'agent recherche :

- légumineuses associées ;
- plantes à racines profondes ;
- plantes à cycle complémentaire ;
- couverts végétaux ;
- cultures intermédiaires ;
- biomasses pérennes ;
- cultures de secours ;
- plantes adaptées aux déficits hydriques ;
- valorisation des récoltes déclassées ;
- valorisation des résidus réellement disponibles.

Une stratégie est définie par :

$$\boxed{A=(C,P,S,M,T)}$$

avec :

- $C$ : culture principale ;
- $P$ : plante(s) partenaire(s) ;
- $S$ : type de sol ;
- $M$ : mode de gestion ;
- $T$ : système de transformation et de valorisation.

---

# 3. Fonctions recherchées

| Fonction | Exemples |
|---|---|
| Azote | légumineuse, fixation biologique |
| Eau | racines complémentaires, couverture |
| Sol | structure, couverture, limitation de l'érosion |
| Temps | cycles différents |
| Espace | hauteurs et profondeurs racinaires différentes |
| Résilience | reprise après stress |
| Biomasse | matière valorisable |
| Revenu | nouveau produit ou débouché |
| Biodiversité | diversification des espèces |
| Risque | diminution de la dépendance à une seule récolte |

La complémentarité peut être représentée par :

$$F(A)=f_{eau}+f_{azote}+f_{sol}+f_{temps}+f_{espace}+f_{biomasse}+f_{revenu}$$

Cette expression constitue un cadre de classement ; les fonctions doivent ensuite être quantifiées avec des données adaptées au territoire.

---

# 4. Conversion biomasse → H₂

Référence de travail pour une configuration HYNOCA :

$$669\ {\rm kg/h}\longrightarrow50\ {\rm kgH_2/h}$$

avec une biomasse de référence à environ 35 % d'humidité.

À 8 000 heures/an :

$$669\times8000=5\,352\,000\ {\rm kg/an}$$

soit :

$$\boxed{5\,352\ {\rm t_{humide}/an}}$$

La valeur arrondie de référence peut être représentée par :

$$\boxed{5\,300\ {\rm t_{humide}/an}}$$

À 35 % d'humidité :

$$1\ {\rm t_{humide}}=0.65\ {\rm tMS}$$

et :

$$1\ {\rm tMS}\approx1.538\ {\rm t_{humide}}$$

Le rendement correspondant est :

$$\frac{50}{0.669}=74.7\ {\rm kgH_2/t_{humide}}$$

donc :

$$74.7\times1.538\approx115\ {\rm kgH_2/tMS}$$

Ainsi, pour les calculs exploratoires :

$$\boxed{1\ {\rm tMS}\approx115\ {\rm kgH_2}}$$

Cette valeur est une **conversion de modèle**, et non un rendement universel de toutes les biomasses.

Pour 5 300 t humides/an :

$$5300\times0.65=3445\ {\rm tMS/an}$$

Donc :

$$\boxed{N_{H6}=\frac{B_{MS,disp}}{3445}}$$

où $B_{MS,disp}$ est la biomasse sèche réellement disponible pour la thermolyse.

---

# 5. Valorisation économique

Pour une stratégie $A$ et un scénario $s$ :

$$\boxed{R(A,s)=R_{alimentaire}+R_{matière}+R_{H_2}+R_{biochar}+R_{chaleur}+R_{carbone}-C_{production}-C_{récolte}-C_{stockage}-C_{transport}-C_{transformation}}$$

Par exemple :

$$R_{H_2}=Q_{H_2}\times P_{H_2}$$

$$R_{biochar}=Q_{biochar}\times P_{biochar}$$

$$R_{carbone}=Q_{carbone}\times P_{carbone}$$

Les prix de l'H₂, du biochar et du carbone restent **paramétrables**.

---

# 6. Biomasse réellement disponible

Le modèle impose une contrainte fondamentale :

$$\boxed{B_{disp}=B_{produite}-B_{\text{retour au sol}}-B_{élevage}-B_{autres}-B_{pertes}}$$

Cette équation est **non négociable**.

La biomasse produite n'est pas automatiquement une biomasse énergétique disponible.

Une partie doit rester dans le système agricole pour :

- maintenir la matière organique du sol ;
- restituer des éléments minéraux ;
- protéger le sol ;
- nourrir éventuellement l'élevage ;
- maintenir les fonctions biologiques ;
- satisfaire les autres usages existants ;
- tenir compte des pertes de récolte et de stockage.

On impose donc :

$$B_{disp}\geq0$$

et :

$$B_{thermolyse}\leq B_{disp}$$

La biomasse effectivement envoyée vers la thermolyse est :

$$\boxed{B_{thermolyse}=\min(B_{disp},B_{besoin\ industriel})}$$

Cette contrainte empêche le modèle de produire artificiellement davantage d'H₂ en retirant trop de matière organique au sol.

## 6.1 Décomposition

Pour chaque culture :

$$B_{produite}=B_{résidus}+B_{cultures\ de\ biomasse}+B_{récoltes\ déclassées}+B_{autres}$$

Les coefficients doivent être déterminés **par culture, région, rendement et système de production**.

Le modèle ne doit jamais supposer que 100 % des résidus agricoles sont récupérables.

On peut définir :

$$f_{disp}=\frac{B_{disp}}{B_{produite}}$$

avec :

$$0\leq f_{disp}\leq1$$

---

# 7. Biochar et eau

Le biochar est traité comme une **variable agronomique**, et non comme une valeur fixe.

Les effets hydriques dépendent notamment :

- du type de sol ;
- de la texture ;
- du matériau ;
- de la dose ;
- de la granulométrie ;
- de la porosité ;
- du climat ;
- du mode d'application.

Une méta-analyse de 939 observations rapporte des augmentations moyennes de la capacité en eau disponible (AWC) de l'ordre de :

| Texture | Variation moyenne AWC |
|---|---:|
| Sols grossiers | +25,6 % |
| Sols moyens | +20,9 % |
| Sols fins | +11,5 % |

Ces valeurs ne doivent **jamais** être appliquées automatiquement à une exploitation.

L'agent doit utiliser :

$$\boxed{\Delta W=f(sol,biochar,dose,granulométrie,porosité,climat)}$$

On peut alors représenter :

$$W_{disponible}=W_{initial}+\Delta W_{biochar}+\Delta W_{structure}+\Delta W_{couverture}+\Delta W_{racines}$$

---

# 8. Rendement sous stress climatique

Pour chaque stratégie :

$$Y_N,Y_D,Y_C,Y_{DC},Y_P,Y_{DP}$$

puis :

$$R_N,R_D,R_C,R_{DC},R_P,R_{DP}$$

Le critère principal est :

$$\boxed{R_{min}(A)=\min(R_N,R_D,R_C,R_{DC},R_P,R_{DP})}$$

Le classement primaire est :

$$\boxed{A^*=\arg\max_A R_{min}(A)}$$

---

# 9. Indice de résilience

Un indicateur secondaire mesure la perte relative par rapport à l'année normale :

$$\boxed{RI(A)=\frac{R_{min}(A)}{R_N(A)}}$$

Le classement doit distinguer :

1. **revenu absolu résilient** : $R_{min}$ ;
2. **proportion du revenu conservée** : $RI$.

Une stratégie ayant un $RI$ élevé mais un revenu absolu faible n'est pas nécessairement économiquement préférable.

---

# 10. Exemple pédagogique

Les valeurs suivantes sont **fictives** et illustrent uniquement le fonctionnement du classement.

| Stratégie | Normal | Sécheresse | Canicule | D+C | Pluie extrême | D→P | **Minimum** |
|---|---:|---:|---:|---:|---:|---:|---:|
| Maïs seul | 100 | 55 | 65 | 35 | 70 | 30 | **30** |
| Maïs + légumineuse | 97 | 70 | 74 | 55 | 76 | 50 | **50** |
| Maïs + biomasse | 94 | 73 | 77 | 64 | 78 | 61 | **61** |
| Maïs + légumineuse + biomasse | 95 | 78 | 81 | 72 | 82 | 70 | **70** |

Le classement fictif devient :

$$70>61>50>30$$

![Exemple de classement](images/03-strategies-agricoles-revenu-resilient-exemple_FR.png)

---

# 11. Calendrier de biomasse et continuité industrielle

| Mois | Récolte | Biomasse produite | Biomasse disponible | Stock initial | Stock final | Consommation H6 |
|---|---:|---:|---:|---:|---:|---:|
| Janvier | | | | | | |
| Février | | | | | | |
| Mars | | | | | | |
| Avril | | | | | | |
| Mai | | | | | | |
| Juin | | | | | | |
| Juillet | | | | | | |
| Août | | | | | | |
| Septembre | | | | | | |
| Octobre | | | | | | |
| Novembre | | | | | | |
| Décembre | | | | | | |

Le bilan de stock respecte :

$$B_{stock,t+1}=B_{stock,t}+B_{disponible,t}-B_{thermolyse,t}$$

avec :

$$B_{stock,t}\geq0$$

L'objectif est :

$$\boxed{production\ saisonnière+stockage\longrightarrow approvisionnement\ industriel\ continu}$$

Le coût du stockage doit être intégré dans le modèle économique.

---

# 12. Récoltes déclassées : conservation d'une valeur économique

Une mauvaise récolte alimentaire ne doit pas nécessairement devenir une perte économique totale.

Les débouchés peuvent être représentés par une cascade :

$$\boxed{alimentaire\rightarrow alimentation\ animale\rightarrow matière\rightarrow thermolyse}$$

Le choix dépend :

- de la qualité de la récolte ;
- des normes applicables ;
- du prix ;
- du coût de transport ;
- de l'humidité ;
- du coût de transformation ;
- de la disponibilité industrielle.

Le modèle recherche le débouché maximisant la valeur nette :

$$V^*=\max_j(P_jQ_j-C_j)$$

sous réserve des contraintes réglementaires, agronomiques et logistiques.

---

# 13. Biomasses complémentaires

Lorsque leur adaptation au territoire est pertinente, l'agent peut tester notamment :

- miscanthus ;
- sorgho ;
- switchgrass ;
- silphie ;
- bambou ;
- saule ;
- peuplier ;
- camelina ;
- autres espèces pérennes ou annuelles adaptées.

Pour chaque biomasse :

$$B_{biomasse/ha}$$

puis :

$$H_2/ha$$

et, lorsque les paramètres industriels sont disponibles :

$$biochar/ha$$

ainsi que :

$$CA_{biomasse/ha}$$

et :

$$R_{net/ha}$$

Le classement doit porter sur le **système agricole complet**, et non sur la seule production de biomasse.

---

# 14. Première segmentation française

Cette table constitue un **plan de recherche**, et non une prescription agronomique.

| Zone | Cultures dominantes à tester | Compléments à étudier |
|---|---|---|
| Hauts-de-France | blé, betterave, pomme de terre | légumineuses, miscanthus |
| Grand Est | blé, orge, colza, maïs | féverole, légumineuses, miscanthus |
| Centre-Val de Loire | blé, colza, tournesol | légumineuses, miscanthus, sorgho |
| Nouvelle-Aquitaine | maïs, soja, blé, tournesol | sorgho, miscanthus |
| Occitanie | blé dur, tournesol, maïs | légumineuses, biomasses tolérantes au déficit hydrique |
| Bretagne / Pays de la Loire | maïs, céréales, prairies | légumineuses, biomasses pérennes |
| Méditerranée | céréales, vigne, fruits, légumes | espèces adaptées au déficit hydrique |

Pour chaque zone :

$$région\rightarrow sol\rightarrow climat\rightarrow culture\rightarrow association\rightarrow économie$$

---

# 15. France → Europe → Monde

Une fois les modèles français suffisamment documentés, l'agent doit être étendu progressivement à :

- Europe ;
- bassin méditerranéen ;
- Afrique ;
- Inde ;
- Asie du Sud-Est ;
- Amériques ;
- Australie.

La plante ou l'association optimale devient :

$$\boxed{Plant^*=f(climat,sol,eau,saison,culture,marché,mécanisation,biomasse,thermolyse)}$$

L'objectif n'est pas de trouver une plante universelle, mais la combinaison optimale pour chaque contexte.

---

# 16. Calcul à l'hectare

Pour chaque stratégie :

$$B_{disp/ha}=B_{produite/ha}-B_{\text{retour au sol}/ha}-B_{élevage/ha}-B_{autres/ha}-B_{pertes/ha}$$

Puis :

$$H_2/ha=B_{thermolyse/ha}\times\eta_{H_2}$$

où $\eta_{H_2}$ dépend de la biomasse et de la configuration industrielle.

Le revenu total est :

$$R_{ha}=R_{alimentaire,ha}+R_{énergie,ha}+R_{biochar,ha}+R_{carbone,ha}-C_{total,ha}$$

et :

$$\boxed{R_{min,ha}=\min_{s\in S}R_{ha}(s)}$$

---

# 17. Optimisation du territoire

Pour un territoire comportant $i=1,\ldots,n$ systèmes de culture :

$$B_{disp,territoire}=\sum_iB_{disp,i}$$

et :

$$H_{2,territoire}=\sum_iH_{2,i}$$

Le nombre théorique de H6 est :

$$\boxed{N_{H6}=\frac{B_{MS,disp,territoire}}{3445}}$$

L'optimisation réelle doit ensuite intégrer :

- distances ;
- coûts de transport ;
- stockage ;
- saisonnalité ;
- capacités de traitement ;
- marché local ;
- retour du biochar vers les sols.

---

# 18. Boucle matière et carbone

Le système complet peut être représenté par :

$$\boxed{agriculture\rightarrow biomasse\ disponible\rightarrow thermolyse\rightarrow \{H_2,\ chaleur,\ biochar,\ carbone\}\rightarrow agriculture}$$

Le biochar retourné au sol doit être comptabilisé comme une sortie de thermolyse et une entrée du système agricole.

Il faut donc éviter de compter deux fois la même matière :

$$B_{biochar}\rightarrow B_{\text{retour au sol}}$$

---

# 19. Sortie finale attendue

Pour chaque territoire, culture et stratégie :

| Variable | Résultat |
|---|---|
| Territoire | … |
| Culture principale | … |
| Association | … |
| Type de sol | … |
| Climat | … |
| Eau disponible | … |
| Rendement N | … |
| Rendement D | … |
| Rendement C | … |
| Rendement DC | … |
| Rendement P | … |
| Rendement DP | … |
| Biomasse produite | … |
| Retour au sol | … |
| Biomasse élevage | … |
| Autres usages | … |
| Pertes | … |
| **Biomasse disponible** | **…** |
| Biomasse thermolysée | … |
| H₂/ha | … |
| Biochar/ha | … |
| CA alimentaire | … |
| CA matière | … |
| CA énergie | … |
| CA biochar | … |
| CA carbone | … |
| Coûts | … |
| **Revenu minimum** | **…** |
| **Indice de résilience** | **…** |
| H6 nécessaires | … |

Le classement final est effectué prioritairement sur :

$$\boxed{R_{min}}$$

puis sur :

- indice de résilience ;
- besoin en eau ;
- biomasse disponible ;
- revenu annuel ;
- coûts logistiques ;
- stabilité du système ;
- bénéfices agronomiques ;
- potentiel de retour du biochar au sol.

---

# 20. Principe général

L'agent recherche une agriculture capable de produire plusieurs valeurs à partir du même territoire :

$$\boxed{alimentaire+matière+énergie+biochar+carbone}$$

La diversification n'est pas considérée comme une diminution de la production alimentaire.

Elle constitue une **assurance productive** permettant de conserver un débouché économique lorsque le rendement alimentaire devient insuffisant.

Une récolte peut ainsi changer de destination sans perdre nécessairement toute sa valeur :

$$\boxed{alimentaire\rightarrow matière\rightarrow énergie\rightarrow biochar}$$

La thermolyse devient alors un **débouché de résilience**, et non simplement une technologie de production d'hydrogène.

---

# Conclusion

L'objectif final n'est plus seulement :

> **Quelle culture produit le plus dans une bonne année ?**

mais :

> **Quelle combinaison agricole conserve le meilleur revenu lorsque l'année devient mauvaise ?**

Le principe mathématique est :

$$\boxed{A^*=\arg\max_A\min_{s\in S}R(A,s)}$$

avec :

$$S=\{N,D,C,DC,P,DP\}$$

et la contrainte fondamentale :

$$\boxed{B_{disp}=B_{produite}-B_{\text{retour au sol}}-B_{élevage}-B_{autres}-B_{pertes}}$$

Ainsi, l'énergie ne doit pas être obtenue au détriment de l'agriculture.

Le système recherché est une agriculture capable de transformer ses ressources excédentaires ou ses débouchés dégradés en **revenus complémentaires, énergie, biochar et résilience hydrique**, tout en maintenant la fertilité du sol.
