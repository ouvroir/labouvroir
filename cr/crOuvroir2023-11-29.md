---
title: Réunion de laboratoire
description: Compte-rendu de la réunion hebdomadaire du 29 novembre 2023
author: emchateau
date: 2023-11-29
draft: false
tags:
    - cr
---


# Admin

## website (images des projets et question mise en ligne)

Passage en revue du site.
Il manque des images pour l’Encyclopédie, Capitals index, 

Automatisations, sur chaque repo un token. Pour certaines actions, besoin d’un token.

Ne pas changer de repo pour la mise en production. Plutôt mettre un fichier CNAME (sans extension) avec l'url www.ouvroir.umontreal.ca à placer à la racine du repo. Penser à enlever la redirection dans les settings du repo ouvroir.github.io


- reframe

afficher les containers

L'image comme primitive : 
- Comme une image s'affiche dans son ratio ? 
- comme elle fonctionne dans un conteneur
- Quels sont ses attributs (annotations, légendes, etc. IIIF)
- Articulations par rapport à du texte
- Comme deux images intéragissent entre elles ? ()
- Comment des images s'affichent dans un conteneur (ie. gallerie)
- Quelles sont les interactions liées à ces conteneurs ? 


Quelle place des visionneuse IIIF dans l'ecosystem ? Les visionneuses ne font que ce que décrit l'API de présentation IIIF.  


paradigm:
    - comparaison
    - vis-à-vis,
    - gallery (type)

layouts
    - grid

items (primitives):
    - image viewer
    - text
    - annotations

iteraction
    - image to text


Quel est le lien entre l'implémentation technique (reframe) et la modèle abstrait ?


- NAS/vidéo, 
- Trium

## reframe

Poursuite du travail dans Webkit.

Réalisation de nouveaux modèles.

Continuer à poser des questions sur la place respective de CSS et de JavaScript.

Sans JS du mal à voir la place d’autres types de stratégies.

Sur le fait de penser le projet du layout vers le conteneur plus général. Actuellemen traite des layouts, donc du mal à détecter des problèmes. Mais l’impression de passer à côté de certains problèmes. L’idée était cependant d’avancer tête baissée pour identifier des difficultées.

Maintenant, voudrait laisser de côté la question du Layout. Jusqu’ici des questions liées à la place respective des composants, de JS et de CSS pour discuter.

Voudrait donc revenir à des questions évoquées. Travailler sur les Layout peut être pas la force de Reframe, mais travailler sur les conteneurs d’image. Ne devrait-on pas à cette étape repartir sur un viewer OpenSee dragon ou visualiseur de CogApp (intéressant car des webcomponents).

Layout qui permet d’éviter d’avoir à gérer des breakpoint. Pourrait avoir besoin de garder des effets de proportion grace à la librairie et ses dégradations possibles. Veut-on définir un emplacement ou une proportion.


R bien un projet JS
Conteneurs et légendes
Affichage paramètres



# Coordo

Atelier de segmentation

Présentation

La segmentation d’images. Pour une classification sémantique des artefacts culturels.

La segmentation est une opération de traitement des images qui consiste à détecter des zones d’intérêt dans des images en rassemblant des pixels en fonction de critères choisis par les chercheurs. Cette technique s’inscript plus largement dans le domaine de la vision par ordinateur. 

Il s’agit d’une procédure qui s’inscrit plus largement dans les applications de l’intelligence artificielle comme d’autres approches dont nous avons discuté au sein du laboratoire par exemple pour le texte.

Il existe plusieurs manières de segmenter les images. Plusieurs types de segmentation sont utilisées.
La première approche est la segmentation sémantique. Dans cette approche on se concentre sur l’identification et la classe des pixesl d’une image, sans distinction de leurs instances.

Dans l’approche par insatnce, on identifie et classe les objets au sein d’une image. Cette segmentation se fait au niveau de l’objet.

Il existe encore une approche distincte qui sera dite panoptique dans laquelle on identifie et classe tous les objets présents dans les images.

Au-delà de ces différents types de segmentation, cette approche peut également rpendre différentes formes.
- groupes de pixels
- boites englobantes
- lignes
- cercles
- polygones

Pourquoi faire de la segmentation ? Il s’agit notamment de pouvoir classer les images en fonction de leur contenu ou de leur signification. C’est une opération qui permet de faire de la classification en attribuant des images.
Entourer en rouge une partie d’image concerne la segmentation, le fait de l’identifier comme un objet, c’est de la détection.

La détection d’objet consiste plutôt à identifier des objets dans une image. La segmentation cosnsite plutôt à découper les images. Il ne s’agit pas nécessairement d’étapes successives dans un cheminement. Les approches peuvent être combinées entre elles.  La différence entre l’object détection et la segmentation d’instance relève plutôt d’un changement de granularité.


Avant d’aller plus loin sur la segmentation, il peut être utile de revenir sur le fonctionnement des modèles. On parle généralement dans ce domaine de réseaux de neurones par analogie avec le fonctionnement du cerveau humain. Ces réseaux analyse des images en les séparants par partie d’intérêt et grace à différentes opérations statistiques ces parties sont traitées dans des couches pour identifier des objets. Lorsqu’il y a une erreur, le réseau est capable de s’autocorriger. Au terme d’un nombre suffisant d’entraînement, 
Réseaux de neurones convolutifs les plus efficaces pour l’analyse d’images, en raison de leur architecture et de leur capacité à extraire des informations locales.

Flux de travail, acquisition d’iamegs, création d’une Bdd, annotation, entraînement, résultat de la segmentation.

L’entraînement consiste à perfectionner les modèles pour les entraîner et améliorer les résultats. Pour cela part de vérités de terrains, cad de données empiriques qui sont validées par des utilisateurs humains. Il est possible de partir de données déjà disponibles ou de créer ses propres jeux de données.

Plusieurs approches sont possibles
- méthode supervisées [détails]
- méthode non-supervisées [détails]
- méthode semi-supervisées [détails]

Le choix entre ces méthodes dépend de la masse critique de données disponibles et du temps passé pour l’annotation. Enjeu d’équilibre. L’objectif est de créer suffisamment de données tout en passant un temps minimal pour l’annotation. Ces questions au cœur de la réflexion.

## Outils

Comment faire de la segmentation sur les images. Plusieurs outils et plusieurs modèles. Pour commencer besoin d’un modèle. Bien sûr peut faire de l’annotation sur photoshop mais clairement pas conseillés. Il existe plusieurs outils libres ou propriétaires qui sont spécialisés dans ces tâches. Pour délimiter des zones, leur attribuer des classes avec des niveau de complexité différentes selon les projets de chacun. Certains outils permettent d’utiliser des modèles de segmentation pour faciliter le travail.

Pour la segmentation automatique, il existe de nombreux modèles de réseaux de neurones. On a surtout parlé de réseaux circonvolutifs. Le modèle Mask R-CNN fait de la reconnaissance de région au sein des images par instance et par application de masque. Autre modèle utile Yolo qui divise l’image en grille et au sein de la grille détecte des objets en les rattachant à des classes d’objet déjà bien identifiées. Modèle qui reconnaît déjà une classe d’objet.

Montrer que les modèles répondent à des questions conditionnées par leurs donnés d’entraînement. Exemple pour la revue Opus international. Outre le fait qu‘il ait retourné l’image, le modèle a bien réussi à reconnaître une personne mais pas les deux. Et parapluie qui n’est pas présent.

Il existe des outils construits sur des modèles de réseaux de neurones et destinés à réaliser d’autres tâches que simplement reconnaître des objets. Souvent il s’agit d’outils construits en utilisant des librairies Python comme PyTorch, TensorFlow, etc. Comme ces librairies sont développées en Python, implique de savoir coder pour les utilisées.

Se pose aussi la question de savoir qui produit ces outils. Les librairies de base souvent développées par des GAFAM. DAns mes tentatives pour la segemntation de revues, a cherché à identifier des outils pour traiter la presse. Layout Parser semblait intéressant car entraîné pour travailler sur la presse du XXe siècle.

Documentation mal faite. Problème de reproductibilité même si en libre accès. Besoin de pouvoir l’installer et l’appliquer aux environnements de leurs propres auteurs. Problème de dépendances. Librairie 

Discussion sur layout parser et sa vocation à génériciser

Quelques outils génériques ont été développés pour essayer de résourdre des cas génériques. SegmentAnything modèle de réseaux de neurones. Segmentation panoptiques. Résultats très intéressantes. Parvient bien à séparer tous les éléments. Parfois à combiner des parties mêmes lorsqu’elles sont interrompues. Un outils que voudrait utiliser.

Si très intéressant pour le travail de Léa, pour Alice moins intéressant. Le logiciel parvient à détecter les images mais pas le texte. Mais aussi intéressant de comparer pour voir à quel point des outils sont pertinents ou pas les uns par rapport aux autres. Ce qui intéresse Alice dans son travail c’est de pouvoir délimenter les rapports entre les objets dans la mise en page plutôt que la détection d’objets.

Pose aussi la question de la balance à trouver entre les modèles que veut utiliser et leur implémentation technique et ce que l’on donne en entrée. Peut être d’abord de savoir comment traite pour commencer l’image. Quels filtres, etc. comment repère certains éléments.


D’autres outils sont plus spécialisés pour d’autres tâches. Exemple eScriptorium. Intéressant pour reconnaître du texte. Transkribus dispose d’une base de données publiques.

Essai d’utilisation d’Abby fine reader (outil propriétaire). Accès par l’intermédiaire de Huma-Num.

## Formats

Pas d’outils ou de solutions clefs en main, chaque outil amène des problèmes spécifiques. Question de savoir comment travailler dans des environnements plus standardisés et avec des formats plus réfléchis.

Enjeux et difficultés liées à la segmentation. Comment savoir comment fonctionne ? il existe de nombreuses métriques pour qualifier le résultats des modèles. Le f1-score est très utilisé. Le scole IoU intersection over union plus le score est élevé plus la segmentation a été performante.

Quelles erreur rencontre-t-on ?
À gauche, une simple erreur dans la segmentation des objets, reconnait bien l’objet mais manque des pixels. À droite, bonne reconnaissance, mais parties mal localisées. En ce qui concerne l’OCR, problème d’ordre. Exemple ArkIndex avec Teklia. Reconnaît bien les colonnes mais ne reconnaît pas le texte dans le bon ordre... Pas utilisable dans l’état. Ensuite nombreuses erreurs liées au fait que dans une revue le texte et l’image sont poreux. 

Essais CorDeep surtout concentrée sur la reconnaissance et la classification d’images. Palateforme entraînée sur des manuscripts. Génération de texte à partir de fils.

Enjeux d’accessibilité, de reproductibilité et d’interopérabilité.
Il existe de nombreux modèles développés par toute sorte d’acteurs, fonctionnent dans des environnements différents. Pose la question des formats de données et la manière dont peuvent s’inscrire dans différents environnements. Pas de corpus homogènes. Ensemble d’outils conçus dans des logiques de projets. Se comprend car une opération intellectuelle. Mais un enjeu important pour pouvoir produire des tâches de base facile à prendre en main pour les chercheurs.

Un domaine qui reste très fragmenté. Des outils qui évoluent rapidement et risque de devenir obsolètes. Outils qui risquent rapidement de devenir obsolètes car plus maintenus ou mal documentés. Un aspect crucial aujourd’hui autour de la standardisation et l’interopérabilité. Besoin de formats facilement lisibles établis selon des standards communs. Exemple ChatGPT, IA ouverte et en open access.

Amène à des questions d’éthique des données. Nombreuses questions.


## Vers la création de standards pour l’annotation des images

Sur les formats

Différents formats d’enregistrement. Les différents outils présentés permettent d’obtenir des résultats de coordonnées. Polygones ou boites. Souvent enregistré en JSON.

Pas de SVG, coordonnées de pixel.

FOrmat d’export des diférents logiciels. Types d’exports différents. Cf. Tropy.

Idem pour la description des documents même si un effort pour les formats développés.
