---
title: Rencontre avec Koumbit du 12 septembre 2022
author: ouvroir
date: 2022-09-12
description: Compte-rendu de la rencontre
draft: true
tags:
    - serveur
    - cr



---

# Ouvroir & Koumbit

Rencontre aec Hubert

ouvroir@umontreal.ca
emmanuel.chateau

[jitsi](https://meet.jit.si/SkiPuzzlesInteractCautiously)

[notes]
Module puppet pour Matrix: https://forge.puppet.com/modules/cheasles/synapse

suivi: 
- Hubert: consulter l'équipe et devis,~fin mai
- Hubert: test de Collabora si possible
- Lena+Emmanuel: calculQc, accès et allocations organisées. Prévoir une réunion de travail (inclut la question des backups)
- Emmanuel: partager les instructions d'installations BaseX

## Descriptions de la prestation demandée (12 mai 2022)

Installation et configuration de serveur

- serveur http Apache + routage + nodeWeb
- déployement de machines virtuelles

Préférence des bases SQLite plutôt que mySQL. MariaDB (géré avec AlternC)

Dans l’idéal, avoir un seul serveur pour administrer les bases de données, trouver un tronc commun.
Héberger Strapi ailleurs pour ne pas avoir besoin de le gérer ?

Peut-être y aller de manière simple avec Altern-C

Déployement d’outils

- Création d’un module Puppet pour Cantaloupe
- Créer un module Puppet pour Basex? 


### Étapes de réalisation 2022

1. Été 2022, d'ici fin septembre: 
    - Serveur http avec node web (alternC) (aussi serveur BD)
    - Premier environnement de travail (avec puppet), qui permet de déployer des applications java/nodeJS/php + accès SSH sur le serveur + git pour faire de pull sur github
    - [BaseX](https://basex.org) (serveur dédié ou sur le premier environnment), sera installé par Emmanuel au besoin
    - Reverse proxy

s'il y a du temps: automatisation des backups et/ou nextCloud 

2. Automne 2022, d'ici décembre:
    - [Cantaloupe](https://cantaloupe-project.github.io/): serveur dédié
    - Intégration continue (tâche d'automatisation) avec git
    - automatisation des backups (à discuter)

3. Installation d’applications auto-hébergées (ou Yuno host)
    - Matrix
    - HedgeDoc
    - Mobilizon
    - GitLab
    - nextCloud + Collabora (lool)

devis frais récurrents + devis frais ponctuels
service de monitoring: heures de bureau, sinon 24h/7j. Disponible dans OpenStack? 



### Cas d'usage
Si quelqu'un veut héberger un site (ex: Wordpress), ça fonctionnerait sur la machine sur laquelle il y a altern-c. 
- créer un compte: chaque personne a un environnement spécifique (possibilité de créer un courriel)
- héberger un domaine
- crée une arborescence de dossier dans lesquels pousser les contenus
- configuration de zone DNS du domaine et adresse IP

Envronnement BaseX: 
- charger des données
- déployer des projets git
Système d'întégration continue? (automatisation côté serveur: git push. Sinon connexion ssh + git pull: virtual host, répertoires et lien symbolique vers les répertoires) 

Applications Node.js




## Différents services et intérêts (5 mai 2022)

Administrer des serveurs

- bacs à sable pour la recherche
- services pérennes liés au projet, dont autohéberger des applications comme:
  - hébergement web classique
  - cantaloupe (java)
  - basex (java)
  - bases de données
  - [yuno host](https://yunohost.org/) element (matrix), ~~jitsi~~, hedgedoc, mobilizon

Proposition d'utiliser d'[alternC](https://alternc.com/), équivalent libre de CPanel: gestion nom de domaine, courriels (serveur mail), hébergement d'applications

Gestion des adresses IP, attention aux contraintes de calculQuébec:
- nb de machines, oui facilement 5-6 mais pas 10-15
- limites d'adresse IP
- suggestion: chaque type de service = 1 machine virtuelle

besoins immédiats: (à départager ce qui relève du sys-admin et de l'applicatif)

- sites
- base de données
  - couchDB
- gestion nom de domaines
- serveur nodejs
- serveur php (apps php)
- serveur java
  - base de données xml native
  - serveur cantaloupe 
- sécuriser le serveur

## Procédure installation BaseX
 - à venir (Emmanuel)