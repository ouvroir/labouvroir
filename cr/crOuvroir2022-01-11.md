---
title: Réunion de laboratoire 
description: Compte-rendu de la réunion hebdomadaire du 11 janvier 2022
author: ouvroir
date: 2022-01-06
draft: false
tags: 
  - cr
  - lab
---
# Rencontre du 11 janvier 2022

Kristine, Emmanuel, Lena, William 

## Demo du travail en cours

### Site du labo (Astro)
Terminer la réorganisation i18n.

Contenus
- Rédaction des contenus: se mettre d'accord sur les textes (Commentaires sur hiet les tranduire vers l'anglais
- présentation des équipements: https://drc.ucla.edu/resources/software/ (ajout de l'imprimante 3D dans le labo)
- design / identité graphique ?

### CBC (Svelte)
Données du CBC servi en JSON avec BaseX
[Demo](https://cbc-client.vercel.app/)
- vue par séance
- vue par délibération: liste de fiches (sélection pour regrouper les délibérations en affaires) et formulaire de modification des contenus de la fiche

Fonctionnement rapide même pour charger des pages de 500 délibs par page.
Rapidité de développement

Interface avec [Carbon](https://www.carbondesignsystem.com/), la documentation laisse encore à désirer (entre le site d'IBM, les sites dédiés pour React, Angular et la doc de Carbon pour Svelte). Quelques problèmes à régler, potentiellement documenter les problèmes et/ou contribuer au github. 

Possibilité de créer nos propres composants, au sein du labo. Explorer des outils de prototypage et voir si on crée le nôtre ou non dans la prochaine année. Si on développe quelque chose, ajouter ce qui serait intéressant pour l'histoire de l'art. 
Autre option, styler Carbon en ajoutant une couche par dessus. 

Svelte: génial pour Emmanuel, simple et flexible. Donne envie de faire l'ensemble des projets du partenariat avec. Option de faire le site du partenariat avec, permettrait de générer des sites pour les conférences automatiquement. Peut-on trouver des développeur·se·s compétent·e·s?

### Data Artem
Nouvelle version! 
Model data and inscribed capitals index are still the same site. 
User Inteface stays the same. New views: building, capitals, map, image gallery, floor plans.
Combination of leaflet and Ajax (?).

## Infrastructure

### Nouvelles du labo 
Local du CRIHN au 8e de Lionel-Groulx.
Déménagement à venir, en attente de travaux. Agrandissement et ajout des bureaux de Josée et Lena.


### Serveur
Négociation d'un service Cloud avec Calcul Québec. Budget affecté à l'achat d'un serveur statique (gros rack). 15% par année pour entretien et maintenance + c'est une machine en blanc (ce serait à nous d'administrer: trouver un sys-admin).
- Durée: 5 vs 7 ans
- Concours pour accéder gratuitement au ressources (annuel)
- Accès rapide aux ressources qui est assez généreux: on n'a pas nécessairement besoin de payer pour avoir accès aux ressources. Calcul Québec manque de ressources (personnel) pour accompagner les chercheur·se·s dans la prise en main de la structure. 

Demande d'allocation rapide: la machine est un peu petite donc il faudra la remplacer par une machine plus grosse. Créer des scripts, mais si on stocke des choses, il va falloir les exporter. 

Besoin de clarification: 
- avoir une durée contractuelle: garantie d'accès à l'infrastructure pour 7 ans
- explications claires sur la recopie (serveur de backup): détails sur la prestation
- renvoyer les spécifications 
- Système de sauvegarde (imagerie lourde)
- clarifier l'utilisation des 30'000$
- issue de la réunion: délai d'ici à septembre pour clarifier. Besoin d'un serveur avant.
- Processus d'intégration continue (requiert l'installation de l'outil? )

Budget prévu pour l'installation (FCI), puis l'entretien et la maintenance (FEI). 

Questions: 
- fonds FCI: le devis actuel est pour du matériel chez Calcul Québec. Si on n'arrive pas à une entente avec eux, on peut aller au privé et changer pour aller au privé. Calcul Québec propose de faire un justificatif de modification de dépense: besoins de sont pas des ressources matérielles mais des ressources en personnel pour faire certaines choses. Requiert d'arriver à une entente claire sur ce que va faire le personnel.
- putting aside the evil in Amazon, why not use their services? They work. Si la recherche n'est pas capable d'avoir une infrastructure comparable au public, on va être dans le même problème qu'avec l'édition savante --> enjeu politique. Pragmatisme: avoir un certain nombre de services hébergés dans un cloud commercial. Essayer d'investir dans une infrastructure plus durable pour le long terme, au risque que ça coûte plus cher et de faire le double du travail. Recherche en cours: Puppet, Ansible... Choisir une technologie de déploiement qui est compatible avec plusieurs infrastructures (Calcul québec et Google, Amanzon etc.). Crainte avec Calcul Québec: ils n'ont pas l'habitude de faire du service web, ne peuvent pas garantir une disponibilité chiffrée de la ressource. Pas de garantie de bande passante. 

Who uses what, in DH? 
- Erudit is on Calcul Québec (but maybe not for the public side) To ask
- France: Techniciens qui configurent les serveurs et s'occupent les serveurs. Chercheur·se·s s'occupent de l'administration des logiciels. C'est ce qu'on veut créer mais n'existe pas encore. Ex: Virtual machines d'Humanum mais problèmes de redimensionnement et de gestion des contenus. Modèle en train d'être revu. Hackathon en mai pour essayer de concevoir une autre façon d'allouer des ressources aux chercheur·se·s en sciences humaines, ex: faire des recette Ansible.
- Aux É-U, ce sont les TI qui s'en chargent ou ils vont au privé. Amazon, Google: on dit ce qu'on veut et ça marche, c'est facile.
- Amazon: clusters de machine. Services pré-installés avec interface de configuration. 

Option d'utiliser un service commercial jusqu'à que Calcul Québec, en configurant le service commercial avec Ansible pour prévoir la migration. 

## Activités  (présentiel - virtuel)

### Réunions hebdomadaires
Les mardis à 10h30

### Brown bag lunches
Zoom, mais pas trop long: 30-45 min? 
Ne pas recouper avec les Midis du CRIHN (invités plus distants)

Choisir des gens plus proches pour pouvoir les inviter en personnes plus tard: commencer par nous ou par du monde de l'extérieur? 
- Antoine Courtin: nouveau centre de documentation du Musée d'Orsay
- gens de JStore pour le digital storytelling

Liste de gens qui travaillent en DAH au Québec? Emmanuel a quatre listes (labos, projets, chercheur·se·s, ...).

### Atelier WAX
Atelier de gestion d'exposition en ligne

Techno:
- WAX (site statique)
- Jstor (digital storytelling with Jekyll)
- Svelte (code produit à la fin n'est pas super clean non plus. Très bien pour les applications interactives, utiliser Svelte pour les aspects interactifs uniquement?  )

## Rencontres
- Malaga (vendredi 14 janvier)
- Rencontre de Kristine avec Marie-Ève (comité de bibliothèque): ressources numériques pour les projets. 

- DIRO (attendre à fin janvier, après le rush de la rentrée)

## Varia

- [Research Data Management: What is the Worst That Could Happen?](https://github.com/ouvroir/labouvroir/issues/65)

- Commande de matériel: scanTents. Délais administratifs et attente des locaux (où faire livrer pendant que l'Université est vide)?