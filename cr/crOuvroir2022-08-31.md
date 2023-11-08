---
title: Recontre IIIF - Bibliothèques
description: cr de la rencontre avec Martin
author: ouvroir
date: 2022-08-31
draft: false
tags:
    - cr
    - IIIF
    
---

# Rencontre IIIF - Bibliothèques

## Common
Création d'un serveur d'image
→ du bac à sable à serveur IIIF pour Common (et Righettino)
- module des archives ouvertes pour qu'elles deviennent des dépôts opérables pour les images
- projet pilote en autonomie, voir ensuite si ça intéresse PORTAGE
- support ou conseil sur des solutions techniques

indépendemment des questions dêxpositions numériques, besoins de la plateforme Common pour mettre en commun les contenus historiques et sources documentaires + publication d'une encyclopédie numérique

dépôt d'image 
- visionner une image
- associer des métadonnées dans Common (pas de gestion des métadonnées dans Common)


Bibliothèques: 
Partent des métadonnées aux bib. Callypso (ContentDM).
Veulent sortir du modèle en séparant les métadonnées du modèle de données.
Mais abordent les choses depuis les métadonnées car central et ne peuvent pas se planter là-dessus. Doivent faire avec les outils en place, ne se lanceront pas dans du développement. Ne sait donc pas jusqu’à quel point va y arriver.

images: stockage, préservation, services (IIIF)
Pas seulement du stockage brut mais associer des services autour de ça.

Là où doivent se poser des questions, à qui cela est destiné. Les bibliothèques ont deux types de collections :
- celles dans Calypso
- offre de soutien à la recherche (un peu théorique, ne peuvent pas supporter toute la recherche à l’UdeM)
Pour ce deuxième volet, cherche donc à mettre en place quelque chose qui permette un simple drag and drop d’une image dans une interface et qui permette, sans avoir à renseigner trop de métadonnées, d’offrir des services de base. Quelque chose qu’aimerait garder car lorsque l’on numérise des collections, il y a un travail sur les collections qui ne permet pas de les publier d’emblée. Il aimerait que déjà puisse avoir des services.

Pb que ContentDM qu’un seul mode de stockage. Pour lui pas compatible.

Exemple de Nakala en France. Quid de FRDR ou DATAVERSE

stockage robuste, pas de risque / stabilité des identifiants et des URLs
Ce qui a été décalé à une seconde phase, l’aspect préservation pour une partie des collections. Ne s’attend pas à l’offrir pour des collections externes. Avec des outils pour valider les contenus.

éditions numériques ne sont pas publiées par des éditeurs, devraient aller dans des bibliothèques, devient "leur" collection

service tiers des bibliothèques pour le dépôt d'image
- envisageable pour l'été 2023
- l'intermédiaire d'une API, dépôt par le client Common (qui permettra de saisir des métadonnées)
- revalider pour s'assurer qu'il n'y a pas d'angles morts
- question de la gestion des droits (consultation)

Sont intéressés par le fait de disposer de ces cas d’usages
Pb de la gestion des droitss. Traditionnellement en bibliothèques deux cas de figure : 
- diffusé à tout le monde
- diffusion bibliothèque udem
Voudraient aller plus loin. Mais ne saurait pas faire pour des collaborateurs musées, ou autres, etc.

*qu'en est-il des archives confidentielles à Mélanie? Ce serait le genre de chose qu'elle ne numériserait pas?*

D’ici l’été prochain, travaillent sur deux volets en parallèles : l’infrastructure de stockage et l’évolution et remplacement de la couche métadonnées
Récemment, à la suite d’une discussion avec les TI, ont appris qu’ils allaient signer une entente cadre avec Amazon pour le cloud. Permettra de disposer de toutes sortes de services. Nous évitera de le faire de notre côté. Facilité de souplesses.
Pourquoi Amazon et non CalculQuébec? Pas les ressources ni leur mission de gérer ça

Remplacement de la couche métadonnées ContentDM. Envisage de choisir d’ici les fêtes pour plannifier d’ici l’été prochain nouveau stockage. Au tournant des fêtes sauraient quelles technologies utiliser, etc.

Pas une migration très complexe à faire.
Si remplacer contentDM pour Calypso petit. Mais l’idée ici, construire pour l’avenir avec d’autres partenaires et services. Facile de trouver des remplacement. Critère pas remplacer ContentDM mais pouvoir aller plus loin à l’avenir.

décrire le service et le type d'interface qu'on voudrait avoir pour évaluer la faisabilité


## Atelier
proposer atlier/hackathon IIIF Atkins le 29 novembre, à suivre
- requêtes sparql pour traiter le contenu savant - collègue de sciences ou biologie
- expo numérique
- importance de la préparation en amont: arriver à quelque chose de défini côté technique pour favoriser les conversations
- sur quelle période? 3x 1/2 journée? 

<!-- hackathon de la crcen
"Navigations anthologiques: l'Anthologie grecque à l'ère des Digital Classics", taking place from the 27th to the 29th of
October).
-->

Canadiana: McCord, MNBAQ
Harvard, plusieurs outils faciles et documentation pour les profs pour intégrer du contenu pour les prof.

intérêt pour les bibliothèques:
- moins dans le codage que le processus
- résultat: à partir de l'ouvrage rendu disponible, voici ce qu'on a pu produire

Bibliothèque prévoit organiser une journée en interne autour des initiatives à venir
Comité de direction dans 2 semaines.
Rapport d’un groupe de travail sur la numérisation.

Projet FCI avec le CRIHN et les bibliothèques tourné vers la numérisation, diffusion et visualisation

Martin va nous envoyer son architecture cible 

Rapport du groupe de travail sur la numérisation très centré sur les collections.

## Suivi 
Invitation aux portes ouvertes et aux fika.

Se revoir quand on est prêts à détailler les services qu'on aimerait avoir (description fonctionnelle)