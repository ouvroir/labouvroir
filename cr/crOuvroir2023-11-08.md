---
title: Réunion hebdomadaire du 8 novembre 2023
description: Compte rendu de la réunion
author: ouvroir
date: 2023-11-08
draft: false
tags:
    - cr
---

Ordre du jour :

- calendrier, invitations, ateliers
- reframe
- common

## calendrier

### Midi-causerie

Andrea Gozzi présent aux portes ouvertes a travaillé sur des applications muséales sur l’intégration du son dans les expositions. Il pourrait venir en parler.

Par ailleurs, en réunion de laboratoire on avait envisagé plusieurs invitations possibles
- Andrea Gozzi (fin décembre)
- Léa Saint-Raymond (fin janvier)
- Schonagen (février)
- Talitha > Brésil (mars)
- Pierre-Carl Langlais (avril)
- Johanna Daniel (mai-juin)

### Autres événements

Atelier segmentation avant le départ de Léa.

Atelier Expot avec Marie fin décembre (Semaine 20)

## Commons

Josselin Morvan, disponible à partir de janvier.

Un gros du travail qui concerne l’intégration avec Zotero.

## Expot

Point d’information à William sur l’avancement du projet. Construction d’une ontologie.

## Reframe

Un projet Svelte a été mis en place. Pour faire des tests, une première étape pourrait consister à développer des composants Svelte. Une telle solution pourrait immédiatement permettre de tester la question de l’accessibilité de pouvoir faire appel à des ressources IIIF (pour les métadonnées), en se focalisant sur ce qui s’affiche dans une page avec du texte. Identifier un premier vocabulaire pour les composants et les propriétés.

Passer en web component impose seulement de builder différemment les objets et leur intégration dans le projet. Dans l’absolu le développement des webcomponents devrait être externalisé. Il paraît donc logique pour prototyper de pouvoir travailler dans un environnement plus confortable.

Un repo est dédié à l’élaboration d’une bibliothèque de composants Svelte. Un projet SvelteKit pourrait faire appel à ces composants.

- Textes, liste d'images (IIIF ?)
- Layouts


Premier problème, orientation de l'image.
En fonction du de l'orientation (portrait, paysage), adapter la grille pour le placement de l'image

Formats classique des images photos 
- 4:3
- 16:9
- 4:5
- 5:7
- 4:3
- 3:5
- 3:2
- 1:1


Dans un premier temps, penser des images dans une flexbox. 
Tout à la même hauteur ou tout à la même largeur.

Préoccupation des collègues : layout cf catalogue accrochage, biennal 

Image
- légende à deux niveaux
- conteneur
- orientation et comportement en fonction

