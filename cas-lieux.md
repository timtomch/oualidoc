---
title: Lieux
parent: 3. Règles d'alignement
has_children: false
nav_order: 4
permalink: /lieux
---

# Lieux: cas particuliers

Cette page regroupe les procédures d'alignement à suivre pour traiter certains cas particuliers
qui peuvent intervenir dans les instances **noms de lieux**.
Ces procédures sont en cours de discussion par le groupe de travail Ouali et sont amenées à évoluer.

## Formes historiques des noms de pays

Les règles d'indexation RERO/Renouvaud diffèrent des règles RAMEAU appliquées par IdRef. C'est notamment le cas pour les formes
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

**Décision:** Dans ce cas de figure, les deux notices source sont à aligner vers la première notice cible. En-effet, même si la note
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

**Décision:** Non-alignement (rouge) pour les deux cas ci-dessus car l'équivalence n'est pas exacte. Pour le deuxième cas,
après vérification dans le guide RAMEAU, rien n'indique qu'un bassin recouvre une vallée, il s'agit donc bien de deux
concepts distincts.

## Lieux français et suisses

Vu qu'IdRef a en premier lieu été développé pour l'usage des bibliothèques françaises, les notices qu'il contient tendent à
être plus détaillée pour les lieux français par-rapport au registre Renouvaud. Il convient donc de prêter attention aux descripteurs
qui peuvent être plus précis dans le référentiel cible. Une recherche sur le web peut être utile en cas de doute (par exemple
pour vérifier dans quel département se situe une ville), en faisant attention aux homonymes.

### Exemple

| Source                  | Cible                                          | 
| ----------------------- | ---------------------------------------------- |
| Alba (France)           | Alba (Ardèche) ([idref:027630692](https://www.idref.fr/027630692))|

**Décision:** Alignement (vert). 

À l'inverse, les localités suisses sont en général moins présentes dans IdRef, surtout lorsqu'il s'agit de subdivisions politiques
comme les districts. Si l'équivalence parfaite n'est pas trouvée, il faut rejeter l'alignement pour ainsi créer de nouvelles
entrées dans IdRef au moment de l'import.

### Exemple

| Source                     | Cible                                          | 
| -------------------------- | ---------------------------------------------- |
| Aarau (Suisse, district)   | Aarau (Suisse ; région) ([idref:157139158](https://www.idref.fr/157139158))|

**Décision:** Non-alignement (rouge). 

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

**Décision:** Non-alignement (rouge). La notice cible candidate ci-dessus (Diocèse de Rome) est de type collectivité alors que 
la notice source est une entité géographique. Aucun autre candidat n'a été trouvé.

* Un diocèse est une subdivision hiérarchique (collectivité) mais peut avoir été entré par erreur comme un lieu.

| Source (Lieu)            | Cible (Collectivité)                                                                  |
| -------------------------| ------------------------------------------------------------------------------------- |
| Rome (Italie, diocèse)   | Eglise catholique. Diocèse (Rome) ([idref:075686678](https://www.idref.fr/075686678)) |    
|                          | Église catholique. Diocesi (Rome) ([idref:031476015](https://www.idref.fr/031476015)) | 

**Décision:** Alignement vers le second candidat. Il s'agit dans ce cas d'une erreur lors de la création de la notice source
dans RERO: la notice a été créée avec un type lieu alors qu'il aurait fallu utiliser
le type collectivité. De plus dans ce cas de figure, il y a un doublon dans le référentiel cible (IdRef)! Il convient d'appliquer
[les règles à suivre en cas de doublon](regles#doublons-dans-le-référentiel-cible) et aligner vers le deuxième candidat car (a) il y a
un plus grand nombre de notices bibliographique en commun avec celui-ci et (b) il s'agit de la notice la plus ancienne (identifiant
plus petit).

* Pour les parcs nationaux, il existe des autorités de type lieu et de type collectivité

Celles-ci ne sont pas interchangeables! En-effet, le guide RAMEAU admet que le même nom peut recouvrir plusieurs entités.
Ainsi on distingue le Parc National Suisse en tant que lieu, du Parc National Suisse en tant qu'institution vouée à la protection
de ce dernier.

| Source (Lieu)                                    | Cible                                                       |
| ------------------------------------------------ | ------------------------------------------------------------------- |
| Parc national des Ecrins (France, parc national) | Écrins (France ; Parc national des) ([idref:182441245](https://www.idref.fr/182441245)) - type **Lieu** |
| Parc national suisse (Suisse, parc national)     | Parc national suisse ([idref:06707202X](https://www.idref.fr/06707202X)) - type **Collectivité** |

**Décision:** Uniquement aligner les notices de type lieu vers une notice correspondante de même type! Dans les exemples ci-dessus
on alignera (vert) le parc national des Écrins car il existe une notice de type lieu correspondante. Par contre, on prendra une
décision de non-alignement (rouge) pour le Parc national suisse, car il n'existe pas de notice correspondante de type lieu
dans IdRef (celle qui existe est de type collectivité).

## Noms géographiques non-localisés (transfrontaliers)

En règle générale, selon les règles RAMEAU (section 2.3.3 page 214)

* On ne localise pas les noms géographiques qui excèdent les limites d'un État
* Cependant, on peut localiser les parties nationales d'entités transnationales **sauf pour les cours d'eau**.

### Exemples

| Source                                  | Cible                                                         | 
| --------------------------------------- | ------------------------------------------------------------- |
| Kurdistan (région transfrontière)       | Kurdistan ([idref:027367533](https://www.idref.fr/027367533)) |
|                                         | Kurdistan (Turquie) ([idref:027840336](https://www.idref.fr/027840336)) |
|                                         | Kurdistan (Iran) ([idref:02784031X](https://www.idref.fr/02784031X)) |

**Décision:** Alignement (vert) vers le premier candidat (Kurdistan), vu qu'il s'agit du descripteur recouvrant toute la région
du Kurdistan.

| Source                                  | Cible                                                         | 
| --------------------------------------- | ------------------------------------------------------------- |
| Kurdistan (Iran)                        | Kurdistan (Iran) ([idref:02784031X](https://www.idref.fr/02784031X)) |
|                                         | Kurdistan ([idref:027367533](https://www.idref.fr/027367533)) |
|                                         | Kurdistan (Turquie) ([idref:027840336](https://www.idref.fr/027840336)) |

**Décision:** Alignement (vert) vers le premier candidat (Kurdistan (Iran)), vu qu'il s'agit ici d'un descripteur ne recouvrant que la
portion iranaise du Kurdistan.

| Source                                  | Cible                                                         | 
| --------------------------------------- | ------------------------------------------------------------- |
| Rhône (cours d'eau) -- France           | Rhône (cours d'eau) ([idref:027242692](https://www.idref.fr/027242692)) |

**Décision:** Alignement (vert) même si le descripteur "France" est perdu. En-effet, selon les règles RAMEAU, les cours d'eau
ne sont pas localisés.

| Source                                  | Cible                                                         | 
| --------------------------------------- | ------------------------------------------------------------- |
| Rhône (vallée) -- Suisse                | Rhône, Vallée du (Suisse) ([idref:028236424](https://www.idref.fr/028236424)) |
|                                         | Rhône, Vallée du (France) ([idref:030982634](https://www.idref.fr/030982634)) |
|                                         | Rhône, Vallée haute du (France) ([idref:085647276](https://www.idref.fr/085647276)) |

**Décision:** Alignement (vert) vers le premier candidat. Dans ce cas, il s'agit d'une formation géographique transnationale
(vallée du Rhône et non le cours d'eau lui-même) subdivisée en parties nationales, il est donc pertinent d'aligner vers les 
mêmes subdivisions.


## Sites archéologiques et autres cas complexes

**Dans le doute, s'abstenir!** Il peut arriver que l'alignement ne soit pas évident à moins d'être un.e spécialiste du domaine. Si
un doute subsiste sur un alignement, il est toujours préférable de le renvoyer dans le panier commun (bouton "-") et laisser à
un.e spécialiste le soin de s'en charger.

### Exemple

| Source                                  | Cible                                          | 
| --------------------------------------- | ---------------------------------------------- |
| Thèbes (Egypte) -- Tombeau de Sen-nefer | Cheikh Abd el-Gournah (Égypte ; site archéologique) Tombe de Sennefer |
|                                         | Cheikh Abd el-Gournah (Égypte ; site archéologique) Tombe de Sennéferi |
|                                         | Deir el-Médineh (Égypte ; site archéologique) Tombe de Sen Néfer et Néfertari |

**Décision:** À moins d'être spécialiste et pouvoir déterminer de manière certaine vers quelle notice aligner, 
remettre la notice dans le panier commun de notices à traiter (bouton "-").