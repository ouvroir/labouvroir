---
title: Rencontre avec Koumbit du 2 septembre 2022
author: ouvroir
date: 2022-09-02
description: Compte-rendu de la rencontre
draft: true
tags:
    - serveur
    - cr


---

# Rencontre avec Koumbit

Rencontre avec Timothée Guic

## intro
présentation du laboratoire
- infrastructure numérique

condition de financement: travailler avec CalculQuébec et la DigitalResearchAlliance
- offre: infrastructure as a service
- création des machines à la demande
- requiert de les administrer
- OpenStack (redimensionnable en fonction des besoins)
- capacité à dédier un disque sur une machine pour le stockage (Requiert un plan de départ)
- ressource cloud: on installe ce qu'on veut
- limitation en bande passante entrante
- on peut créer "autant d'instances qu'on veut"
- limitation sur le nombre d'adresses IP 

enseigne à Vancouver
assez occupé jusqu'à la fin de l'année 2022
2023 prévoit d'être plus disponible

## besoins
- bacs à sable pour la recherche
- services pérennes liés au projet, dont autohéberger des applications
    - hébergement web classique
    - nodejs + svelte
    - intégration continue avec Github
    - basex (java)
    - bases de données
    - web sémantique (java)
    - yuno host element (matrix), jitsi, hedgedoc, mobilizon, gitlab
    - cantaloupe (java) (?)
    - il faudra héberge common
- prod non critique

modèles d'intégration continue
considérer Gitlab? faciliterait certaines procédures avec des pipelines préexistants (pas faisable d'ici fin décembre)

réduire les dépendences et limiter les couches technologiques
gestion la plus automatisée possible

À voir pour Ansible, Puppet, ...

ligne de temps | priorités: 
- d'ici décembre, applications de projets
- baseX
- bacs à sable (bien réfléchir comment)
- hedgedoc etc.
- sécurité/sauvegarde des données persistantes: service de backup sur une autre machine

suite:
- prod (applications légères hébergées avec github pages)
- LAMP pas d'urgence

## suite

indications du temps (fourchette en temps et argent)

contrat: service sur la base d'honoraire (Requiert un devis)
- attention: réattribuer l'item du serveur calculQc
- FEI entretien de l'infrastructure

nous revient avec une proposition d'ici le début de la semaine prochaine


## Questions

*Est-ce qu'on peut employer Tim pour faire la base de données pour Common s'il sait se servir de baseX?* peut-être, en 2023