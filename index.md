---
layout: default
title: Introduction
nav_order: 1
description: "Documentation du projet Ouali de migration des autorités RenouVaud vers IdRef."
permalink: /
---

# Introduction

En 2021, la Coordination Renouvaud a entamé un projet de migration de registres d'autorités locales vers le référentiel IdRef.
Pour mener à bien ce projet, il est nécessaire d'aligner le plus possible de notices d'autorités locales (qu'on appelle référentiel
_source_) vers les notices équivalents dans IdRef (le référentiel _cible_). On identifie également les notices sources qui n'ont
pas d'équivalence dans IdRef, afin que l'on puisse ajouter celles-ci à IdRef lors de la migration.

L'outil **Ouali** a été développé pour mener à bien ce projet. Ouali remplit deux missions:

* Alignement automatique des notices d'autorité
* Aide à l'alignement manuel (arbitrage) lorsqu'un alignement automatique est impossible

Ouali utilise une combinaison d'algorithmes pour comparer les référentiels sources aux entrées dans IdRef et trouver des
équivalences exactes. En raison de règles syntaxiques, normes de translittération, conventions, traductions etc. différentes
entre les référentiels locaux et IdRef, la comparaison ne peut pas se borner à une équivalence exacte mais doit tenir compte
des formes rejetées, comparer différentes orthographes, permutation de termes, etc. Un score est calculé pour chaque candidat
ainsi identifié dans le référentiel cible. Lorsque ce score est supérieur à un certain seuil, Ouali considère l'équivalence comme
sûre et elle n'a donc pas besoin d'être validée. En revanche, un arbitrage manuel est nécessaire lorsque le score est inférieur
à ce seuil, lorsqu'il y a plusieurs possibilités, ou lorsqu'aucun candidat n'a été trouvé.

C'est là qu'entrent en jeu les professionnels prenant part au projet, aussi nommés **Oaulinautes**. Pour rendre le travail
d'arbitrage ou d'alignement manuel le plus simple et intuitif possible, Ouali réunit en une interface web les outils
nécessaires à cette tâche. C'est cette interface qui est ici documentée.

Cette documentation s'organise comme suit:

1. [Aperçu des étapes du chantier de migration vers IdRef](/chantiers)
2. Présentation de l'interface d'Ouali et des outils à disposition
3. Règles d'alignement
    3.1 Généralités
    3.2 Cas particuliers