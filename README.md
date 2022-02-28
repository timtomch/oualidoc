---
title: Introduction
has_children: false
nav_order: 1
---

# Introduction

Bienvenue dans la documentation Ouali. Ce site est amené à évoluer dans les prochains jours.

## Démarrage

On accède à Ouali en naviguant vers [ouali.renouvaud.ch](ouali.renouvaud.ch). 

Utilisez vos identifiants Alma habituels pour vous identifier, en prenant soin de choisir le réseau 
(Network Zone, Sciences et Patrimoines, Écoles et Lecture publique) correspondant à votre identifiant.
Veuillez contacter la [Coordination Renouvaud](mailto:coordrnv@renouvaud.ch) si vous rencontrez des
difficultés à vous connecter à Ouali.

## Fonctionnement général

Le système Ouali gère des alignements entre des paires (source-cible) de référentiels. Un alignement consiste à définir pour chaque élément du référentiel source une correspondance vers un élément cible (ou une non-correspondance lorsque aucun élément cible ne correspond). Ainsi, chaque alignement (entre deux référentiels) est constitué de nombreuses correspondances (entre des éléments des référentiels concernés)

Pour construire ces alignements, le système effectue, pour chaque élément source, une recherche d’éléments cibles correspondants qui sont ensuite comparés de manière détaillée au moyen d’un algorithme de correspondance. En fonction des résultats de ces calculs de correspondance, le système va émettre une décision pour l’élément source concerné qui consistera soit à établir automatiquement des informations de correspondance pour l’élément source (avec ou sans entité cible correspondante), soit de mettre l’élément source en état d’attente d’arbitrage manuel.

Ces éléments en attente d’arbitrage peuvent ensuite être traités au moyen de l’interface d’arbitrage décrite dans ce manuel et ainsi compléter l’alignement.

### Instances



![Instances Ouali](/img/alignements.svg) 




## Interface d'arbitrage

Lorsque vous ouvrez une nouvelle instance, la fenêtre suivante s'affiche.

Chaque utilisateur se voit automatiquement attribuer un ensemble d’éléments à arbitrer (initialement 25) qu’il peut alors traiter à son rythme, tout en rejetant les cas qu’il n’est pas en mesure de traiter. Au fur et à mesure de l’avancement, des nouveaux éléments sont automatiquement attribués en fin de liste à de sorte à conserver un ensemble contenant toujours au moins 25 éléments jusqu’à ce que la totalité des cas à arbitrer aient été traités. 

Les éléments restent attribués pour une période de 10 jours au maximum (remis à zéro lors de chaque connexion sur Ouali). Ensuite, ils redeviennent disponibles pour être attribués à d’autres utilisateurs.

Le processus d’arbitrage manuel consiste à sélectionner un élément source à traiter dans les liste des éléments à traiter (1) pour l’analyser (2) ensuite choisir l’entité cible correspondante (3) au moyen de la liste des candidats automatiques (4) ou au moyen d’une recherche manuelle (5). Une fois qu’une entité cible correspondante a été sélectionnée, ou qu’aucune entité cible correspondante n’a pu être identifiée, il est alors possible de définir le détail des informations de correspondance (type, niveau de confiance, …) au moyen du formulaire adéquat (6).

![Interface Ouali](/img/interface-alignement.png) 

Les numéros et lettres ci-dessous correspondent aux numéros sur la figure.

1. Liste des éléments sources comprenant un onglet nommé Attribués pour accéder à la liste des éléments attribués spécifiquement à soi, ou traités par soi, et un onglet Tout contenant tous les éléments.
    1. Bouton permettant d’obtenir des éléments attribués supplémentaires (ajoutés en fin de liste)
    2. Bouton permettant de rejeter tous les éléments attribués et de recevoir un nouvel ensemble d’éléments attribués
    3. Bouton pour rejeter un élément spécifique
    4. Liste des éléments traités précédemment
2. Détail de l’élément source en cours de traitement. La couleur de l’en-tête indique l’état de la correspondance pour cet élément: bleu = aucune information de correspondance définie (en arbitrage), vert = correspondance avec un élément cible définie, rouge = correspondance sans élément cible (rejet)
    1. Bouton permettant d’accéder à la vue MARC de l’entité
    2. Liste des notices bibliographiques liées et des correspondances existantes (partie droite)
3. Détail de l’élément cible (forme du contenu identique à l’élément source)
4. Liste des candidats automatiques avec une indication sur le résultat de correspondance automatique
5. Onglet permettant d’accéder à la recherche directe, si les candidats automatiques ne semblent pas satisfaisants.
6. Panneau de correspondance pour l’élément source, et formulaire de correspondance utilisateur (voir ci-dessous)
7. Etat global de l’alignement (nombres d’éléments avec ou sans correspondance et en attente d’arbitrage)

###Panneau de correspondance
Ce panneau donne une vue d’ensemble des diverses sources de correspondance existante pour cet objet. Cela comprend:

* Alignement utilisateur: correspondance (non-correspondance) précise définie explicitement par un utilisateur (correspondance manuelle)
* Alignement externe: alignement pré-existant tels que VIAF ou provenant d’un projet local
* Recherche automatique: algorithme de recherche automatique de correspondance dans le réservoir cible à partir des libellés de l’objet source. Cet algorithme fournit un ensemble de candidat classé en trois catégories: valide (vert), fort (orange) ou faible (rouge)

La partie inférieure (décision) indique la correspondance effectivement établie par le système. Celle-ci est définie par un algorithme de décision à partir des informations existantes. En l’état, l'algorithme sélectionne la première correspondance valide parmi les 3 sources d’informations prises dans l’ordre, soit:

1. Si une correspondance utilisateur existe, alors celle-ci sera systématiquement sélectionnée
2. Sinon, si une correspondance externe existe, alors celle-ci est sélectionnée
3. Sinon, si la recherche automatique produit un unique candidat valide, alors celui-ci sera sélectionné
4. Sinon, aucune correspondance (ou non correspondance) ne sera établie pour cet élément qui sera alors considéré comme devant être attribué pour un arbitrage utilisateur

Finalement, le panneau comprend également un bouton permettant de définir, ou d’éditer, les informations de correspondance utilisateur.
