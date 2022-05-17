---
title: Rencontre avec Koumbit
author: ouvroir
date: 2022-05-05
description: Compte-rendu de la rencontre avec Koumbit
draft: true
tags:
    - serveur
    - cr


---

# Rencontre Koumbit

Hubert 

Présentation du labo

## Koumbit
équipes:
- dev
- compta
- infrastructure/sys admin

Travaille principalement avec leur parc de serveur dans un centre de données à Montréal. Quelques clients à l'externe

Coop de travail enregistrée en OBNL, sans patron, hiérarchie horizontale. 18 ans, né dans les mvt sociaux, spécialisation groupes syndicaux et militants.

Un modèle unique, gèrent l’entièreté des services et ensemble des logiciels libre.

Utilisation d’un gestionnaire de configuration: Puppet


## Ouvroir

CalculQc → computeCanada remplacé par la digital research alliance, infrastructure de recherche, née bottom-up d'universités puis consortium
Gouvernement voudrait avoir une meilleure maîtrise sur l'ensemble de l'affaire, nouvelle organisation qui est sensées les régimenter, moment de transition

Services cloud, peu d'expérience, font plutôt de l'infrastructure as a service, pas d'administration de service logiciel ou de couches plus développées. Il y aura du cloud communautaire mais qui restera cantonné dans des machines virtuelles coordonnées avec OpenStack.

Financement nous contraint de faire affaire, en premier lieu, avec Calcul Qc. Avantages → infrastructure qui pourrait nous faire bénéficier de services pour l'archivage et la création de backups, infrastructure coast-to-coast. Autre services: calcul de pointe. Allocations de base pour la recherche

Notre financement: 
- achat d'une machine qui nous soit propre
ou
- entrer dans leur cloud, pour le partage des ressources entre chercheurs
- enjeu des sciences humaines et leur appropriation de l'infrastructure numérique de recherche → pas de financement pour des techniciens/sysadmin. Faire évoluer les modèles et explorer des modèles cohérents pour que les chercheur·se·s s'approprient cette infrastructure. 

Prestataire de service aligné sur les valeurs du labo. 
Investir dans le cloud communautaire pour l'avenir de la recherche scientifique malgré la pression à aller vers le cloud commercial qui sert les besoins standards avec beaucoup de facilité 

Orchestration, techn. libres: possibilité d'arriver à un écosystème très consistant. 

Koumbit: 
- quelques centres de recherche déjà chez Koumbit
- site web omeka uOttawa → Solidarité avec les peuples autochtones, implication auprès de la chaire de recherche du Canada en traditions intellectuelles et autodétermination des Premiers Peuples  ...

Département histoire uqam
Confluences des premiers peubles, Chaire de recherche du Canada en traditions intellectuelles et autodétermination des premiers peubles Ottawa

archivage des projets universitaires

### Différents services et intérêts
Administrer des serveurs
- bacs à sable pour la recherche
- services pérennes liés au projet, dont autohéberger des applications
    - hébergement web classique
    - cantaloupe (java)
    - basex (java)
    - bases de données
    - [yuno host](https://yunohost.org/) element (matrix), ~~jitsi~~, hedgedoc, mobilizon

essayer de limiter le nombre d'applications
essayer d'avoir une certaine autonomie sur l'installation et l'utilisation

utilisation d'[alternC](https://alternc.com/), équivalent libre de CPanel, gestion nom de domaine, courriels (serveur mail), hébergement d'applications

cloisonner l'environnement, machines virtuelles séparées

## Koumbit x Ouvroir

Gestion adresses IP

limite l'admin système à l'extérieur, se limiter dans les nouvelles technologies aussi 

habitués à installer des nextcloud, tout est prêt pour ça

communication: mattermost

crucial pour la prestation: applicatifs métier, environnement java pour bd, connexion au serveur web avec proxy http

besoins immédiats: 
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

Communications entre les services.
Principalement de l'installation, interface réseaux, firewall, et que le labo fait plus de l'installation, 
gestionnaire de zone

structure de financement: budget de fonctionnement (annuel), argent sur une base récurrente pour l'entretien et l'ajout de fonctionnalités.

limites calculQc
- nb de machines, oui facilement 5-6 mais pas 10-15
- limites d'adresse IP
- suggestion: chaque type de service = 1 machine virtuelle

devis à préciser
taux horaire à 120$/h

## suite
[pad](https://demo.hedgedoc.org/NSJb8ZEhQ9yibmPHSaJhAQ#)