---

title: Réunion IIIF bibliothèques
author: ouvroir
date: 2023-09-25
draft: false
tags:
     - cr
     - IIIF

---
# Rencontre de suivi 

Solution en voie de production de la part des bibliothèque : Utilisation de Dspace qui nécessite de définir un peu autrement les spécifications de l'API

Comment les bibliothèques souhaitent-elles travailler avec les données de recherche? 
- encore dans la définition de l'offre de service

Contexte: projet CRSH financé et porté par l'UdeM
Exposition des enjeux de la recherche du Partenariat/laboratoire
- enjeu d'hébergement à long terme (Martin va en parler d'avantage) de l'encyclopédie
- contenu de l'encyclopédie XML avec LEAF-writer, suivre les modèles d'openEdition
- projet reframe, librairie de mise en scène des images mais aussi des contenus éditoriaux (texte+image, exposition, mise en scène)

Site de Carl Therrien: exposition horizontale
- offrir un espace de conservation à long terme pour des publications statiques
- plus les technologies sont pérennes, plus on peut prévoir une conservation à long terme
- penser un acte de publication (pas de mises à jour régulières)

Prévu de diffuser une offre de service balisée dans les grandes lignes.

Encyclopédie
- pas une quantité d'images gigantesque donc pas un enjeu de stockage
- d'avantage un enjeu de responsabilité: qui prend la charge de la publication/hébergement des images?
- recherche d'un ancrage institutionnel pour la pérennité du projet

Question des images se distingue un peu des questions d'hébergment (possibilité de s'arranger avec Calcul Québec et Calcul Canada → organiser le transfert des choses)
Vraie question problématique: serveur configuré pour la gestion des images

Martin voit ça comme un dépôt sur lequel il y a des services
- côté humain: faire des recherches, consulter
- papyrus: coalition avec des copies réparties
    - préservation = responsabilité/mission des archives
- Même chose: volonté de travailler sérieusement sur la conservation et la sauvegarde, mais pas basé sur des normes
    - pas une mission de préservation mais grande mission de diffusion et inclut la conservation à long terme
- pensent, pour le projet de Carl Therrin notamment, de produire un DOI
    - maintenance du DOI va de pair avec l'idée de conservation à long terme

Implicitement, dans nos besoins, l'interface de dépôt de l'image on avait prévu de la construire
- la solution proposée par les bibliothèques peut l'offrir
- même principe que le dépôt dans papyrus
    - pipleline: déposant (qui se crée un compte) puis mécanisme de révision (chargé·e·s de révision/validation)
    - gesion des droits d'accès etc.

Accès autorisés face aux appartenances institutionnelles: projet multi-institution, ex est-ce qu'un compte UQAM aurait accès? 
- on peut avoir des comptes locaux (contournement au besoin)
- à suivre pour les comptes externes

Enjeux de la gestion des données de recherche actuellement en débat au sein du partenariat.
- politique de l'ouverture des données
- établissements se dotent actuellement chacun de leurs propres stratégies
- il faut bien qu'il y ait un établissement qui prennent la charge des données

Les bibliothèques auraient pu aussi proposer un accompagnement dans la mise en place du serveur d'image, duquel nous serions maîtres de la chose
2 arguments contre
1. la durée
2. spéclialisation: gens dont c'est le travail 

Calypso 2.0
- collections de l'UdeM 
- risque d'amalgame encore plus fort avec les bibliothèques de l'UdeM
- envie de mieux mettre en valeur leurs collections: travail identitaire qui s'applique aussi à d'autres contenus
- sinon, notions de communautés/collections, avoir des thèmes visuels/navigation différents par communauté. URL reste bib.umontreal.ca mais on pourrait le *brander* CIECO
- forme d'éditorialisation de la collection

Responsabilité de la mention de production des images  ou des droits qui s'y appliquent
- images produites par le partenariat
- images destinées à la publication

Bibliothèques perçues comme un peu plus neutres
Ce qui prédomine reste la question technique

## Calendrier
en attente après les TI (attente pour entente AWS pour ne pas s'embêter sur le dimensionnement (discussion depuis 1 an, le contrat est signé))
- initialement prévu après les fêtes
- mais retardé un peu pour la mise en valeur en amont des contenus

formation des sys admin la semaine prochaine
mise en place de la structure TI, cases encore à cocher: Contrainte technique des ti

Vise actuellement entre janvier et avril. 
Avoir des images sur un serveur à l'été ne devrait pas être un problème

Comment mettre en valeur cette collaboration ? Comment pouvons-nous aider dans ces prochaines étapes? 

Si approche très top-down, risque de prendre 5 ans pour savoir où va atterrir. À l’inverse, si collabore, trouvera que c’est fun.
Mais Martin propose d’écrire une page sur le service que l’on nous rendrait et en parlerait avec Stéfanie. Poser les balises d’une offre de service.

Stockage de vidéo → prévu.
Suite aux discussion avec TECHNES
Pas de solution de sauvegarde du travail vidéo des étudiant·e·s

Possibilité de diffusion contrainte. Par contre, la mission reste la diffusion: souplesse et facilité n'est pas le premier critère, nécessaire mais pas au cœur du projet.

Chercheur·se·s qui disent qu'il·elle·s n'ont pas de données de recherche: perception de ce que sont des données de recherche.

Numérique bouscule la notion de collection, mais aussi les catalogues de bibliothèques

À court terme, de quoi avons-nous besoin? 
- stockage d'images en IIIF le plus tôt possible
- ce qui nous permettrait de mettre en place les mécanismes de versement d'images

Pas de serveur de test, mais on peut avoir une recette pour installer ça en local sur un mac: display + serveur cantaloupe
- personnalisations calypso sont sur un github public
Faire les tests avec ça
- tester l'API
- voir l'interface de dépôt 
Façon court terme d'avancer
- échanger après si on a des questions

En octobre, sinon novembre: installation de serveurs (prod et pré-prod)

En parallèle, démarche politique pour s'assurer que tout va bien dans les annonces etc.

Modèle de l'intégration continue: pousser vers un répertoire git, puis avoir des github actions qui publient le site web vers un serveur

Émir dit qu'il y a, pour les mises à jour, un système qui fonctionne, pas loin du 100% automatisé. Martin va regarder ce qui a été mis en place.

Nom de domaine: encore cas par cas. On va vouloir un nom CIECO. 

Martin va avancer sur le côté politique, voir comment les bibliothèques se positionne, et va nous contacter avec ses notes d'install. 