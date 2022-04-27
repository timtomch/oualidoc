---
title: 3. Règles d'alignement
has_children: none
nav_order: 3
permalink: /regles
---

# Règles d'alignement

Cette section décrit les règles à suivre lors de l'arbitrage des alignements dans Ouali. Les règles ci-dessous s'appliquent
à toutes les instances. Vous trouverez également une liste de cas particuliers à chaque instance dans les pages suivantes:

* [Collectivités et congrès](congres)

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

**IMPORTANT: En cas de doute:** ne prendre aucune décision et remettre la notice dans le lot des notices à traiter (cliquer sur le bouton "-").

Il est important de se rappeler de la différence entre un alignement à arbitrer (aucune décision prise, en gris dans Ouali) et un
non-alignement (en rouge). Le premier restera dans la pile des alignements à traiter jusqu'à ce que quelqu'un prenne une décision,
par exemple par un.e spécialiste du domaine s'il s'agit d'un cas complexe. Tandis qu'une décision de non-alignement indique qu'on est
certain qu'aucune équivalence n'existe et provoquera la création d'une nouvelle notice dans IdRef lors de la migration.

## Doublons dans le référentiel cible

Il peut arriver que l'on tombe sur des doublons dans le référentiel cible.
Dans ce cas, l'alignement ne doit être défini que vers **une seule notice cible** et les points suivants
sont à considérer pour choisir vers quelle notice définir l'alignement.

**Consigne:**
1. Si le référentiel cible est les **ATC**, choisir une notice cible au hasard, cela a peu d'importance.
2. Si le référentiel cible est **IdRef**, aligner en priorité vers la notice cible ayant le plus de notices bibliographiques en commun avec la notice source.
2. Sinon, aligner vers la notice cible ayant le plus de notices bibliographiques liées.
3. Sinon, aligner vers la notice cible la plus complète (p.ex. notes d'application)

Il n'est pas nécessaire de prendre note des cas de doublons rencontrés.

(décision GT IdRef 7.3.2022)