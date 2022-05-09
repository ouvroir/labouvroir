---
title: Rencontre avec Calcul Québec
description: Compte-rendu de la rencontre avec l'équipe Calcul Québec
author: ouvroir
date: 2022-01-06
draft: true
tags: 
  - serveur
  - FCI
  - cr
---
# Rencontre du 6 janvier 2022
Présence: Emmanuel Château, Jean-François St-Pierre, Pier-Luc St-Onge, Lydia Vermeyden, Suzanne Talon, Lena Krause

Voir ce que l’on a besoin et voir ce qui existe chez nous et choses que pourraient

## Présentations 
Présentation d'Emmanuel, Lena et du laboratoire
4 produits logiciels à fournir par le laboratoire: 
- publication d'une encyclopédie numérique
- outil de partage documentaire
- outil de documentation des accrochage de collections muséales
- bibliothèque JS pour la production d'expositions numériques

Laboratoire accompagne le projet de partenariat mais qui doit aussi devenir une infrastructure de recherche dédiée pour l'histoire de l'art et la muséologie numérique à l'UdeM. Besoin du plus d'infrastructure possible, dont un budget pour acheter un serveur à 30'000$. Objectif de servir pas juste les besoins actuels mais aussi les projets à venir.  Il y a beaucoup de chercheur·se·s qui ont des projets webs. 

Besoins doubles (environnement de production et environnement de test) :
- applications métiers (produits qui ne sont pas typiques et qui requierent sinon un serveur dédié)
- hébergement de multitudes de site webs et bases de données
- conteneurs et bacs à sable

Quelles solutions pour administrer la machine? 

Si on prends un serveur dédié, openStack ou investir sur Terraform avec des outils d'automation, sous réserve de trouver des personnes compétentes pour le faire. 

Quel dimensionnement de la machine, quelles fonctionnalités (snapshots, backup, sécurité)? 

Identifier des solutions pour les espaces de sauvegarde (préférable de sauvegarder ailleurs)

3 enjeux: 
- pas sûr de la nécessité d'avoir un serveur d'aussi grande taille: ouverture à en faire profiter à la communauté et construire un noyeau de services pour les humanités numériques? 
- inceritudes par rapport à l'offre: disponiblité web, borne passante
- infogérance interne ou externe? 


Trois scenarios possibles :

- Solution hébergée sur la grille de Calcul Québec auto-administrée avec infogérance
- Solution hébergée mutualisée sur la grille de Calcul Québec avec un partenariat pour une partie de la maintenance
- Souscripton à un service cloud privé

Problèmes: 
- financement de l'entretien des infrastructure: est-ce que c'est rendu possible aujourd'hui? 
- quelle expertise pour les solutions sur les humanités numériques

Pour ce qui est de l’entretien, dépend du modèle d’intégration. Devis négocié de 30 000$ pour de l’infonuagique. Mais donnait une allocation pour du Cloud (beluga). Dans ce modèle là l’opération est en partie financé par du transfert mais essayerait d’obtenir le FEI (15% du budget hardware).

Si on allait sur un modèle plus standalone (serveur dédié), difficulté à trouver des gens pour s’en occuper 15%.

deuxième problématique, ne serait pas admissible dans aucune aide de financement, requiert de trouver les fonds complets.

Argent qui serait mieux investi dans des salaires pour développer des services que dans de l’infrastructure. Obtenir de l’infrastructure par défaut.

Quelle est l’offre de service dont aura besoin.
"Avec un RPP, il y a moyen d'avoir l'équivalent du serveur sous la forme d'une allocation."

Comment pourrait-on développer un service dans lequel pourrait développer ce genre d’enjeu là et que reste standard et répond aux besoins tout en restant soutenable en fonction de la croissance. Solution 

Humanum: machines virtuelles qui servent des clusters de machines. Pas une virtualisation classique car sur plusieurs noeuds de machines. Préconfiguration en fonction des besoins avec des recettes préparées. Permet d'installer des choses qu'on ne peut pas installer au privé mais sans avoir besoin de faire de sys-admin. Problème chez Humanum: ne savent pas ce qu'il y a sur les machines,  complexe dans la sécurité. 

Chercher un modèle plus adapté, à créer ensemble. 

Quelque chose auquel réfléchit depuis longtemps sans avoir un vrai plan pour y arriver. Principalement difficile car rarement plusieurs chercheurs en même temps pour y parvenir. Par exemple avoir quelqu’un spécialisé dans Apache. Expérience Huma-Num comme une expérience brute.

Selon les compétences dans l'équipe

On a fait une demande d'accès rapide: expérience riche d'enseignement. Honnêtement, un·e chercheur·se en SHS est incapable de répondre aux questions posées. 
Exemple: besoin de BaseX, connaît les problèmes (java, coûteux en consommation). 

Allocations RPP identiques aux allocations rapides (requiert toujours et encore d'avoir sa propre expertise en configuration)

Réfléchir le *wording* pour la borne passante: il y a des besoins très différents (site webs versus envoi de données au CERN)

Envisager d'avoir une interface (parler à un humain) pour lancer une VM, mais résout uniquement l'accès, car après ce sera encore une VM "tout nu". Si on avait des recettes Terraform toutes prêtes pour Calcul Canada, on compose des services: les préparer (Ansible et terraform) comme environnements de bases pour les humanités numériques qui seront ensuite adaptable pour chaque projet. Est-ce qu'ils ont les compétences en interne? 

Low input: solutions qui sont capables de servir le plus grand nombre de gens possible avec une main d'œuvre limitée (1 seule personne à l'interne). 

Comment on fait? on a 30 000$ à dépenser, on a besoin d'un serveur, on a besoin d'avoir des espaces d'expérimentation disponible pour les chercheur·se·s.

Seule composante qui ne rentre pas dans l’allocation rapide, c’est le stockage. 10To mais à justifier. Réseau qui est à nous à définir (zone privée, zone publique).

Construire pour avoir une meilleure migration pour la suite. Designer dès le départ pour une migration éventuelle puisque nous et eux sont incertains pour l'évolution des besoins. Pour externaliser cela, il faut une dépense pour externaliser les frais d'entretiens. Se débrouiller pour récupérer les fonds sur le CRSH? FEI est seulement débloqué par la dépense initiale du FCI. 

Prises de copies hors site? Plateforme dans la même bâtisse est pleine, prévoient au moyen terme une seconde plateforme ailleurs. 

Ce qui aurait le plus de valeur seraient des services de développement qui sont fait de telle sorte que tout soit récupérable. On ne déploie rien directement, on écrit des scripts qui déploient sur le cloud, donc tout est récupérable. Combien de temps pourrait être consacré à ça? Poste affiché, donc dès qu'ils trouvent quelqu'un ça aiderait, essayer d'avoir une attitude proaAfin de préciser ...'infrastructure. A déjà été fait plusieurs fois: "après évaluation des besoins, l'argent réellement requis sont des salaires pour développement." 

Temporalité: 7 ans (Partenariat). On a parlé de 5 ans (FCI), c'est la durée de vie utile des machines. Besoin d'une garantie d'un minimum de services sur une durée de vie plus longue. Seul enjeu réel: que Calcul Québec cesse d'exister. Objectivement c'est un risque mais il est plutôt faible, pourrait être planifié. 

Plus important d'investir dans le déploiement de script avec des outils pour performants dans Terraform (Félix-Antoine pour l'expertise, Pier-Luc a suivi le modèle, peut-être les connaissances personnelles des administrateurs cloud). Est-ce que ça pourrait être intéressant d'offrir un stage (conseillé par Félix-Antoine) pour développer une solution initiale avec Terraform? 

Comment avancer pour le moment? 
- on prend une allocation de ressource dans la distribution automatique: 
- avoir une VM: développer quelque chose dessus mais tout scripter, comme ça quand ça déborde on va sur quelque chose de plus grand. On choisit/investit dans quoi? 
Terraform : niveau trop haut, déployer des machines.
Se concentrer sur Ansible ou Puppet et décider un plan de besoin (combien de recettes)
- configurer un serveur Apache ou ngix
- gérer les virtual hosts
- sécuriser la machine
- avoir Java, python, julia, nodejs
- base de donnée XML native (conteneur de servlet getty: connecter le port à un service externe)
- processeur XML java
- base de données SQL
- servir le site web du projet CIECO (base de donnée): test pour voir la disponibilité de service de Calcul Québec. Requiert la possibilité d'installer les services.

OpenStack inclut un firewall qui peut être configuré (tout ouvert ou tout fermé). Si on a de l'expérience avec un firewall software préinstallé dans une machine virtuelle c'est possible aussi.

Projet de Jeff Albert et Ryan (?) à UVIC: VM standard ou scripts de déploiements standards.

Le labo va progressivement se retrouver à héberger les projets de plusieurs collègues, exemple Suzanne Paquet. 

Terraform serait trop haut niveau. OpenStack interface. Expérience de Marcello: achat de serveur et tout était redéfinit par l'interface du logiciel installé dessus. Est-ce que OpenStack réinterprète les choses? OpenStack gère création, ouverture, fermeture, snapshot, réseautique. On crée nos propres machines avec OpenStack.

p8-30: possibilité de créer deux P4-15.

4 machines virtuelles ou plus: demander minimum 4 instances
- Serveur Apache propre machine
- Base de données XML
- Julia
- ...

Openstack n'interagit pas avec les services installés. Dans OpenStack, il faut préciser quelle machine est dans quel réseau (1, 2, ... ). Scripter la machine virtuelle apache avec ansible pour réutiliser ou utiliser comme base de départ. Planifier installation et configuration du serveur, peut servir pour le développement et pour la production. Recettes qui seront compatbiles avec tous les environnements OpenStack.

Recettes toutes prêtes Terraform (apache PHP, Docker): pas certain que ça va jusqu'au bon niveau (fichiers de configuration). Terraform définit un environnement, une infrastructure. Ce n'est pas nécessaire dans le court terme, mais ce serait avoir une longueur d'avance en cas de transfert des machines. 

1 seul cloud chez CalculQuébec. 

Rencontre avec Huma-num le 20 janvier. 
Magic Castle

Si on a besoin de faire du traitement numérique lourd en analyse d'images? Analyse automatique de reconnaissance d'écriture: allocation de base devrait suffire, il faut juste que les logiciels soient installés. 
En ce moment, le processus d'allocation de ressources n'est pas fait pour des projets. Emmanuel a pris les allocations à son nom mais pour le Partenariat, ce qui pourrait bloquer pour d'autres projets qui ne sont pas dans le partenariat. Le système est fait pour une allocation par chercheur·se principal·e. Analyse d'image serait peut-être mieux fait sur les serveurs de calcul et non sur le Cloud. Mais est-ce que les logiciels sont installés? Suite d'outils avec Kraken (OCR). Est-ce ça s'installe sur les grappes? Ce qui inquiète Pier-Luc c'est l'envoi des tâches à partir des machines virtuelles. Envoi avec clés SSH mais quel compte sera utilisé? Limiter la clé SSH dans ses actions: faire une seule chose, transférer les images. 

Serveur d'images IIIF (protocole pour l'échange d'images). Sert aussi pour importer des images dans eScriptorium. Cantaloupe pourrait juste aller dans l'infonuagique. L'accès internet est bloqué pour les grappes (possibilité de charger un module pour github). 

Faire des instances temporaires pour le calcul, ne requiert pas de demande: utiliser son compte normal, transférer ses données et les traiter. Par contre, s'il faut faire installer des logiciels, il vaut mieux s'y prendre d'avance pour tester le bon fonctionnement comme ça tout sera prêt.

Sur les grappes HPC, on suppose que les données sont déjà sur le système de fichiers réseaux. Machine de calcul temporaire (lancée juste pour faire le calcul, il faut voir quel sont les besoins de calcul). Quels sont les délais d'attente raisonnable? Pas de réel délais, possibilité de le faire par batch et en différé. 

Installation de Cantaloupe: voir comment la grille de service est efficace sur le web. Test des services et de la borne passante. Offrir un service sur une machine dédiée. 

## Conclusion de la rencontre

Labo: pour le moment, on travaille sur le cloud et on se débrouille. Obtenir les VMs, écrire à Jean-François si jamais.

Calcul Qc + Labo: on requalifie la dépense FCI pour déployer des recettes (paragraphe descriptif, soit calcul Québec soit par un consultant externe). Est-ce qu'on doit attendre le recrutement de l'analyste?

Suzanne: contacter l'équipe de uVic pour demander des nouvelles de leur projet. Idée d'avoir des VMs plus étoffée. Suggestions sur les technologies les plus intéressantes? 

Clarifier au plus tard en septembre les conditions d’accès (Allocation projet, etc.)


## Conclusion

Faire un relevé de décision et leur envoyer. En profiter pour relancer si l'accès aux allocations n'est pas réglé.

Définir une prestation de départ pour la mise en place de la première allocation (si possible reproductible)

Essayer l’infrastructure
Prendre le temps négocier un accord formel sur l’emploi des dépenses.



Esquisse de la mission (prestataire externe, facture et honoraires, surplus finances Partenariat): 
Configuration d’un serveur virtuel sur OpenStack et scriptage de machines virtuelles

VM1
- Serveur Nginx
- Utilitaires système (ssh, git, vim, etc.)

VM2 Base de données XML native
- Environnement Java
- BaseX
- Utilitaires système

VM3 
Python, NodeJS, ...

VM4, Serveur d’image
- Cantaloupe
- Utilis

VM5 Bacs à sable
- Docker avec ou sans Kubernetes
- Utilitaires systèmes

ou alors un serveur et des dockers.