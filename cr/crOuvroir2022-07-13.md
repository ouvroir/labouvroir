---
title: Réunion hebdomadaire du 13 juillet 2022
description: Compte rendu de la réunion
author: ouvroir
date: 2022-07-12
draft: false
tags:
    - cr
    
---

# Rencontre hebdomadaire

## IIIF - Righettino

### Github Repositories
IIIF experiments, righettino-client, righettino-project ??

try to reduce the number of repositories as far as we can
Ideally two repos:
- `iiif-experiments`
- `righettino-project` or `righettino-client`
Be careful with the teams and projects organisation

documenting tools with a [template](https://github.com/ouvroir/righettino-project/tree/main/documentation) to describe them

Everything from righettino-project will be moved to IIIF Experiments. Righettino-client will be left free, waiting for a client.


### prototype with canvas-panel

Canvas-Panel from Digirati, allows lot of methods to have access to different viewers and manipulation. For instance, there are currently various version of the Presentation API. With Canvas-Panel, it’s possible to normalize a version 2 manifest.

Canvas-Panel is now developped as a webcomponents instead of a React components. It’s still a very early version and the documentation is sparse.

It was possible to experiment various things with it and it worked. Zoom in, zoom out, annotation highlighting. Looks like a good fit. It appears more useful than openSeaDragon.

To do:
- what is the status of atlas viewer (+license), and compare it with openSeaDragon
- contact Canvas Panel to figure what their roadmap is

Canvas-Panel can be see as a :
- a wrapper around a viewer. Not so painful to do. 
- manage iiif stuff (manifest conversions)
If you want a basic viewer don’t use Canvas-panel

Ne pas retenir Canvas-Panel pour les fonctionnalités génériques de conversions, etc. Mais plutôt pour la capacité à autoriser de riches interactions visuelles pour construire des expositions virtuelles.

Pas certain à quel point hackable.

- Document the dependancies and the licences of the product and Atlas (the viewer)
- Explore more about the customization
- Identify how much work for typical interactions

Kristine salue le travail de documentation en cours qui est très important pour le laboratoire et le domaine.


### web components 

A lot of debates are going on currently about web components. Depending you stay on the platform side or the framework side.

We must consider if we want to build svelte components or web components? 
web components allow interoperability between frameworks
svelte has an option to write svelte components and export them as web components


## CBC

Mauricio is not here today. We’ll discuss his work on the Mont D’or modeling next week.
Emmanuel is meeting with the French national archives tomorrow. 

## Common
<!--
où le reste de la recherche actuellement effectuée? 
Google drive marie et mélanie. Johanne? 
-->

### Zotero
statut compte ouvroir? 
- ok officieux de Johanne
- utiliser le FEI? 

vérifier comment ça fonctionne
créer des collections pour les étudiant·e·s de la formation? 

systeme de nommage: cieco- ...

Fréquences de backups? 
nb de bibliothèques
[issue](https://github.com/ouvroir/labouvroir/issues/132)

## Événements du labo
Programmation de l’année prochaine 


### Horaires
Kristine enseigne les lundis et les jeudis pm à l’automne
Emmanuel enseigne lundi pm à l’automne

Kristine enseigne les lundis pm et les jeudis am à l’hiver
Emmanuel en Europe à l’hiver donc est disponible les après-midi.

collaboratoires CIÉCO les vendredis probablement

plan individuel meetings with other labs

*Debug your humanities* avec Marcello et la crcen
- Emmanuel: XQuery
- Lena: Zotero, md+Git (ou séparés)

### Regular activities
keep tuesdays lab days
events: first two tuesdays of every month

par semestre: 
- 1 atelier 
- 2 midi-causeries

Kristine gives a talk in Dartmouth in August

### Midi-causeries automne

Invite guests for collaboration
Present projects


Septembre: midi-causerie lié au travail effectué avec les stagiaires MITACS pendant que Kenan est là? (avec Kenan et Chaitanya par Zoom)

- Antoine Courtin
- Valérie Angenot, UQAM (Sabbathique? )
- Nicola Camerlenghi, Dartmouth
- Tim Sherrat https://timsherratt.org (GLAM workbench)

### Atelier

begining of october : proposal → photogrammetry avec Kathrine Cook
- Collaborer avec Joel et/ou Patricia aussi? 
- scanner technes


### Special events
Social event for the back-to-school
- rentrée le 6 septembre
- proposition: 13 septembre **IT’S A DATE**

define lab open hours 

demos: 
- IIIF
- Zotero
- pretty pictures? 
emprunter un projecteur? 

IIIF Hackathon in winter

To do: 
- confirmer dates possibles avec Michael and Marcello @emchateau
- vérifier si Valérie prend une sabbatique @ktanton
- demander à Denis si on peut faire un midi-causerie Righettino-IIIF @emchateau
- breakfast meetings with other labs to consider at large