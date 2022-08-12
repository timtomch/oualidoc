---
title: 3. Règles d'alignement
has_children: true
nav_order: 4
has_toc: false
permalink: /regles
---

# Règles d'alignement

Cette section décrit les règles à suivre lors de l'arbitrage des alignements dans Ouali. Les règles ci-dessous s'appliquent
à toutes les instances. Vous trouverez également une liste de cas particuliers à chaque instance dans les pages suivantes:

* [Noms de personne](personnes)
* [Collectivités et congrès](congres)
* [Titres](titres)
* [Noms de lieux géographiques](lieux)

Ces procédures sont en cours de développement et restent à discuter par le groupe de travail Ouali.
Elles sont donc amenées à évoluer.

## Généralités

Le but du projet est de remplacer les référentiels existants par IdRef. On cherche donc à remplacer chaque notice d'autorité
existante par **son équivalent exact dans IdRef**. Lorsque ce n'est pas possible, il faut dans tous les cas prendre une décision
de non-alignement (rouge). Cela provoquera la création d'une nouvelle notice dans IdRef lors de la migration.

**S'il existe un équivalent exact:** établir l'équivalence (en vert) de type "exacte" entre la notice du référentiel source et celle
du référentiel cible. Par exemple, aligner _Manche (tunnel)_ vers _Manche, Tunnel sous la_.

**S'il existe un équivalent proche ou similaire:** prendre une décision de non-alignement (rouge). Par exemple si _Ormont-Dessus (Suisse, VD)_ n'a pas d'équivalence dans le référentiel cible, il faut choisir l'option "aucune correspondance" plutôt que de l'aligner vers 
le terme existant _Les Ormonts (Suisse)_.

**S'il n'existe aucun équivalent:** prendre une décision de non-alignement (rouge). Par exemple si _Glärnisch (Suisse, mont)_ n'a
aucune équivalence dans le référentiel cible, il faut choisir l'option "aucune correspondance".

**IMPORTANT: En cas de doute:** ne prendre aucune décision et retirer la notice du lot des notices attribuées (cliquer sur le bouton "-" dans [la liste des notices à traiter](interface#1-liste-des-notices-%C3%A0-traiter).):

<img src="/oualidoc/img/interface-retirer-alignement.png" alt="Retirer une notice de la liste des notices à traiter" width="200px"/>

Il est important de se rappeler de la différence entre un alignement à arbitrer (aucune décision prise, en gris dans Ouali) et un
non-alignement (en rouge). Le premier restera dans la pile des alignements à traiter jusqu'à ce que quelqu'un prenne une décision,
par exemple par un.e spécialiste du domaine s'il s'agit d'un cas complexe. Tandis qu'une décision de non-alignement indique qu'on est
certain qu'aucune équivalence n'existe et provoquera la création d'une nouvelle notice dans IdRef lors de la migration.

## Doublons dans le référentiel cible

Il peut arriver que l'on tombe sur des doublons dans le référentiel cible.
Dans ce cas, l'alignement ne doit être défini que vers **une seule notice cible**. Pour choisir vers quelle notice définir l'alignement, il faut comparer leurs identifiants.

L'alignement se fait vers la notice cible ayant l'identifiant le plus petit (c'est-à-dire la plus ancienne).


### Exemple

| Source                      | Cible                                                                                  |
| --------------------------- | -------------------------------------------------------------------------------------- |
| Vagaggini, Cyprien          | Vagaggini, Cipriano 1909-1999 ([idref:195300351](https://www.idref.fr/195300351))      |
|                             | Vagaggini, Cyprien bénédictin 1909- ([idref:077449681](https://www.idref.fr/077449681))|

**Décision:** Aligner vers la seconde cible (idref:077449681). Comme son identifiant est plus petit, elle a été créée avant la seconde.

Il faut suivre cette consigne, même si la notice plus récente est plus riche et mieux documentée !

## Autorités ambigües ("pots communs")
Certaines notices d'autorité sont liées à des documents qui n’ont a priori pas de lien entre eux. 

Exemple : L’autorité « Sabine Rey » regroupe des documents traitant d’au moins trois domaines différents :

    Derborence, la nature et les hommes : treize randonnées commentées / Rey, Sabine / 991000227679702852
    Effets de la photobiomodulation sur la récupération sportive chez les athlètes / Rey, Sabine / 991021429997502852
    Réflexions sur les relations affectives enfants-éducateurs / Rey, Sabine / 991007774739702852

Cela est dû à une ancienne pratique où l'identité de la personne (ou autre entité) n'était pas vérifié et où l'on se contentait de reprendre une forme, même si elle ne correspondait pas. On appelait cette pratique les "pots communs".

Dans ce genre de cas, on va trouver dans IdRef plusieurs autorités possibles. Il faut choisir celle qui partage le plus grand nombre de notices liées communes.

Il faut également signaler les notices liées erronées en utilisant la fonctionnalité "Signaler une vedette incorrecte":
1. Placer le curseur sur la notice bibliographique voulue.
2. Faire un clic-droite.
3. Choisir "Signaler une vedette incorrecte".

Ouali ajoute un sous-champ $$5 à la vedette incorrecte. Elle sera modifiée ultérieurement.
