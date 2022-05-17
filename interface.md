---
layout: default
title: 2. Interface Ouali
has_children: false
nav_order: 3
description: "Présentation de l'interface d'Ouali et des outils à disposition"
has_toc: false
permalink: /interface
---

# Interface Ouali

On accède à Ouali en naviguant vers [ouali.renouvaud.ch](https://ouali.renouvaud.ch). 

Utilisez vos identifiants Alma habituels pour vous identifier, en prenant soin de choisir l'institution (Sciences et Patrimoines, Écoles et Lecture publique, Network Zone) correspondant à votre identifiant.
Veuillez contacter la [Coordination Renouvaud](mailto:coordrnv@renouvaud.ch) si vous rencontrez des
difficultés à vous connecter à Ouali.

## Capsules vidéo

Une introduction à l'usage de l'interface Ouali est également disponible sous forme de [courtes capsules vidéo](https://coordvd.zendesk.com/hc/fr/articles/4458702255378--Nouveaut%C3%A9-04-22-Introduction-%C3%A0-Ouali).

## Fonctionnement général

Le système Ouali gère des alignements de notices d'autorité entre un référentiel source et un référentiel cible. Chaque _alignement_
représente une notice d'autorité du référentiel source aligné vers une notice dans le référentiel cible.

Pour construire ces alignements, le système effectue, pour chaque notice du référentiel source, une recherche de notices dans le 
référentiel cible correspondantes qui sont ensuite comparés de manière détaillée au moyen d’un algorithme. 
En fonction des résultats de ces calculs de correspondance, le système va émettre une décision pour la notice source concernée qui 
peut prendre les formes suivantes:

* établir automatiquement une décision d'alignement vers une notice correspondante dans le référentiel cible,
* établir automatiquement une décision de non-alignement (il n'y a pas d'équivalence dans le référentiel cible),
* laisser la notice source en état d'attente d'arbitrage manuel.

Ces éléments en attente d’arbitrage peuvent ensuite être traités au moyen de l’interface d’arbitrage décrite dans ce manuel et ainsi compléter l’alignement.

Chaque utilisateur se voit automatiquement attribuer un ensemble de notices à arbitrer (initialement 25) qu’il peut alors traiter à son rythme, tout en rejetant les cas qu’il n’est pas en mesure de traiter. Au fur et à mesure de l’avancement, des nouveaux éléments sont automatiquement attribués en fin de liste à de sorte à conserver un ensemble contenant toujours au moins 25 éléments jusqu’à ce que la totalité des cas à arbitrer soit traitée. 

Les éléments restent attribués pour une période de 3 jours au maximum (remis à zéro lors de chaque connexion sur Ouali). Ensuite, ils redeviennent disponibles pour être attribués à d’autres utilisateurs.

## Codes de couleur

<img src="/oualidoc/img/interface-couleurs.png" alt="Codes couleurs utilisés dans Ouali" style="float: right; margin-left:10px;" width="150px"/>
Lorsqu'une **décision d'alignement** vers une notice du référentiel cible a été effectuée (soit automatiquement soit après arbitrage
manuel), la notice s'affiche en **vert** dans Ouali.

Lorsqu'une **décision de non-alignement** a été effectuée (automatiquement ou manuellement), la notice s'affiche en **rouge**.

Lorsqu'une notice est **en attente d'arbitrage** (aucune décision n'a encore été prise), elle s'affiche en **gris**.

La notice **actuellement sélectionnée** (sur laquelle on travaille) s'affiche en **bleu**.

<br style="clear:both;"/>
## Liste des instances

Une fois identifié dans Ouali, la liste des [instances](chantiers#instances-ouali) s'affiche. Cliquer sur le bouton "Arbitrage" pour
ouvrir l'une des instances et débuter le travail d'arbitrage.

![Liste des instances dans l'interface Ouali](/img/interface-liste-instances.png) 

Noter qu'il peut être nécessaire de faire défiler la liste des instances pour les afficher toutes.

## Interface d'arbitrage

Lorsque vous ouvrez une nouvelle instance, la fenêtre suivante s'affiche.

![Interface d'arbitrage Ouali](/img/interface-alignement.png) 

On remarque les éléments d'interface suivants (décrits plus en détail plus loin):

1. Liste des notices à traiter dans le référentiel source
2. Détail de la notice source en cours de traitement (sélectionnée dans la liste 1)
3. Détail de la notice candidate cible (sélectionnée dans la liste 4)
4. Liste des candidats automatiques proposés par Ouali
5. Onglet Recherche pour lancer une recherche manuelle dans le référentiel cible
6. Formulaire d'alignement
7. Barre de progression de l'instance active (nombres d’éléments avec ou sans correspondance et en attente d’arbitrage)
8. Menu d'aide et menu utilisateur (pour se déconnecter)
9. Retour à la liste des instances

Le processus d’arbitrage manuel consiste à sélectionner une notice source à traiter dans les liste des éléments à traiter (1) pour l’analyser (2) ensuite choisir l’entité cible correspondante (3) au moyen de la liste des candidats automatiques (4) ou au moyen d’une recherche manuelle (5). Une fois qu’une entité cible correspondante a été sélectionnée, ou qu’aucune entité cible correspondante n’a pu être identifiée, il est alors possible de définir le détail des informations de correspondance au moyen du formulaire d'alignement (6).

### Liste des notices à traiter

Cet élément d'interface contrôle quelle notice du référentiel source est sélectionnée pour traitement.

L'onglet "Attribués" s'affiche par défaut:

<img src="/oualidoc/img/interface-source-attribues.png" alt="Liste des notices attribuées" width="200px" style="float: left; margin-right:20px;"/>

Cette liste comporte les notices qui ont été attribuées automatiquement à l'usager actif. Les opérations suivantes sont possibles

1. Obtenir des notices attribuées supplémentaries (ajoutées en fin de liste)
2. Rejeter tous les éléments attribués et de recevoir un nouvel ensemble d’éléments attribués
3. Rejeter un élément spécifique et le renvoyer dans le lot général des notices à traiter. C'est l'option à choisir lorsqu'on n'est pas certain de la décision à prendre. La notice sera réattribuée à un autre usager.
4. Cliquer sur une notice dans la liste pour la sélectionner et l'afficher dans la partie 2 de l'interface.
5. Au-dessous de la liste des notices à traiter s'affichent les derniers éléments traités dans l'ordre chronologique inverse (dernière modification en haut de la liste). 

<br style="clear:both;"/>
En cliquant sur l'onglet "Tout" on accède à la liste de toutes les notices présentes dans le référentiel source actif. 

<img src="/oualidoc/img/interface-source-tout.png" alt="Liste de toutes les notices du référentiel source" width="200px" style="float: left; margin-right:20px;"/>

On peut ici 

1. rechercher une notice dans le référentiel source par texte ou avec son numéro de notice
2. ou naviguer la liste des notices avec les options de pagination.

Noter que les résultats d'une recherche s'affichent dans la page 1 de la liste. Lorsqu'on fait une recherche dans cet onglet, 
s'assurer que la page 1 est sélectionnée.

<br style="clear:both;"/>
#### Modifier un alignement

Il est possible de sélectionner une notice déjà traitée (dans l'onglet Tout et dans la liste des éléments traités)
et ainsi modifier une décision déjà prise (par exemple pour corriger une erreur).

### Détail de la notice source    

Détail de l’élément source en cours de traitement.

![Notice source en cours de traitement](/img/interface-tab-source.png) 

Les opérations suivantes sont possibles

1. Bouton permettant de basculter entre la vue MARC et l'affichage visuel de la notice source
2. Liste des notices bibliographiques liées et des correspondances existantes. Un clic droit sur l'une de ces notices affiche un menu contextuel avec les deux options suivantes
3. Voir la notice bibliographique liée au format MARC
4. Signaler que la notice d'autorité courante a été attribuée par erreur à cette notice bibliographique. Il peut arriver que l'on tombe sur un cas de figure où une notice d'autorité a été attribuée par erreur. On peut ainsi signaler une telle erreur pour qu'elle soit corrigée par la suite. Cette opératio a pour effet d'ajouter un sous-champ "vedette incorrecte".
5. Cette icône indique la catégorie de notice dont il s'agit (ici une notice de type lieu/géographique)
6. Numéro de la notice dans le référentiel source. C'est le numéro à noter si l'on relève une question ou un problème avec une notice particulière et qu'on souhaite le transmettre à quelqu'un. Ce numéro unique permet de retrouver la notice en question avec plus de certitude qu'avec la vedette.

### Détail de la notice cible   

Détail de la notice cible actuellement sélectionnée dans la liste 4. Les éléments d'interface sont ici identiques au panneau précédent (notice source), à l'exception du menu contextuel dans la liste des notices bibliographiques liées, qui n'est pas disponible ici.

### Liste des candidats

Liste des candidats proposés par Ouali. La petite icône affichée donne une indication du niveau de confiance attribué par Ouali à chacun des candidats affichés: confiance élevée (vert), confiance partielle (organge), confiance basse (rouge).

Cette liste n'est pas exhaustive, elle ne reprend que les candidats proposés par l'alogrithme d'Ouali. Pour rechercher l'ensemble du
référentiel cible, basculer dans l'onglet de recherche (section suivante).

### Recherche dans le référentiel cible

Lorsqu'aucun candidat proposé par Ouali n'est satisfaisant, une recherche manuelle dans le référentiel cible est souvent nécessaire.
Cette opération s'effectue dans l'onglet Recherche à côté de la liste des candidats:

![Interface de recherche dans le référentiel cible](/img/interface-recherche-cible.png) 

Les opérations suivantes sont possibles

1. Introduire ici la chaîne de caractères à rechercher. La recherche se fait immédiatement dès que l'on commence à taper du texte dans ce champ, il n'est donc pas nécessaire de taper "retour" pour lancer la recherche. La recherche se fait dans les formes principales et rejetées.
2. Les résultats retournés s'affichent ici. Cliquer sur un des résultats pour le sélectionner, les détails s'affichent alors dans le panneau de détail de la notice cible (numéro 3 dans la vue d'ensemble) et cette notice sera utilisée pour définir l'alignement.
3. Le type de notice s'affiche ici pour chaque résultat de recherche.
4. Par défaut, la recherche se fait dans tous les types de notice, mais il est possible de restreindre la recherche pour se cantonner à un type particulier. Par exemple, si on aligne des notices géographiques, il peut être utile de restreindre les résultats de recherche à ce type pour éviter de sélectionner par erreur une notice d'un autre type.

Quelques considérations à observer

* La recherche par texte n'est en principe pas sensible à la casse ni la ponctuation. L'ordre des mots peut jouer un rôle en revanche. Lorsqu'on ne trouve pas les résultats escomptés, il peut être utile d'essayer plusieurs permutations des mots pertinents.
* Faire également attention aux différences de graphie, de langue ou de translittération. Là encore, plusieurs essais sont parfois nécessaires avant de trouver la correspondance recherchée.
* Pour l'alignement vers IdRef, il peut être utile d'utiliser [l'interface de recherche native d'IdRef](https://www.idref.fr/) suivant la complexité de cas.
* Si on a l'identifiant d'une notice dans le référentiel cible (par exemple le numéro d'une notice IdRef trouvé lors d'une recherche dans leur interface web), il est possible de la retrouver en utilisant le même champ recherche. Une notice ainsi trouvée par identifiant s'affiche en bleu:

![Recherche par identifiant du notice cible](/img/interface-recherche-cible-id.png) 

### Panneau d'alignement (correspondance)

Lorsqu'on a trouvé une notice dans le référentiel cible vers laquelle on souhaite aligner la notice source sélectionnée,
ou qu'on s'est assuré qu'il n'y a aucune équivalence pour cette notice, on utilise ce panneau pour enregistrer cette décision.

La couleur de l’en-tête indique l’état d'alignement actuel de la notice source sélectionnée: bleu = aucune information de correspondance définie (en arbitrage), vert = alignement avec un élément cible défini, rouge = décision de non-alignement (rejet).

Après s'être assuré que la notice actuellement sélectionnée dans la liste des candidats (4 dans la vue d'ensemble) ou l'onglet 
recherche (5) est correcte, utiliser les options accessibles via le menu contextuel à côté du bouton "Définir" pour enregistrer la décision d'alignement:

![Actions rapides du panneau d'alignement](/img/interface-correspondance-actions-rapides.png) 

1. Cliquer sur la flèche à droite du bouton "Définir" pour accéder aux options d'enregistrement rapide
2. Choisir l'option "validation immédiate" pour enregistrer une décision d'alignement vers la notice cible sélectionnée (vert)
3. Choisir l'option "rejet immédiat" pour enregistrer une décision de non-alignement (rouge)

Ces deux options d'enregistrement rapides sont suffisantes pour la très grande majorité des cas.

Cependant, il peut être nécessaire d'afficher les détails d'un alignement, notamment lorsqu'on doit corriger un alignement existant.
Pour cela, cliquer sur le bouton "Définir" pour afficher l'interface détaillée:

![Interface détaillée du panneau d'alignement](/img/interface-correspondance-detail.png)

Les actions suivantes sont possibles dans cette interface:

1. Le bouton "+" permet d'ajouter la notice cible actuellement sélectionnée dans la liste des candidats à l'alignement en cours
2. Le bouton "-" permet de dissocier une notice cible déjà définie pour l'alignement en cours
3. Il est ici possible de définir des alignements de plusieurs types. **Dans le cadre du projet Ouali, on ne définit que des correspondances de type "exacte".**
4. Le niveau de confiance peut être spécifié ici. Cette fonctionallité n'est actuellement pas utilisée dans le cadre du projet Ouali.
5. Il est possible d'ajouter un commentaire spécifique à un alignement ici. Cette information n'est pas sauvegardée dans Alma et ne sert que pour le projet de migration vers IdRef. Ce champ peut être utilisé librement.
6. Utiliser l'icône disque pour enregistrer l'alignement tel que défini.
7. Utiliser le bouton "x" pour fermer la fenêtre d'alignement sans sauvegarder les changements.

Si aucune notice cible n'est ajoutée à la liste avec l'option "+" ci-dessus, l'alignement sera sauvegardé comme une décision de non-alignement (rouge). Si une notice cible est ajoutée, ce sera sauvegardé comme une décision d'alignement (vert).

À noter qu'il est techniquement possible d'aligner vers plus d'une notice cible, mais on n'utilise pas cette fonctionnalité dans le cadre du projet Ouali. **Vérifier qu'il y a bien une seule notice cible** avant de sauvegarder un alignement.

**Marche à suivre pour corriger un alignement erroné:**

1. Sélectionner la notice source avec un alignement à corriger
2. Sélectionner la notice cible correcte (s'il y en a une) dans la liste des candidats ou l'interface de recherche
3. Cliquer le bouton "définir" du panneau d'alignement pour en afficher l'interface détaillée
4. Retirer la notice cible erronnée au besoin avec le bouton "-"
5. Lier la notice cible correcte sélectionnée (s'il y en a une) avec le bouton "+" et vérifier que le type d'alignement soit bien "exacte"
6. Sauvegarder l'alignement

## Glossaire

Dans le cadre du projet Ouali, on définit les termes suivants

| Terme                  | Définition                                                                                                |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Alignement             | Un alignement est une équivalence exacte entre un terme du référentiel source et un terme du référentiel cible. Par exemple _Manche (tunnel)_ (rnv:010007214) --> _Manche, Tunnel sous la_ (idref:028049799) |
| Cible                 | Le référentiel _cible_ est le fichier d'autorité _vers lequel_ on définit un alignement. Par exemple, dans le cas d'un alignement des ATC vers IdRef, les ATC sont la _source_ et IdRef la _cible_. |
| Instance               | Le chantier d'alignement est séparé en plusieurs lots en fonction de la catégorie des termes d'autorité, les référentiels source et cible, et parfois le nombre de notices bibliographiques liées. À chaque lot ainsi défini correspond une instance Ouali. [Voir la liste des instances pour plus de détails.](chantiers#instances-ouali)|
| Référentiel            | Un référentiel est un des fichiers d'autorité avec lesquels on travaille. Rnv-mat, ATC et IdRef sont des référentiels. Voir aussi _source_ et _cible_.|
| Source                 | Le référentiel _source_ est le fichier d'autorité _à partir duquel_ on définit un alignement. Par exemple, dans le cas d'un alignement des ATC vers IdRef, les ATC sont la _source_ et IdRef la _cible_. |