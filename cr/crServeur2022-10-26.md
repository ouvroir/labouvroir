---
title: Calcul Québec
description: cr de la rencontre avec CalculQuébec
author: ouvroir
date: 2022-10-26
draft: true
tags:
    - cr

---
## Rencontre avec Calcul Québec

Pier-Luc St-Onge
Meghan Landry
Sarah Cameron-Pesant, MA en littérature et sciences de l'information. Bibliométrie avec Vincent Larivière

Réunions dans l’optique de pouvoir aider les gens en recherche en shs. Comme il y a beaucoup de besoin pour une plateforme web pour travailler des analyses avec des chartes graphiques, besoin de faire du travail supplémentaire.

Jupyter hub, mais besoin d’applications standards pour les sciences humaines et sociales.
Autres outils sans doute nécessaire. <!-- référence à Humanum je crois oui mais il centrait trop sur le traiatement de données, donc je voulais recadrer plus large -->

Espérant du temps personne pour implémenter l’infrastructure info-nuagique. Manquait à l’époque de temps personne. Mais depuis recrutement de Sarah.
Maîtrise en littérature, travail sur Erasme. Maîtrise en sciences de l’information dans l’idée de devenir bibliothécaire. Projet de recherche sur les données d’Érudit. Puis travaillé comme annalyse chez Érudit

A pu prendre connaissance des échanges et des tickets.

Besoins du laboratoire
1. solution d'hébergement web at large, faire tourner des services professionnels, avoir une certaine flexibilité et offrir l'hébergement d'applications pour la recherche en cours. 
2. Offrir des bacs à sable
Définition de services

Recherche de prestataires de notre côté. Pouvons-nous travailler avec un administrateur privé pour administrer notre instance CalculQuébec? 
Financement FCI: budget à requalifier en un service cloud avec de la prestation

Si on s'occupe de la création des instances etc, il va falloir sélectionner une instance plus petite (plus petit devis demandé) pour rémunérer le prestataire de service. 
Souhait de travailler avec CalculQuébec pour modéliser des cas courants qui peuvent servir à d'autres chercheur·se·s et d'autres services, un peu plus que du IAS.

Concours d'allocation de ressources, ce qu'on demande n'est pas vraiment plus gros. On voudrait avoir du service et que ça serve au-delà du 

Que peuvent pour nous les collègues qu’ils ont rassemblés
Question accès externe.

RPP Ressources pour les portails et les plateformes.
Personnel spécialisé dans les systèmes info-nuagique. Sarah entrée pour le soutien aux SHS.

Besoins de notre équipe:
- systèmes courants type LAMP
- applications nodejs (Svelte, Astro)
    - si possible en intégration continue
    - serveur de base de données
    - gestion de persistance (secrets, fichiers, bd)
- application java
    - édition critique numérique
    - édition numérique Encyclopédie (base de données XML native)
- web sémantique
    - data store RDF
- recopie, archivage
- mise en place de sandbox
- (serveur d'image IIIF: négociations avec la bibliothèque)
- application plus consommatrice en données
    - calcul
    - traitement de lots d'images

Déploiement avec scripts d'automatisation type Ansible ou Puppet

Enjeux autour du cloud avec la DRA, pas encore de véritable investissement sur de nouveaux logiciels. On ne peut pas attendre de l'alliance de nous apporter ces solutions dans l'immédiat.

Acenet Chris 
Chris Geroux, Dalhousie University, [Acenet](https://www.ace-net.ca/team.html) spécialisé dans le Cloud
Pour le moment rien de prévu. Nous regardons du côté de Omeka-S pour héberger des portails web. 

Argent demandé pour HSS series.
Meghan Landry commencé en juin. Beaucoup de réunion pour logiciels de recherche dans le cloud. Offrent actuellement wordpress avec plugins. Regardent en direction d’autres packages possibles. 
DH in a box, multiple software and applications in one.
Récemment cloud [workshop](https://www.ace-net.ca/acenet-cloud-from-a-to-z-tickets-413049541297.html) au cours des deux dernières semaines. Travail avec Jekyll. Mais pour le moment pas grand chose au-delà de Wordpress.

Jean-François Landry fait partie de l’équipe cloud au niveau de Calcul Québec.
Un service GitLab pour l’alliance

Service Sys-admin? Non, toujours pas du côté de calculQuébec
Travailler avec Sarah pour définir et génériciser les cas d'usage
Peut nous aider dans le développement de l’offre de service, développer les besoins de la communauté SHS, faire des focus group pour répondre aux besoins de la communauté.
Sur place, peut faire le pont avec l'équipe

Si on fait appel au prestaire de service (Tim), est-ce qu'on rajoute une phase de discussion avec eux? 
Indépendant qui travaille en contexte de recherche, connaît la grille parce qu'il travaille sur la côte ouest, intérêt pour la construction du service

Du côté de l'alliance :
Donner un soutien au développement de la solution.
Dire à un prestataire d’installer quelque chose .

Réunion pour discuter avec eux, Suzanne et Tim aussi. 

Dans l'immédiat, les services sont offerts en accès à la pile RAS. Si on a besoin de plus grand, ça prendrait une demande d'allocation pour avril 2022. Concours est maintenant mais les allocations sont en avril.

Accès à ces services. Mais si on achète le serveur, quelle est la différence?
Demander des ressoures et stockage sur deux instances (Ex: beluga et arbutus)

Modèle CalculQuébec n'est pas adapté à notre cas d'usage. Nous amène a répéter où est le service? 
Réunion avec Suzanne vendredi, veut lui écrire avant pour insister sur ce besoin. À quoi sert l'argent et on fait quoi avec?

Grappe fonctionnelle. Ne prévoit pas de coupure à court terme pour remplacer le cable. Maintenance réseau pour fin novembre (béluga, narval, 1-2 jours).

Créer une instance persistante, recommandation de Félix-Antoine Fortin (qu'on a rencontré en mars). Comme c'est sur un disque physique on peut redimensionner sans tout casser
Il y a moyen d'avoir des volumes de stockage.
Cadre actuel du RAC: pas tant de limite, concours d'allocation
[RAS](https://docs.alliancecan.ca/wiki/Cloud_RAS_Allocations) a une limite: accès rapide

RAS rapid access 
- 20 instances
- Avoir un disque persistant

Possible de travailler avec un Sys-admin externe. Nous qui le payons. En terme de sécurité nous nous détachons du niveau de sécurité dans vos machines externes. Pour nous, le fait que vous fassiez appel à un prestataire nous rassure plutôt qu’autre chose. C'est possible que l'Alliance demande un jour que CalculQuébec vérifie l'état de sécurité de chaque machine.

Possibilité de créer un compte à quelqu’un. Créer un nouveau rôle dans CCDB commandité par CCRI. Non-research staff.

Discussion avec Suzanne pour contractualiser et déterminer le service auquel on accède, requit pour documenter auprès du FCI. 
- périmètre des services: ni RAS, ni RAC → construire sans contraintes
- sinon: RAS mais garantie de persistance pour pouvoir redéployer l'instance

Bacs à sable: besoin de tous les chercheur·se·s, pourrait être pris en charge par CalculQc. Service à développer pour la communauté
- déployer rapidement une petite application ex: cantaloupe
- installer, puis détruire après le test
nécessite de préciser le cas d'usage mais Sarah a des idées aussi
Difficulté de tester des choses en dehors des environnements standards, ex: déployer rapidement une base de données type CouchDB avec NodeJs
Services commerciaux: pas d'installations car ils traitent beaucoup de cas générique. 
Services d'intégration continue orientés web: rendr, vercel

MagicCastle automatise la construction et la desctruction. Il y a certains moyens de ajouter des nœuds.

Rencontrer Sarah prochainement à Montréal
Va essayer d'ici-là de jeter un œil aux offres de services commerciaux

## Suivi

Redhat, fabriquent OpenStack et Ansible
ont aussi un service cloud