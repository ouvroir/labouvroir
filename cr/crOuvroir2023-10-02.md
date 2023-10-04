---
title: Réunion labo
author: ouvroir
date: 2023-10-02
draft: 
tags:
     - cr


---

# Réunion de travail 

solliciter Jérôme


## Display

Plusieurs réunions ont eu lieu avec Lena, Zoë, David et Emmanuel pour travailler sur Display. Ces rencontres ont beaucoup fait évolué le projet. David Valentine travaille en particulier sur la partie modélisation et Zoë apporte ses fines connaissances de l’exposition pour mettre à l’épreuve le modèle.

Repo Display + repo diplay-ontology

Une première esquisse de modèle a été élaborée avec les technologies du web sémantique sous la forme d’une ontologie OWL dans le logiciel Protege. Définition d’un artefact et des relations entre les artefacts. Articulation avec l’ontologie Bot du W3C pour le domaine bâti.

Au-delà des séances de travail sur le modèle se pose la question de l’angle de travail à adopter sur les modèles. En partant de la proposition d’Emmanuel de travailler sur le modèle de la programmation visuelle, je me demande si on ne devrait pas travailler avec des blocs très simples pour pouvoir raisonner en termes d’échelle et d’incertitudes.

voir s’il faudrait penser quelque chose de vraiment modulaire (pas de dessin, juste des blocs) pour "forcer" la réflexion? Le dessin peut présenter l’inconvénient de permettre des variantes et de sortir des contraintes.

Questions d'interfaçage
- quand/comment on rentre les données
- rendu des données: 3D, [threeJS](https://threejs.org/), "rendu à plat" (cube déplié)

enjeu d'utilisabilité: saisie laborieuse, données lacunaires, besoins variables en reconstitution d'exposition

Point de départ du web sémantique: travailler sur les inférences pour les incertitudes



## Reframe

Discussion pour faire le point sur le projet avec Emmanuel.

Comment faire pour réinvestir des gens dans le projet? Designer, developpeur, à quel moment dans le projet: quand tout est conçu, pendant la conception? 

Concevoir des composants assez flexibles et abstraits qui réalisent un tâche assez spécifique. Travailler sur la logique entre le texte et l'image, et les interactions qu'on peut avoir au sein d'une page

Technologies vs approche. Besoin de faire une sorte d’état des lieux, des manières de présenter des images et de modéliser son articulation avec le texte : exemple mosaïque d’image, légende, etc. 
Il s’agit donc dans un premier temps de définir une typologie des modes d’affichage des images.

D’un point de vue technique, on s’oriente vers la définition de web components: ce qu’il y a de plus versatile, pas lié à un framework en particulier. Besoin de tester des manières de faire car il existe plusieurs manières de les utiliser. 
- Ex. Tailwinds où c’est surtout le CSS qui vient structurer le tout, problème de classes proliférentes. 
- ex. SlideJS qui permet de faire des slides show, api ouverte. Intéressant car une gross sémantique sur la manière dont la librairie est construite
- ex. MeltUI, Spectrum, Carbon approche centrée sur des composants JavaScript, laissant en grande partie CSS de côté

composant: en terme de layout et non en terme de stylage.

Modélisation et système abstrait

Périmètre de la mise en page et de l’interaction (voir les définitions du W3C dans CSS Grid et Dispay Flex)

Besoin auquel on répond (rapport IIIF et visionneuses, etc.)

Voir 
[musées numériques Canada](https://www.museesnumeriques.ca/)

Cas d’usages: 
- exposition numérique
- présentations interactives
- générateur de mise en page type album photo

Besoin de lister des cas typiques
Identifier si peut tout concevoir. Travailler avec un développeur. Quelle temporalité du travail ?

## Display - brainstorm
Mapper le SI de Display avec le cas d'usage d'exposition numérique

Définir un produit

- Objectif général
- Cas d’utilisation
- Fonctionnalités
- Saisie des données
- Sources - références


### question des vues de salles (option)

Automatisation de l’identification des œuvres possible dans le cas où l’ensemble de la collection est numérisées.
Analyse spatiale également possible.
- doctorants de Sébastien Roy qui travaillent sur l'espace → MITACS MNBAQ

Lister les sources (commons)
Granularité du rattachement à la source: souvent un problèmes dans les bd historiques. D'abord un problème d'interface: quand on entre une information, choisir une source et la lier. Travail serait habituellement séquentiel: analyse d'une source après l'autre. La plateforme peut être intéressante pour croiser les sources.

Common réunit des sources liées à des entités exposition
Liste des sources est ainsi déjà saisie.

Annotation https://annotorious.github.io

fonctionnalité optionnelle: segmentation/zones des images avec Pass

Explorer la possibilité d’un moteur d’analyse ?
- segmentation automatique des images
- reconnaissance d’objet
- analyse spatiale

Passage de l'analyse spatiale à une analyse formelle cf. Cardon *La revanche des neurones*

Faut-il projeter la documentation dans l’espace ou bien seulement l’information extraite.


### Fonctionnalités

cas d'usage
- documenter une exposition à partir de sources
- croiser les sources pour essayer de résoudre des inconsistences/incohérentes
    - documenter les contradictions
- produire des rendus

Carnet de laboratoire
- essais / choses qui ne fonctionnent pas 
- outil de prise de notes stéoroïdé pour documenter une exposition
- incorporer le processus de grammatisation de l'information
- fonctionnalités: 
    - entrer des données
        - importer une documentation (commons)
        - saisir une liste d'œuvres
    - aider à sourcer, repérer les inconsitution, résoudre les inconnus, produire une analyse de l'exposition
    - convertion des données dans le web sématique
    y a-t-il un besoin de dire explicitement les choses qu'on ne sait pas ? 

De quoi a-t-on besoin pour avancer ?
Que doit contenir le Cahier des charges ?
Quelles sont les prochaines étapes du travail ?

todo:
- hypothèses "idées" de ce que ferait le logiciel "si on fait ça, alors..."
    - contraintes
    - affordances
- former ainsi 3 scénarios, à ensuite mélanger ou exclure , ...


## Reframe - brainstorm

Usabilité
- à qui s’adresse le logiciel ? 
    - briques utilisables par d'autres après
    - modèle des web components

### web components

- interfaçage des web components (custom components) avec des paramètres à renseigner
    - pas une interface graphique
    - mais abstrait avec des paramètres et des fichiers de configuration

Utiliser des web components (standard du web) ou dans un environnement particulier (framework)?
Question de maintenance et de capacité à les programmer
- frameworks (ex: lit) facilient la mise au point
- svelte a un moteur de rendu de web components

À quel moment est-ce qu'on généricise? Ou on prototype d'abord et on généricise après?
terme "web component" custom element → element web custom: ne devrait pas demander de configuration. Il faudrait simplement importer un fichier, comme on importerait un .js. 

Maquettes de site?
Comment lister le périmètre des spécifications qu'on veut traiter?

### Analyse de l'état des lieux, exemples

recherche et collecte d'exemples déjà existants
mais sur le web, est-ce qu'on apprendrait encore beaucoup? Aller plus voir ailleurs
- jeux vidéo
- web documentaire
- ouvrages / revues 

Essayer de créer un langage abstrait pour définir la bibliothèque, basé sur un certain nombre de primitives. Se trouveraient-elles radicalement changées par des exemples? 
Ne pas se cantonner au web 

En même temps il y a plusieurs besoins de base qui ne sont pas satisfaits en ce moment

Faut-il s’essayer sur des modèles classiques ? Dans quelle mesure travailler sur des exemples plus excentriques est essentiel pour définir nos primitives.

Deux approches possibles
- on commence par le prototype d'un exemple, pas un code sur lequel on construit


### Layout

enjeu d'articuler des images et le texte

partir du bas ou du haut? 
- de la grille au module
- du module à la grille

sémantique de la page
- section
- article
- paragraphe
comment les composants interagissent et existent au sein de ces hiérarchies? ex: un composant doit exister dans un élément qui a telle propriété
Enjeux de cascade, prendre en compte les contextes

Est-ce qu'on veut créer des macro-templates? 

Inspiration de la bande dessinée? 
nouveaux formats de diffusion

Modèle
- ordre d'apparition? très classique

Complexité de penser du responsive (taille de l'écran) vs s'affranchir de la taille de l'écran 
Hayden: pratique commune du responsive avec des media-queries mais ça ne marche qu'à moitié, on fait des hypothèses sur la taille de l'écran. Approche d'*every layout* → penser des composants qui sont nativement responsive. Pas de cas limite car il n'y a pas de fourchette de taille

Épistémologie visuelle
- coordination des éléments

Il faut des cas d'usages, des corpus, des séances de travail.

## Travail avec Jérôme
travailler alternativement ou conjointement sur du co-design? plutôt alternativement.
Réfléchir sur les questions de typologie.

Avoir une discussion toutes les typologies. Faire travailler une assistante sur ce sujet.
Peut-être aurait-il un vocabulaire pour décire les typologies. Vocabulaire que pourrait mettre en œuvre dans l’interface.

Faire émerger un vocabulaire ensemble au cours d’ateliers. Tous les 15 jours. Si possible le lundi après-midi. 

## Suite

Quelle place pour IIIF ?

Définir un premier use case. Idées : 
- batiments civil, corpus de thèse d'Emmanuel,
- exposition en ligne, 3e chapitre de Valentine
- Comment montrer les NFTs ? (Encyclopédie, Nathalie Casemajor)
- chronologie de la muséologie numérique ? 
- partir d'une exposition en cours et penser sa version numérique? 
- Art public
- Righettino

Chercher un use case issu de l'encyclopédie si possible.

Base
- niveaux de titre & narration (regroupements type nav)
- visionneuse
- galeries
- texte en vis-à-vis d'une image

penser à prezi/sosie