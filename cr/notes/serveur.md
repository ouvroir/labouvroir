# Serveur

## Présentation

Le laboratoire de muséologie numérique est une infrastructure destinée à soutenir le travail conduit dans le cadre du Partenariat *Des nouveaux usages des collections dans les musées d’art*. Ce laboratoire fournit à l’ensemble de l’équipe un équipement de pointe pour mener la recherche mais aussi pour expérimenter et développer de nouveaux usages des collections numérisées qui utilisent le web, les techniques de visualisation 3D et la réalité virtuelle et augmentée. Il donne l’occasion de créer une infrastructure éditoriale solide pour l’Encyclopédie numérique et de produire trois développements informatiques qui seront mobilisés dans les différents axes de la recherche : d’abord avec la mise en place d’une plateforme collaborative de travail pour le travail sur les archives ; ensuite avec la création d’un outil numérique consacré à la documentation et la reconstitution 3D des accrochages de collections ; enfin, avec la création d’une librairie JavaScript destinée à faciliter la production et le déploiement de dispositifs d’expositions numériques et de l’illustration de l’Encyclopédie. C’est aussi une structure polyvalente qui permet de faciliter le travail collaboratif et l’organisation de téléréunions avec les partenaires muséaux et internationaux du projet. Sa création permet de doter le Canada d’un équipement de recherche dédié à l’expérimentation et le développement d’innovations dans le domaine de la muséologie numérique.

Avec ses équipements matériels, le laboratoire permet la documentation des nouveaux usages de collection, la création de contenus multimédias interactifs et la production d’interviews filmées pour l’Encyclopédie. Il donne l’occasion d’expérimenter de nouveaux usages numériques des collections et de développer des applications innovantes autour des collections muséales numérisées sous la forme de démonstrateurs qui utilisent le web, les techniques de visualisation 3D, la réalité virtuelle et augmentée. C’est une structure polyvalente qui permet également le travail collaboratif et l’organisation de téléréunions avec les partenaires. Enfin, un serveur fourni par Calcul Québec permet d’héberger toutes les applications et d’offrir des bac-à-sables numériques. Ce laboratoire de muséologie numérique qui sert l’ensemble des chercheur·se·s du projet, ses partenaires et les étudiant·e·s, est placé sous la responsabilité de Johanne Lamoureux (UdM) chercheuse principale du Partenariat et du responsable de la cellule numérique Emmanuel Château-Dutier (UdM) qui est spécialisé en édition structurée ainsi que dans le domaine des métadonnées culturelles et du web sémantique. Kristine Tanton (UdM) coordonne les aspects relatifs à la 3D et la réalité virtuelle et augmentée. Le recrutement d’un responsable technique du développement de l’infrastructure pour trois ans est destiné à assurer la mise en place du laboratoire et la réalisation des outils proposés.

## Item initialement financé par le FCI

Serveur physique 32 cœurs 7Go 48To + 1To (Calcul Québec) (30 554 + 8 059$ ; total 38 613$)

L’hébergement des applications, de la plateforme collaborative et des données de recherche nécessite un serveur physique dédié. Celui-ci sera hébergé par Calcul Québec avec une sauvegarde automatique dans le cadre d’un rehaussement de sa plateforme infonuagique. La configuration du serveur permettra la création de machines virtuelles pour accueillir l’ensemble des projets des co-chercheurs et des étudiant·e·s au sein du laboratoire et mettre en place des « bacs-à-sable ».

## Scénarios possibles

Calcul Québec propose une allocation de ressource reposant sur l’infrastructure info-nuagique et d’employer une partie de la dépense initiale pour du salaire en développement.

<!-- requalifier la dépense FCI pour déployer des recettes -->

Trois scénarios sont envisagés :
- une solution hébergée sur la grille de Calcul Québec auto-administrée avec infogérance
- une solution hébergée mutualisée sur la grille de Calcul Québec avec un partenariat pour une partie de la maintenance
- la souscripton à un service cloud privé

2 enjeux pour l’équipe : 
- financement entretien
- expertise pour des solutions adaptées aux DH

Des sommes ont été budgétés au titre du Fonds pour l’entretien des infrastructures  pour le renouvellement et l’entretien des équipements. 

## Expression des besoins

Les besoins du laboratoire sont sans doute relativement représentatifs des projets qui peuvent être conduits dans le domaine des humanités numériques.
- utilisation d’applications métiers difficiles à héberger sur des solutions mutualisées du commerce hors cloud commercial (environnement Java, etc.). 
- hébergement d’une multitude de site web avec le recours à diverses bases de données
- conteneurs et bacs à sable.

Environnement
- Linux CentOS ou Debian ou Ubunutu

Solution d’administration serveur (Open Stack sur Calcul Québec)
- provisions virtual servers;
- installs software packages;
- creates users;
- starts code processes, etc. 

Comme il s’agit de partir de zéro et que nous avons le choix dans l’approche pour la gestion des services, dans la mesure où la compétence est disponible, nous envisageons de travailler selon un modèle d’opération Infrastructure as Code (IaC). 

L’automatisation repose sur l’utilisation d’utilitaires d’automatisation et de conteneurs.
- Terraform (network, security group)
- Gaïa (GUI pour Terraform)
- Cloudenet avec OpenStack pour ajouter scripts automatiques Ansible++
- Ansible++ pour le déployement des services

La partie du travail concernant l’automatisation d’OpenStack serait plutôt à la charge de Calcul Québec. La prestation de service qu’assume le laboratoire relèverait plutôt de l’utilisation de Ansible.

Solutions 
- CPanel
- openStack + Kubernetes
- Plesk Debian
- Digital Ocean, Amazon AWS et Microsoft Azure, Apache CloudStack, OpenNebula, ...
  https://www.openstack.org/
  https://marketplace.digitalocean.com/apps/cpanel-whm

Instantanés et sauvegardes (Snapshot et Backup)
- Snapshot (pour les restaurations) -- pas nécessairement une bonnée idée pour l’infrastructure, d’autres options sont possibles en particulier dans le contexte de script de création. Snapshot ne fonctionnent pas sans le BootInstance, pas une bonne option de backup.
- Privilégier Automated Backup, possibilité d’utiliser d’autres sites ou multisite. Sarah et Lydia explorent une option avec Obect Storage (Victoria) = Dual storage

Plage d’adresses IPv4 et IPv6
Le nombre d’adresses IP n’est pas un grand problème sur Beluga. Voir ce qui est le mieux sur Beluga.
2 adresses IP

Protection DDoS
Dépend de la plateforme, nombreuses options possibles : fail2ban, reverse proxy ?

Nb de CPU à évaluer. Pour ce qui est des traitements graphiques lourds dans le cadre de projets relatif au patrimoine, nous pensons avoir recours à des demandes d’allocations de ressources distinctes.

SSD pour le disque de démarrage et app

Le disque persistant doit être utilisé pour les fichiers de génération de projet, les fichiers de cache, les fichiers journaux et d'autres fichiers temporaires. 

Définir une bande passante publique minimale
Définir un traffic entrant et sortant gratuit

>La bande passante en direction de l'internet commercial est très limitée, l'utilisation devrait principalement être faire entre sites connectés aux réseaux de recherche nationaux, donc les universités, hopitaux, CEGEP et instituts de recherche (incluant les équivalents internationaux connectés à leurs réseaux de recherche).

### Sécurisation

Connexion SSH
Fail2ban
Pare-feu (interne iptables ou réseau ?)

Stockage de sauvegarde (FTPS, NFS, ou CIFS)

Quid Load balancer

### Hébergement d’applications web

- Serveur HTTPs (Apache HTTP, [Ningx Open Source](https://www.nginx.com))

Langages de programmation
- Java
- Python
- **NodeJS** / Deno / 
- Julia

Outils systèmes
- outils systèmes linux habituels (vim, ssh, etc.)
- npm / yarn
- utilitaire de gestion de version Java, NodeJS ?
- git
- etc.

Applications
- [BaseX](https://basex.org) XML native database
- [Cantaloupe](https://cantaloupe-project.github.io) High-performance dynamic image server in Java
- [Saxon](http://saxon.sourceforge.net) XSLT and XQuery Processor
- Base de données SQL [PostgreSQL](https://www.postgresql.org) et [SQLite](https://www.sqlite.org), en cluster ?
- Base de données en graph [Blazegraph](https://blazegraph.com), [Neo4J](https://neo4j.com)
- [Strapi](https://strapi.io)

Continuous integration avec Git
Automatisation
Kubernetes si mutualisation

Infrastructure as code + DevOps

- machines virtuelles
- réseaux
- équilibreurs de charge
- bases de données
- autres applications en réseau

### Stockage

SSD pour les applis et le cache et RAID

Stockage de données vidéo et son.

Gestion électronique de documents GED ou Serveur de stockage en réseau NAS

### Bacs à sable

Conteneurs Kubernetes

## Dimensionnement

Répartiteur de charge ?
Haute-Disponibilité

Réseau

- Bande passante privée
- Bande passante publique

Espace de sauvegarde



## Entretien

Devis qui évoque des frais de 12% annuel
Durée d’accès au service au-delà des 5 ans ?

## Offres commerciales

Gandi Serveurs VPS

V-R9, 53,21$ par mois

- 4CPU/8 Go RAM
- 25Go stockage extensible à 1To
- 1 IPv4/v6 incluse
- Trafic 3To inclus

V-R16, 148,71$ par mois

- 8CPU/16GB RAM
- Stockage 25Go, extensible à 1To
- 1 IPv4/v6 incluse
- Trafic 3 To inclus

OVHCloud
https://www.ovhcloud.com/en-ca/

OVH Rise-4
AMD Epyc 7371 -16 c/32 t-3.1 Ghz/3.8 GHz
Mémoire à partir de 128 Go

https://www.ovhcloud.com/fr-ca/bare-metal/

200 * 12 = 2 400/an soit 12 000
500 * 12 = 5 000/an soit 30 000

Un serveur dédié est un serveur physique situé dans l’un des datacenters. Contrairement à une solution d’hébergement web dite mutualisée qui sont techniquement gérées par l’hébergeur, on est entièrement responsable du serveur dédié.

Configuration réseau, mode bridge
Alias IP


Amazone AWS

Google Kubernetes Engine GKE

## Infogérance

Exemple d’infogérance
https://www.devclic.fr/conseils-services/infogerance/serveur/

https://circleci.com/blog/learn-iac-part02/

Vagrant

https://www.pulumi.com/


https://github.com/opencontainers/image-spec
https://github.com/opencontainers/runtime-spec

---

Points à discuter

- Specs
- Durée
- Entretien
- Solution


---


## To do

- [x] Lire le [papier](https://engagedri.ca/assets/documents/whitepapers/crihnLivreBlancNOIRN.pdf) (lmk)



## Instances

### Cacul Québec

Suzanne Talon en vacances jusqu'au 10 décembre donc à décider/acheter en janvier

### Calcul Canada

- [x] [Créer compte](https://ccdb.computecanada.ca/account_application) compute Canada (lmk)
- [x] Écrire à calcul québec (Lydia) pour savoir quelles sont les allocations disponibles (emcd)

Courriel échangé avec [Lydia Vermeyden](lydia.vermeyden@ace-net.ca), research consultant, responsable des DH

Observations: 

- Formulaire du service d'accès rapide (RAS) au ressources infonuagiques est incompréhensible.
- Il paraît inadapté que ce soit l'investigateur principal qui remplisse la demande de création d'instance alors que celui-ci ne réunit pas nécessairement les compétences techniques pour le compléter.
- La présentation des services infonuagiques et de la localisation du service est difficile à saisir pour l'hébergement d'applications web.



## Besoins

### Achat FCI

#### Option 1

plus cher mais plus d'espace

négocier usage au-delà des 3 ans

frais d'opération et de configuration 12 % 

- n'était pas éligibles au FCI 
- à reconfirmer maintenant qu'ils sont incorporés



#### Option 2 

moins cher et et moins d'espace

on requalifie la dépense FCI pour déployer des recettes
