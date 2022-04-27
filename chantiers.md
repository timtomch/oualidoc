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

1. Registre ATC (notices d'autorité de noms de personne, collectivités et congrès)
2. Registre rnv-mat (autorités matière comportant noms de personne, collectivités, congrès, titres et lieux)

Pour les notices de type titre et noms de lieux, il suffit donc d'aligner le fichier rnv-mat vers IdRef. En revanche, pour les noms
de personne, collectivités et congrès, il est nécessaire dans un premier temps d'aligner les notices rnv-mat vers ATC avant d'aligner
ces dernières vers IdRef. Enfin, il faut aligner vers IdRef les notices rnv-mat pour lesquelles il n'y a pas d'équivalence dans les ATC.

On sépare les notices à aligner en fonction de leur catégorie, et des étapes intermédiaires d'alignement vers les ATC lorsque c'est
pertinent. Chacune de ces opérations d'alignement est représentée sous la forme d'une flèche dans le diagramme suivant

![Instances Ouali](/img/alignements.svg)

On remarquera que pour l'alignement de rnv-mat vers les ATC, on ne sépare pas les notices de type collectivités et congrès. Ceci est
dû au fait que les collectivités et congrès sont parfois utilisé de manière interchangeable dans les ATC (**À VÉRIFIER!**).

## Instances Ouali
Il y a environ 1.2 million de notices à traiter au total. On estime qu'Ouali est capable d'aligner automatiquement 60%-80% de cas, suivant la catégorie, ce qui laisse environ 200'000 notices à arbitrer manuellement.

Pour rendre le travail plus simple à gérer, les notices à traiter sont séparées par catégorie et étape d'alignement (vers les ATC
ou vers IdRef). Les lots les plus volumineux sont également subdivisés en fonction du nombre de notices bibliographiques liées
(occurences). On appelle _instances_ les lots de notices ainsi formés.

Voici la liste des instances à traiter. Le code décrivant chaque instance se retrouve dans le diagramme ci-dessus, suivi d'un chiffre
lorsqu'une instance est subdivisée en fonction du nombre d'occurences.

| Code      | Catégorie                | Chantier           | Occurences          | Notices (total) | À arbitrer (estim.) |
| ----------| -------------------------|--------------------|---------------------|-----------------|---------------------|
| RI-G      | Lieux                    | rnv-mat vers IdRef |                     | 19'116          | 6'500               |
| RI-T      | Titres                   | rnv-mat vers IdRef |                     | 4'336           | 700                 |
| RA-P1     | Noms de personne         | rnv-mat vers ATC   | occurences faibles  | 15'748          | 2'200               |
| RA-P2     | Noms de personne         | rnv-mat vers ATC   | occurences élevées  | 39'070          | 6'800               |
| AI-P1     | Noms de personne         | ATC vers IdRef     | occurences faibles  | 753'928         | 94'000              |
| AI-P2     | Noms de personne         | ATC vers IdRef     | occurences moyennes | 128'666         | 24'000              |
| AI-P3     | Noms de personne         | ATC vers IdRef     | occurences élevées  | 129'157         | 29'000              |
| RI-P      | Noms de personne         | rnv-mat vers IdRef |                     | 12'000 (est.)   | 2'000               |
| RA-C      | Collectivités et congrès | rnv-mat vers ATC   |                     | 13'502          | 4'400               |
| AI-C1     | Collectivités et congrès | ATC vers IdRef     | occurences faibles  | 82'747          | 33'000              |
| AI-C2     | Collectivités et congrès | ATC vers IdRef     | occurences élevées  | 12'934          | 5'600               |
| RI-ORG    | Collectivités            | rnv-mat vers IdRef |                     | 4'500 (est.)    | 1'000               |
| RI-CO     | Congrès                  | rnv-mat vers IdRef |                     | 3'000 (est.)    | 1'000               |

(état: avril 2022)