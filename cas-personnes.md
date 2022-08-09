---
title: Noms de personne
parent: 3. Règles d'alignement
has_children: false
nav_order: 1
permalink: /personnes
---

# Noms de personne: cas particuliers

Cette page regroupe les procédures d'alignement à suivre pour traiter certains cas particuliers
qui peuvent intervenir dans les instances **noms de personne**.
Ces procédures sont en cours de discussion par le groupe de travail Ouali et sont amenées à évoluer.

## Spécificités du référentiel IdRef

Il faut être attentif au fait qu'IdRef contient des entrées de noms de personne de type "sujet", par exemple pour les personnages
historiques ou fictifs.

IdRef est le fichier d'autorité du Sudoc, qui est un catalogue collectif de bibliothèques de recherche et de l'enseignement supérieur en France. On va donc y trouver peu de personnalités étrangères de domaines non académiques (musiciens suisses, juristes suisses, etc.). Exemple : Jost, Felix, juriste suisse. Il y a peu de chance que l'on trouve un ouvrage de droit suisse dans le Sudoc.

Les règles de catalogage utilisés pour la création d'entrée dans IdRef diffèrent de celles utilisées dans les référentiels rnv-mat
ou ATC. Notamment, IdRef utilise la forme francisée pour les noms propres (p.ex. _Louis II roi de Bavière 1845-1886_) alors que les ATC
par exemple utilisent la langue d'origine (_Ludwig II, roi de Bavière_).

Pour plus de détails, [consulter la documentation IdRef](http://documentation.abes.fr/aideidref/accueil/fr/index.html).

## Attention aux homonymes

En général, on recommande de prêter une attention particulière aux notes d'application pour s'assurer qu'il s'agit
de la bonne personne: dates de vie, localisation géographique, discipline, etc.

Les notices bibliographiques liées peuvent également fournir des indices précieux sur la discipline d'un auteur particulier, etc.
S'il n'existe aucune notice bibliographique commune aux notices source et cible, une recherche sur le web ou sur Worldcat peut
être utile pour identifier les autres oeuvres d'un auteur particulier.

## Attention aux notices de type "auteur-titre"

Il est important d'aligner vers une notice cible de même type que la notice source. Ainsi, les notices de type "nom de personne"
ne doivent pas être alignées vers les notices de type "auteur-titre" que l'on trouve dans IdRef.

### Exemple

| Source                      | Cible                                                    |
| --------------------------- | -------------------------------------------------------- |
| Baudelaire, Charles         | Baudelaire, Charles 1821-1867 ([idref:026709635](https://www.idref.fr/026709635)) |
|                             | Baudelaire, Charles 1821-1867 Le Spleen de Paris ([idref:028640454](https://www.idref.fr/028640454))|
|                             | Baudelaire, Charles 1821-1867 Correspondances ([idref:034619933](https://www.idref.fr/034619933))|
|                             | ...                                                      |

**Décision:** Aligner vers le premier candidat car il s'agit de l'entrée d'autorité de type "nom de personne" pour Baudelaire. 
Les autres candidats correspondent à des oeuvres.

## Autorité "Nemo"

Il était d'usage au 19e siècle d'utiliser le pseudonyme "Nemo" lorsqu'un auteur souhaitait rester anonyme. Ainsi, l'appellation "Nemo"
se retrouve utilisée par plusieurs individus sans lien les uns avec les autres, il n'est donc pas opportun de créer une notice
d'autorité "Nemo" et d'y lier les ouvrages publiés de manière anonyme. Cependant, de telles notices ont quand même été créées par 
erreur, il faudra donc les supprimer lors du passage à IdRef. Pour simplifier cette procédure, **il est important de ne pas aligner
les notices "Nemo"**.

**Décision:** Ne pas aligner de telles notices mais les remettre dans le panier commun de notices à traiter (bouton "-").
