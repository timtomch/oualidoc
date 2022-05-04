---
layout: default
title: 1. Étapes du chantier
nav_order: 2
description: "Étapes du chantier de migration vers IdRef"
permalink: /chantiers
---
# Étapes du chantier de migration vers IdRef

Les notices à aligner sont séparées en 5 catégories:

1. Noms de personne (abrégés P)
2. Collectivités (ORG)
3. Congrès (CO)
4. Titres (T)
5. Noms de lieux géographiques (G)

De plus, il y a deux fichiers distincts à aligner:

1. Registre ATC (fichier RERO de notices d'autorité de noms de personne, collectivités et congrès et titres)
2. Registre rnv-mat (autorités matière comportant noms de personne, collectivités, congrès, titres et lieux)

Pour les notices de type titre et noms de lieux, il suffit donc d'aligner le fichier rnv-mat vers IdRef. En revanche, pour les noms
de personne, collectivités et congrès, il est nécessaire dans un premier temps d'aligner les notices rnv-mat vers ATC avant d'aligner
ces dernières vers IdRef. Enfin, il faut aligner vers IdRef les notices rnv-mat pour lesquelles il n'y a pas d'équivalence dans les ATC.

On sépare les notices à aligner en fonction de leur catégorie, et des étapes intermédiaires d'alignement vers les ATC lorsque c'est
pertinent. Chacune de ces opérations d'alignement est représentée sous la forme d'une flèche dans le diagramme suivant

![Instances Ouali](/img/alignements.svg)

On remarquera que pour l'alignement de rnv-mat vers les ATC, on ne sépare pas les notices de type collectivités et congrès. Ceci est
dû au fait que certains congrès ont une entrée principale de type collectivité. Vu qu'Ouali utilise cette information lors de la
définition des instances, il n'est actuellement pas possible de séparer les collectivités des congrès dans les ATC.

Il est également à noter qu'on ne fait actuellement pas d'alignement via les ATC pour les notices de type titre. Ceci est dû à une
situation particulière aux titres dans le fichier ATC (certains titres de série ont été ajoutés au fichier d'autorité lors de la
migration initiale vers Alma). En effet, IdRef n'utilise pas d'autorités titre pour le catalogage formel.

## Spécificités des référentiels

### ATC
Le référentiel ATC est utilisé par Renouvaud et a été créé dans le cadre de RERO il y a plus de 20 ans. Son nom provient du fait 
qu'il contient des notices d'autorité de type Auteurs, Titres et Collectivités.
Lors de la création de Renouvaud en 2016, le réseau vaudois a repris ce fichier à son compte, en le développant de son côté et sans 
synchronisation avec le fichier RERO.

De par sa nature romande, le référentiel ATC comporte de nombreuses spécificités régionales. On s'attend à ne pas trouver une notice
cible dans IdRef pour ces notices spécifiques au contexte vaudois. Celles-ci seront créées dans IdRef lors de la migration.

### IdRef
Le référentiel IdRef est surtout utilisé dans des bibliothèques universitaires et de recherche, principalement en France et de plus
en plus dans d'autres contextes francophones. Par conséquent, on s'attend à y trouver des notices assez pointues (par exemple le nom
de doctorants français), par contre les
entrées spécifiques au contexte romand, voire suisse ou germanophone en général, sont plus rares. RERO a commencé à ajouter de telles
notices dans IdRef. Les instances Ouali sont mises à jour régulièrement avec les alignements ainsi fournis par RERO, mais il est 
possible qu'il y ait un délai entre la dernière mise à jour et de telles créations récentes. Il ne faut donc pas s'étonner si on
trouve dans IdRef des alignements "évidents" qui n'ont pas été identifiés par l'algorithme d'Ouali.

Pour plus de détails, [consulter la documentation IdRef](http://documentation.abes.fr/aideidref/accueil/fr/index.html) ou
[le guide d'indexation RAMEAU](https://rameau.bnf.fr/docs_reference/guide_rameau).

## Instances Ouali
Il y a environ 1.2 million de notices à traiter au total. On estime qu'Ouali est capable d'aligner automatiquement 60%-80% de cas, suivant la catégorie, ce qui laisse environ 200'000 notices à arbitrer manuellement.

Pour rendre le travail plus simple à gérer, les notices à traiter sont séparées par catégorie et étape d'alignement (vers les ATC
ou vers IdRef). Les lots les plus volumineux sont également subdivisés en fonction du nombre de notices bibliographiques liées
(occurences). On appelle _instances_ les lots de notices ainsi formés.

Voici la liste des instances à traiter. Le code décrivant chaque instance se retrouve dans le diagramme ci-dessus, suivi d'un chiffre
lorsqu'une instance est subdivisée en fonction du nombre d'occurences.

| Code      | Catégorie                | Chantier           | Occurences          | Notices (total) | À arbitrer (estim.) |
| ----------| -------------------------|--------------------|---------------------|----------------:|--------------------:|
| RI-G      | Lieux                    | rnv-mat vers IdRef |                     | 19'116          | 6'500               |
| RI-T      | Titres                   | rnv-mat vers IdRef |                     | 4'336           | 700                 |
| RA-P1     | Noms de personne         | rnv-mat vers ATC   | occurences faibles  | 15'748          | 2'200               |
| RA-P2     | Noms de personne         | rnv-mat vers ATC   | occurences élevées  | 39'070          | 6'800               |
| AI-P1     | Noms de personne         | ATC vers IdRef     | occurences faibles  | 753'928         | 94'000              |
| AI-P2     | Noms de personne         | ATC vers IdRef     | occurences moyennes | 128'666         | 24'000              |
| AI-P3     | Noms de personne         | ATC vers IdRef     | occurences élevées  | 129'157         | 29'000              |
| RI-P      | Noms de personne         | rnv-mat vers IdRef |                     | (est.) 12'000   | 2'000               |
| RA-C      | Collectivités et congrès | rnv-mat vers ATC   |                     | 13'502          | 4'400               |
| AI-C1     | Collectivités et congrès | ATC vers IdRef     | occurences faibles  | 82'747          | 33'000              |
| AI-C2     | Collectivités et congrès | ATC vers IdRef     | occurences élevées  | 12'934          | 5'600               |
| RI-ORG    | Collectivités            | rnv-mat vers IdRef |                     | (est.) 4'500    | 1'000               |
| RI-CO     | Congrès                  | rnv-mat vers IdRef |                     | (est.)3'000     | 1'000               |

(état: avril 2022)