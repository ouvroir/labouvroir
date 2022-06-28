---
title: Réunion hebdomadaire
description: cr de la réunion du
author: ouvroir
date: 2022-05-
draft: true
tags:
    - cr
---

# Réunion hebdomadaire
- william
- daniel


## Processus décisionnaire pour l’aménagement

Locaux partagé CRIHN + Ouvroir
3 décisions:
- Ouvroir = Emmanuel + Kristine
- validation CRIHN (Michael) + Partenariat CIÉCO (Johanne)
    - décisions esthétiques, mobilier
    - pas besoin pour le suivi des décisions

Préparation dossier de recherche et d'inspiration aménagement au sein de l'ouvroir, présentant deux scénarios possibles, puis valider premières pistes avec Michael et Johanne

### Mobilier 

3-4 postes de travail pour le labo

Salle de conférence, 12-14 places

possibilité de faire la salle en avant aussi si on peut (voir si on peut demander un surplus)

NB: on doit rendre les tables de la salle de séminiaire avant la rentrée


## Tour d’horizon

### Travaux d’aménagement
combien pour refaire l'ouverture pour la porte coulissante + plafond suspendu (attention tuyeau circulation)

Demander une confirmation écrite au deux partis (confirmer par mail le compte-rendu de la réunion pour le valider)
Rédiger courriel pour envoyer aux deux partis.

- privilégier l'option de la poutre posée sur les murs (et éventuellement le poteau) plutôt que de la fixer au plafond
- réduire l'écart avec le plafond si possible pour limiter la menuiserie (à condition que ce soit la meilleure solution pour le faux plafond)
- bien avoir le même diamètre milieu à milieu de la grande vitre ou de celle qui prendra la place 

store: 
- soit on complète avec les mêmes modèles
- soit on en fait des éléments pour donner du peps au local, jouer sur la couleur 
On reste sur du blanc? 
pas de store entre 


profiter de l'été pour déménager les placards (contenu appartient au dépt de littératures et langues du monde)
- option 1: convenir de faire un tri et on vire ce qui ne l'est pas (classeurs vides, documents en double) → préparation de ce qu'il faut mettre aux archives
- option 2: leur demander de le faire, mais question de quand? 
service des archives de l'Université
- rédiger un courriel pour demander au Département de littératures et langues du monde s'il préfère s'en charger ou si on e fait. 

### Perspectives sur les développements techniques

William: test de Svelte comme framework de front-end javascript avec le travail sur Conbavil 

Quelle est la charge du labo en terme de développement ? 
- calendrier
- ressources, avec svelte kit, réutiliser les css 
- prototypage
- outils qui ne sont pas dans le cadre du FCI
- site web du labo
- collaboratoires: statistiques des collections des musées
- expérimentations: recherche et développement
- CSS pour ce qui n'a pas de design (pour le moment)

Stratégie pour les développements: externaliser les services, bien faire attention à conserver les rabais

se concentrer, à l'interne, sur les choses difficiles à externaliser

Briques à externaliser
- identification pour l'ensemble du proet CIÉCO, composant indépendant en svelte kit
- connexion avec API
- fonctions dashboard
- interaction avec API et création de nouvelles entités

Développeur recruté pour le projet CIÉCO (Paul) est prêt à faire du svelteKit. Externaliser, mais dans un environnement qu'on maîtrise. Limiter les dépendances, avoir un système maîtrisable

Site du labo, actuellement en Astro: homogénéiser ? unification des technologies
- Volonté d'essayer Astro et svelte kit en même temps
- conclusion de l'expréience: Emmanuel est plus content de Svelte que d'Astro, mais il est satisfait du résultat du site du labo
- ajouts, exemple calendrier, le faire en svelte dans Astro 

Expérimentations avec IIIF → mène au produit reframe

Design dev avec Louis-Olivier Brassard (loup brun) si possible

William + Lena : monter en compétences en CSS? 
Externaliser un style guide, stratégie atomique qui définit chaque élément
- faire quelques séances de travail avec Every layout
- comprendre les stratégies de cascade (composants dépendants des uns des autres)


### Organisation du travail avec les stagiaires

Emmanuel en France jusqu'au 15 juillet
- garder la réunion hebdomadaire les mardis (à reconfirmer)
- possibilité de faire des rencontres spécifiques pour les stagiaires


Righettino
- William va travailler avec Chaitanya, réunion spécifiques de suivi avant ou après la réunion de labo par exemple avec Emmanuel et Lena
    - exploration of IIIF protocol and tools
    - svelte, compatibility with exisiting tools
    - use and explore existing tools
    - 2 iterations for Righettino. 1 → démo project (associate demo image with text) 2 → elaborate on the first demo. 
    - Unknown parameters: how many things will have to be hand coded for the manifest for example
- 30th of June: Keenan arrives, works with Chaitanya, to work on the editorial content. Trained in TEI, will prepare the sources and museological definition of the application
- Daniel made the detailing, decide with Keenan what to do with leftover of 40 hours

Use Righettino to get knowledge about IIIF and to prepare reframe next year (il y a aura un autre stagiaire l'an prochain)

Mauricio works on 3D models of a thermal bath building from the 19th century. 

Formation IIIF


### Daniel 
bibliography of digital art history projects
- enrich 
- classify using an ontology
William: publish the ressource with svelte 
- try to use the xml directly, cetace web component JS that can read TEI
- like with AJAX, get the file and render it with svelte



