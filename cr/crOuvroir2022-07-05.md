---
title: Réunion hebdomadaire
description: cr de la réunion hebodmadaire
author: ouvroir
date: 2022-07-05
draft: true
tags:
    - cr
    
---

# Rencontre hebdomadaire

## IIIF

Formation IIIF. Découverte de l’écosystème et des overlays. Réalisation d’une démonstration avec des fichiers .png

- make svg files
- get full sized canvas cutouts

William et Chatanya ont continué à explorer les différents viewers. Canvas-panel pas encore essayé car en React.
Duration viewer, pas trouvé la documentation.
Passé à OpenSeaDragon qui paraît présenter le plus de flexibilité.

La documentation de Universal Viewer n’est pas très accessible et très basique. Beaucoup de fonctionnalités mais comme elles ne sont pas très documentées cela est limitant.

Plusieurs difficultés ont été surmontées pour l’installation, mais d’autres problèmes ont été rencontrées avec les extensions.

Savoir si utiliser un framework javascript moderne est la bonne manière d’aborder la question. Peut-être plus intéressant de travailler avec des webcomponents qui seraient par la suite installés en Svelte.

Une rencontre avec Glen Robson qui a été très productive car elle a permis du debugging. Nous avons alors eu le sentiment d’être allés trop vites dans le code. Il était surpris que nous nous lancions si rapidement dans le code.


- ce qui existe est en react 
- autres formes d'interactions


--> Explorer Canvas-panel, à reproduire avec svelte ou avec un webcomponent natif.
- compatible v3?
- essayer de prototyper des interactions de base
- essayer la librairie [manifesto](https://iiif-commons.github.io/manifesto/)
- recheck the delft library iiif & bosch exhibitions: what's the stack, how does it work...
- richer interface for interaction from image to text and back (see video + two texts describing the project)
- full environment to explore and interact with the image
- extend a manifest? or is a manifest file even adapted to what we want to do

Kenan: storyboard d'interactions possibles puis voir comment on peut l'implémenter
- zoom
- rollover avec zones
- texte pour afifhcer des choses dans l'image
- viste guidée dans l'image
- (mettre en surbrillance)


William: web components.
- web components with Svelte ? 
- can web components be a solution for working with librairies that rely on window and document objects?
- overall feeling on working with web components? 

Need for technical documenation (in addition of blog-ish comparison of tools):
- tools vs compliance with IIIF versions + image formats (and image as annotations - svg, jpeg2000)
- tools vs general objective, "average user", roadmap
- tools vs technology stack to be used (can be used with modern js framework ? web components ?)
- tools vs **operations** (ie zoom, back and forth interaction from image to text)
    - operations should be listed as a reminder when comparing tools and examples. (from Emmanuel's writings in GDrive)
- tools vs examples
- tools retro-engineering

- defining procedure to export images (svg) and image annotations


## Cahier des charges *common*
séance de travail débu de la semaine prochaine

## Identité graphique 
CIẼCO
- développement du site web fin de l'été → octobre
- identité graphique reste très similaire à l'origine (mais bitonal)

Avancer pour Ouvroir? dès que c'est plus clair pour common