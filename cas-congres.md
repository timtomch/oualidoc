---
title: Collectivités et congrès
parent: 3. Règles d'alignement
has_children: false
nav_order: 1
permalink: /congres
---

# Collectivités et congrès: cas particuliers

Cette page regroupe les procédures d'alignement à suivre pour traiter certains cas particuliers
qui peuvent intervenir dans les instances **collectivités et congrès**.
Ces procédures sont en cours de discussion par le groupe de travail Ouali et sont amenées à évoluer.

## Il n'y a pas d'équivalence exacte pour une année de congrès

Il s'agit ici de cas d'alignement de notices de congrès. La notice du référentiel source correspond
à une année précise de congrès, mais on ne trouve pas d'équivalent exact dans le référentiel cible.

**Consigne: aligner uniquement les équivalences exactes (lieu et année).** (décision GT IdRef 7.3.2022)

Si l'équivalence exacte n'existe pas, il faut définir un non-alignement (notice rouge). Ainsi une autorité sera créée dans le référentiel cible pour ajouter l'année manquante.

### Exemples

Voici quelques cas de figure qui peuvent se présenter:

* Le référentiel cible dispose de notices correspondant à d'autres années de ce congrès, mais pas l'année désirée. Après vérification, il n'y a pas non plus de notice générique pour ce congrès dans le référentiel cible.

| Source                                   | Cible                                                    |
| ---------------------------------------- | -------------------------------------------------------- |
| International James Joyce Symposium (7 : 1979 : Zürich) | James Joyce International Symposium 5 1975 Paris |
|                                          | International James Joyce Symposium 18 2002 Trieste, Italie |
|                                          | (aucune autre notice correspondante)       |

Décision: non-alignement (rouge)

* Le référentiel cible contient une entrée générique, ainsi que des entrées pour d'autres années du congrès que l'on souhaite aligner, mais pas pour l'année à laquelle correspond la notice source.

| Source                                   | Cible                                                    |
| ---------------------------------------- | -------------------------------------------------------- |
| Exeter Symposium (3 : 1984 : Dartington) | International Exeter symposium                           |
|                                          | International Exeter symposium 05 1992 Exeter, GB        |
|                                          | International Exeter symposium 07 2004 Charney Manor, GB |
|                                          | International Exeter symposium 08 2011 Charney Manor, GB |

Décision: non-alignement (rouge)

* Il existe une équivalence parfaite

| Source                                   | Cible                                                    |
| ---------------------------------------- | -------------------------------------------------------- |
| DARH 2005 (1 : 2005 : Yverdon-les-Bains) | Dextrous Autonomous Robots and Humanoids 1 2005 Yverdon-les-Bains, Suisse                           |

Décision: Alignement (vert)

## La notice source ne comporte pas le nom du congrès (incomplète)

Il peut arriver de rencontrer dans le référentiel source des notices de congrès incomplètes, pour lesquelles
seuls le lieu et/ou l'année sont spécifiées, sans autre détails (p.ex. nom du congrès). 
Il s'agit dans ce cas d'erreurs de catalogage ou d'importation d'anciens référentiels, et **la notice doit
être corrigée**.

**Consigne: mettre la notice de côté (cliquer sur - pour renvoyer la notice dans le panier des notices à traiter)** (décision GT IdRef 7.3.2022)

### Exemples

| Source                                   | Cible                                                    |
| ---------------------------------------- | -------------------------------------------------------- |
| USA Meeting (1999 : Washington, DC)      | ?                                                        |
| Congress (2003 : Lyon, France)           | ?                                                        |

Décision: déférer à un.e spécialiste. Renvoyer la notice dans le panier (gris)

## Il n'y a pas d'équivalence exacte pour la section d'une organisation

Certaines organisations ont des sections (ou chapitres) géographiques ou spécifiques à un sujet d'étude,
par exemple. Il peut arriver que le référentiel source dispose d'une notice spécifique à une telle
section, mais le référentiel cible n'a pas d'équivalence exacte.

**Consigne: s'il s'agit d'une organisation en lien avec la Suisse, indiquer les sections manquantes comme
non-alignement (notice rouge).** (décision GT IdRef 7.3.2022)

Si la notice n'a pas de lien avec la Suisse, on peut aligner vers une notice générique.

### Exemples

Voici quelques cas de figure qui peuvent se présenter:

* Le référentiel cible contient une entrée générique pour une organisation (faîtière) mais aucune pour ses sections. Il s'agit d'un organisme suisse.

| Source                                   | Cible                                                    |
| ---------------------------------------- | -------------------------------------------------------- |
| Oeuvre suisse d'entraide ouvrière. Vaud  | Schweizerisches Arbeiterhilfswerk                        |
|                                          | (aucune autre notice correspondante)                     |

Décision: non-alignement (rouge)

* Le référentiel cible contient des entrées pour d'autres sections de l'organisme que l'on souhaite aligner, mais pas pour la section à laquelle correspond la notice source. Il s'agit d'un organisme suisse.

| Source                                                | Cible                                       |
| ----------------------------------------------------- | ------------------------------------------- |
| Fédération suisse de gymnastique. Section de Montreux | Fédération suisse de gymnastique            |
|                                                       | FSG Fribourg (Suisse)                       |
|                                                       | FSG Fribourg-Ancienne (Suisse)              |
|                                                       | FSG Freiburgia (Fribourg, Suisse)           |

Décision: non-alignement (rouge)

(Ajouter un exemple de section non-Suisse)