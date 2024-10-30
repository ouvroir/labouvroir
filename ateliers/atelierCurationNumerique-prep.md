---
title: Préparation de l’atelier «Curation numérique»
author: ouvroir
date: 2022-03-01
description: Rencontre de préparation pour l’atelier de Curation numérique
category: cr
tags:
    - atelier
    - cr


---

# Atelier «Curation numérique»

10 et 17 mars 

- B-343 de 13h à 16h
- B-351 de 16h à 19h -> en mode self service pour les étudiants de Kristine?

## Déroulement de l’atelier

Kristine est inquiète que Juncture serait trop difficile pour les étudiant·e·s. <!-- -> finalement après les échanges, c’est ok.-->
Emmanuel voit deux avantages:

- rédaction des contenus en markdown
- niveau d’utilisation des ressources variable: plusieurs types de contenus interactifs

Choix de sujet / sources disponibles

- cours de Kristine: choix d’un thème: 
  - 3 objets liés au sujet
  - chaque objet a un label (75-150mots) et un cartel
  - texte d’introduction (350 - 500mots)
- Emmanuel: reprendre un sujet et le "raconter" différemment
- contenus IIIF: Gallica, Met, [Artstore de JSTOR](https://about.jstor.org/librarians/artstor/)



## Juncture

[tests Alix](https://github.com/digitalArtHistory/publicarchi) code dans le dossier + petit [wiki](https://github.com/digitalArtHistory/publicarchi/wiki/Compilation-des-composants-Juncture)


Page d’accueil: faire une page d’accueil comme vitrine des projets? 

Utilier github directement dans le navigateur: 

- créer une branche 
- faire un PR pour ajouter au main

Contenus: 

- carrousel IIIF
- images
- tableur
- iframe
- chronologie
- graphiques / network (à tester)
- cartes (à tester)

pas de module de galerie? 

- carrousel IIIF (si on met plusieurs visualiseur IIIF à la suite, ils sont concaténés sous la forme d’un carrousel)


## Continuous integration

### repo collectif

Travail en ligne: on ne voit pas immédiatement ce que ça donne <!-- pour réler cela, on peut faire ajouter automatiquement un bouton de visualisation comme celui proposé par Juncture -->

deploy le site depuis github action? <!-- peut-être pas nécessaire de faire intervenir un GH Actions vu que le déploiement se fait tout seul -->

Déployer une instance ?

on s’occupe de rassembler le travail des étudiant·e·s

### étapes individuelles

- chacun crée un compte github (cf. https://semestriel.framapad.org/p/juncture)
- branche à leur nom
- dossier avec leur page
- y inclure les images? 

partir du template de base ~~ou construire from scratch?~~ -> le template contiendrait le bouton `<a href="https://juncture-digital.org"><img src="https://juncture-digital.org/images/ve-button.png"></a>`, mais on ne part pas du template de Juncture mais d’un template fait maison (avec les paramètres  )
structure le récit, étapes incrémentielles

page READ.ME contient un bouton qui parse le répertoire github et le site de juncture affiche le contenu interprété

## Étapes de l’atelier

Quelles étapes pour faire avancer pédagogiquement? 

Heure 1: "cours"

- présentation du cadre de l’exercice: story telling digital 
- présenter l’outil Juncture
- présenter l’exercice attendu (et la deuxième session pour enrichir)
- présentation du modèle
- rapide cours sur la syntaxe markdown + hyperlien
- pour en savoir plus: aspect plus technique envisageable lors de la seconde session
- démonstration avec explication des composants et comment la "publier", différents exemples de visualisation

Démo dirigée: Set group of steps that are done together (prise en main collective)

Heures 2&3: travail individuel 

- prévoir une pause

- mode atelier avec accompagnement individuel
- feedback et présentation / débuggage pour ceux qui veulent 


Tout le monde doit avoir: 

- une galerie IIIF
- un autre contenu à choix
- une carte.



---


---

title: Juncture
date: 2022-03-04
category: cr
lang: fr
tags:
    - atelier
    - cr
description:

---


Avant la démonstration : 

- on crée et déploie une application Juncture pour l’atelier --> :ok: cf. https://github.com/digitalArtHistory/recits-numeriques
- on paramètre la home page de l’application :ok:
- on crée plusieurs dossiers (1 par étudiant) nommés avec des chiffres (liste dans le pad pour qu’ils déclarent leur projet) --> :ok: cf. https://github.com/digitalArtHistory/recits-numeriques/pull/2
- dans chaque dossier, avoir une coquille (bannière + bouton) :ok:

## Introduction sur le story telling

Récits visuel et histoire de l’art

- Storymap https://story.maps.arcgis.com/apps/Cascade/index.html?appid=f4fd10e5f8d24d0eb7a02e33fa4c03f5
- https://medialab.github.io/portic-storymaps-2021/fr/
- https://vinepair.com/wine-colonized-world-wine-history/#1

## Présentation de Juncture

[Juncture](https://juncture-digital.org/) est un projet expérimental de l’organisme à but non lucratif JStor destiné à publier des essais visuels interactifs. L’utilisation de Juncture ne nécessite aucune connaissance informatique mais permet de présenter des essais enrichis avec des ressources visuelles, avec des cartes ou des données.

Présentation des fonctionnalités

- sections interactives
- images avec IIIF (metadata, zoom, gallerie, annotation)
- références Wikidata
- données tabulaires, cartes et chronologies


Pour la démonstration : 

- montrer comment modifier un fichier dans Github
- chaque étudiant prend un dossier le renomme d’après son sujet
- demander aux étudiants de donner le titre de leur travail (dans le pad https://semestriel.framapad.org/p/juncture)
- on fait un pas à pas ensemble, où on ajoute petit à petit les choses dans la coquille de départ
  - ajout de texte (rudiments Md)
  - ajout de titres
  - ajout de liens
  - ajout de listes
- petit à petit on intègre les éléments de visualisation Juncture
  - image sans IIIF
  - image IIIF (avec ou sans seq)
  - liens Wikidata
  - vidéos
  - tablestructure
  - timeline
  - map
  - network

## Références

### Juncture

voir https://demo.hedgedoc.org/Ep664DZES7CifJ9JHO-RMA?edit

https://semestriel.framapad.org/p/juncture

### Ressources

Collections IIIF

- [Gallica](https://gallica.bnf.fr)
- [Metropolitan Museum of Art](https://www.metmuseum.org)
- [Getty](http://www.getty.edu/museum/)
- [Paris-Musée collections](https://www.parismuseescollections.paris.fr)
- [Bibliothèque numérique de l’INHA](https://www.inha.fr/fr/bibliotheque/bibliotheque-numerique.html)

- [Biblissima](https://biblissima.fr)
- [Vatican Library](https://digi.vatlib.it/)
- [British Museum](https://www.britishmuseum.org/collection)
- [Morgan Library]
- [Wellcome collection](https://wellcomecollection.org)
- [Digital Library of Medieval Manuscripts Viewer](https://dlmm.library.jhu.edu/viewer/#dlmm)

https://iiif.io/guides/finding_resources/3

# Juncture

Juncture est un cadre de travail libre et ouvert pour produire des essais visuels engageants à partir de simples fichiers textes.

Au cours de cet atelier, nous vous proposons d’expérimenter l’écriture d’un essai interactif sur le sujet de votre choix.

## Avant la séance

- Créer un compte GitHub
- Se familiariser avec la syntaxe Markdown


## Essai d’exemple

Les monuments de Paris

- Jeu des monuments de Paris
  https://gallica.bnf.fr/ark:/12148/btv1b530061678.item

https://gallica.bnf.fr/ark:/12148/btv1b53029838s

Wailly, Charles de (1729-1798). [Premier projet de l’Odéon, 1786].
Plume, encre de Chine et aquarelle ; 30 x 57,3 cm. Paris, Bnf http://gallica.bnf.fr/ark:/12148/btv1b10303500d

- Arc de triomphe --> Chalgrin
- École nationale des Beaux-arts --> Duban
- Colonne de Juillet --> Alavoine
- Bibliothèque Sainte-Geneviève --> Labrouste
- Opéra --> Garnier

- focus Haussmann

une carte
une image annotée
des liens vers Wikidata
Statistiques