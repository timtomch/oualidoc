---
title: Noms de lieux géographiques
parent: 3. Règles d'alignement
has_children: false
nav_order: 3
permalink: /lieux
---

# Lieux: cas particuliers

Cette page regroupe les procédures d'alignement à suivre pour traiter certains cas particuliers
qui peuvent intervenir dans les instances **noms de lieux**.
Ces procédures sont en cours de discussion par le groupe de travail Ouali et sont amenées à évoluer.

## Formes historiques des noms de pays

Les règles d'indexation RERO/Renouvaud diffèrent des règles appliquées par IdRef. C'est notamment le cas pour les formes
historiques de noms de pays. Dans RERO, la convention est de créer une notice distincte lorsqu'un pays change de nom.
Dans IdRef, cela dépend si le changement de nom est accompagné d'une discontinuité territoriale. Selon [le guide d'indexation RAMEAU](https://rameau.bnf.fr/docs_reference/guide_rameau)
(page 209), _lorsqu'il y a une continuité de nom ou de territoire, la forme actuelle du nom est la seule retenue_
et les anciens noms sont spécifiés dans les formes rejetées.

Pour résoudre ce type de cas, il convient de vérifier les notes d'application et vérifier si la vedette de la notice source se
retrouve dans les formes rejetées de la notice cible.

**Consigne: respecter les normes d'indexation du référentiel cible (IdRef). Lorsqu'il y a continuité de nom ou de territoire, aligner vers la forme actuelle du nom d'un pays.** (décision RERO 4.5.2022)

### Exemple

| Source                                   | Cible                                                              | 
| ---------------------------------------- | ------------------------------------------------------------------ |
| Chine (république populaire)             | Chine ([idref:027633179](https://www.idref.fr/027633179))          |
| Chine                                    |                                                                    |

Décision: Dans ce cas de figure, les deux notices source sont à aligner vers la première notice cible. En-effet, même si la note
d'application RERO stipule l'utilisation de _Chine (république populaire)_ pour les documents traitant de la Chine après 1949,
cette distinction n'est pas faite dans IdRef car il y a continuité territoriale. Par ailleurs, on retrouve _Chine (réublique populaire)_
dans les formes rejetées de la notice cible _Chine_ ([idref:027633179](https://www.idref.fr/027633179)).

## Région géographique proche

On cherche toujours à aligner vers des équivalences exactes, il faut donc éviter les notices cibles proches mais qui ne
correspondent pas exactement aux notices sources. Dans le doute, consulter [le guide d'indexation RAMEAU](https://rameau.bnf.fr/docs_reference/guide_rameau).

**Consigne: toujours aligner vers l'équivalence exacte** (décision RERO 4.5.2022)

### Exemple

| Source                                   | Cible                                          | 
| ---------------------------------------- | ---------------------------------------------- |
| Amérique du nord -- ouest                | Pacifique, Côte du (Amérique du Nord)          |
| San Juan (Etats-Unis, bassin)            | San Juan Valley (Calif. ; vallée)              |

Décision: non-alignement (rouge) pour les deux cas ci-dessus car l'équivalence n'est pas exacte.

## Alignement vers une collectivité

Il peut arriver que l'on ne trouve pas de notice correspondante de même type (lieux). En étandant la recherche à d'autres
catégories, notamment les collectivités, on trouve ce qui semble être des candidats valables. 
En principe, **il ne faut pas aligner vers des notices d'autres types**
mais il convient de vérifier s'il ne s'agit pas d'une erreur dans la notice source.

**Consigne: toujours aligner une source de type lieu vers une cible de type lieu.** (décision RERO 4.5.2022)

### Exemples

Voici quelques cas de figure qui peuvent se présenter:

* Distinguer les subdivisions ecclésiastiques géographiques (lieux) des subdivisions hiérarchiques (collectivités)

| Source (Lieu)                            | Cible (Collectivité)                                                |
| ---------------------------------------- | ------------------------------------------------------------------- |
| Rome (Italie, province ecclésiastique)   | Diocèse de Rome ([idref:075686678](https://www.idref.fr/075686678)) |

Décision: non-alignement (rouge). La notice cible candidate ci-dessus (Diocèse de Rome) est de type collectivité alors que la notice
source est une entité géographique. Aucun autre candidat n'a été trouvé.

* Un diocèse est une subdivision hiérarchique (collectivité) mais peut avoir été entré par erreur comme un lieu

| Source (Lieu)            | Cible (Collectivité)                                                                  |
| -------------------------| ------------------------------------------------------------------------------------- |
| Rome (Italie, diocèse)   | Eglise catholique. Diocèse (Rome) ([idref:075686678](https://www.idref.fr/075686678)) |    
|                          | Église catholique. Diocesi (Rome) ([idref:031476015](https://www.idref.fr/031476015)) | 

Décision: Alignement vers le second candidat. Il s'agit dans ce cas d'une erreur lors de la création de la notice source dans RERO: 
la notice a été créée avec un type lieu alors qu'il aurait fallu utiliser
le type collectivité. De plus dans ce cas de figure, il y a un doublon dans le référentiel cible (IdRef)! Il convient d'appliquer
[les règles à suivre en cas de doublon](regles#doublons-dans-le-référentiel-cible) et aligner vers le deuxième candidat car (a) il y a
un plus grand nombre de notices bibliographique en commun avec celui-ci et (b) il s'agit de la notice la plus ancienne (identifiant
plus petit).

