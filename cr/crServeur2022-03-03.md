---
title: Rencontre de suivi avec Calcul Québec du 3 mars 2022
author: ouvroir
date: 2022-03-03
description: Compte-rendu de la rencontre
draft: true
tags:
    - serveur
    - cr

---

# Rencontre de suivi avec Calcul Québec

Rencontre avec Félix-Antoine Fortin

Présentation des besoins et de la situation par Emmanuel
- disposer rapidement de ressources
- éviter le travail supplémentaire (pas de staff / capacité)

Allocation d'un instance
- ce qui est difficile à changer: dimensionnement du disque (stockage) racine de l'instance = 10To de volume de départ
- migration 
- si on n'utilise pas la RAM et les cœurs → risque de se faire taper sur les doigts (plus de contingence et demande de redimensionner)
- possibilité allouer plus de cœuers et de mémoire vive sans même arrêter la machine
- sur béluga: accès par projet. Bien s'assurer que le contenu du projet du FCI a un disque distinct
- pas de service de low balancing → 1 instance = 1 adresse IP

Investir l'argent du FCI dans du service de personnel 
- montant donne accès à un quota précis? ne veut pas dire que les ressources sont disponibles
- si on veut commencer à créer des instances, il faut s'assurer que le service d'accès rapide va nous créer un instance dans le bon cloud (béluga et non arbutus) 

## Fonctionnement
Séparer les instances par besoin
- baseX
- Cantaloupe


Lancer une instance
- allocation des instances (p1-1gb, p1-2gb etc) peut être modifié
- on peut choisir, à la création, de ne pas supprimer le volume après la terminaison de l'instance 

Stockage racine d’une instance qui est difficile à redimensionner. Mais assez d’espace disponible en accès rapide pour créer des volumes de départ importants.
Personne ne vous tappera sur les doigts si n’utilise pas le stockage. Plus de contingence sur la RAM et les cœurs.
Possible allouer plus de cœurs.


Demander créer l’instance avec un disque à part qui ne sera pas supprimer lorsque je vais tranférer l’instance.
Béluga.
Adresses IP publiques.
IP flottantes plus rares. Celles à partir desquelles pourra se connecter sur l’internet depuis une adresse. Si veut créer des sites publics, etc.
Si des instances différentes chaque service aura une adresse IP distincte. Pas de service de low balancing. Une instance = une adresse IP.

Pas un problème d’avoir un service.
Si veut séparer les choses en logique principal pb l’adresse IP publique.

Bien choisir : Supprimer le volume après la destruction de l’instance.
Si seulement un nom image pas de volume créé.
Si pas de nom d’image alors OK.

Après lors recréation dans la source au lieu d’utiliser une image, utilisera le volume.

### Backups

Pas de solution NAS pour le moment.
Ne sait pas où Calcul Québec va. Offre du backup sur Tape pour le HPC. Backup urgence car laborieux pour aller chercher les données.

En cas installation, etc. Dans l’interface de Open Stack, faire des snapshots. Un quota qu’il faudra discuter sur le nombre et la taille totale.

Si met de côté les erreurs humaines liées à l’opération de la VM. Les données ou l’installation sont stables et répliquées trois fois.


### Vidéo et son
Solution reste à trouver

Durée de la garantie matérielle: 3 ou 5 ans
Si on a besoin de plus long, il faut voir avec un dépôt institutionnel ou autre (même problème partout)

### Automatisation
Choix du système d'automatisation (puppet, ansible)? 

Le plus communément utilisé dans le cloud de calculCanada et calculQuébec c'est Ansible. Donc ils ont l'expertise pour réviser et conseiller, accès à une communauté. 

Si la configuration s'applique à une machine virtuelle à la fois, Ansible devrait amplement répondre à nos besoins et on peut retrouver des recettes pour le faire.
Eventuelle combinaison d'Ansible et DockerFile. À un moment donné, on devrait avoir accès à des cluster Kubernetes à la demande.

Conteneurs pour la reproductibilité des calculs scientifiques, Singularity (HPC)
Applicable à d'autres scénario? 
Né dans un contexte d'utilisation de partage par plusieurs usagers
Exécuter des DockerFile dans Singularity.

Conteneurs: mécanisme de définition est séparé de l'engin pour l'exécuter.
Pas toujours biens vus car opaques et plus lourd pour venir aider un chercheur.

Enjeux lorsqu’il sera question d’ouvrir certains ports ou accès à certains services à l’externe. Groupe de sécurité dans OpenStack qui par défaut sont tous barrés.
Pour éviter de se faire tapper sur les doigts éviter certains ports à tout l’internet mais limiter à certaines institutions.
Comme pas de contrôle sur ce qui est installé, audit pour identifier vulnérabilité sur remote desktop.

### Sécurité

Les pays qui ont de grosses fermes de hackers connaissent l’existance de la plage d’adresses IP disponibles à Calcul Canada. Ne pas s’étonner de voir des tentatives d’introduction. Pare feu de Open Stack ok pour un accès limité à l'institution (mais pas internet au complet)

Peut installer un second pare-feux éventuellement car celui de OpenStack limité dans ses fonctionnalités. Possible de configurer un pare-feu par défaut pour chaque instance.

Bonne pratique avoir groupes définis par instance.
Travailler avec des reverse proxy 

Principal souci: 
- maintenir ses instances à jour
- choix du système d'exploitation: ce avec qui on est plus à l'aise

### Prestataire
Incertain à quel point les gens vont être familier avec OpenStack (mais c'est offert par OVH et un autre gros joueur)

Mise en place devrait aller. Principal défi sera de maintenir les choses sur le long terme. Planifier l’opérationnalisation de ces choses là sur plusieurs années, que ne perdiez pas de données et avoir des gens intéressant à ces choses là. Si nombre usagers croits, réfléchir scaling.

Si arrive à faire la démonstraction que des choses qui déservent une communauté au niveau québécois (centaine, milliers d'utilisateur·rice·s), ne pas hésiter à revenir vers Calcul pour dire que nous plus capables de l’opérer à cette échelle puisque groupe de recherche, seriez-vous prêts à "reprendre le flambeau" / faire de la place pour offrir ce service directement?

### Durabilité
Négocier l'accès à l'infrastructure au-delà des 5 ans du labo?
Pratique habituelle d'utilisation du matériel beaucoup plus longtemps que les garanties matérielles

Jouer dans le cloud commercial dans les limites qui sont disponibles en tant que groupe de recherche → gros aspect gratuit, représentants commerciaux dédiés à la recherche qui peuvent allouer des crédits rapidement. Représentant Amazon EST Canada.

Recommande d'avoir un pied dans le cloud commercial parce que malgré toutes les bonnes intentions de CalculCanada, ils ne pourront jamais égaler l'offre du cloud commercial.

### Intégration et déploiement continu
github workflows
openstack API (un peu lourd)

Sur nos instances: déployer des API ou des logiciels qui ont des APIs disponibles sur internet


## Questions
qui s'occupe du déploiement du cloud à calculQuébec: un sysadmin dédié + offre d'emploi actuelle à l'UdeM (sous Jean-François)
sinon, ça se passe au niveau national

