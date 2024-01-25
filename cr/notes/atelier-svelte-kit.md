---
title: Atelier Svelte
desc: notes atelier svelte
author: Ouvroir
date: 2024-01-24
draft: false
tags:
    - atelier
    - sveltekit
    
---


## Presentation de Svelte
Emmanuel Château-Dutier

### Site dynamique
Un site dynamique désigne un site sur lequel certaines pages sont des pages dynamiques, c’est-à-dire des pages créées à la demande (on parle aussi de page générées « à la volée ») par le serveur. Le contenu des pages dynamiques va donc changer sans que cela soit le fait du webmaster.

Les pages seront générées en temps réel à partir d’informations contenues dans des bases de données en fonction d’interaction avec les internautes. Exemples de paramètres d’interaction : date et heure, numéro d’article, caractéristiques de produits,…

Modeles classiques site web de dev web dynamiques = maj se fait de maniere dynamique du cote du serveur. Les pages sont servis par php, script coté serveur. 
Un web plus dynamique, mieux mis à jour. Appele aussi web participatif ou [web.2.0](//https://fr.wikipedia.org/wiki/Web_2.0)
Facilite production des pages en utilisant systeme template.
Wordpress par cette infrastructure 

### Site statique

Retour à la publication de sites statistiques. 

Un générateur de site statique (static site genetors – SSG) est un programme qui permet de créer des sites web à partir de fichiers textes en langage HTML. Ces fichiers sont ensuite convertis en fichiers binaires par le serveur web avant qu'un utilisateur face une requête. Cela permet donc de réduire la charge du serveur et d'améliorer les performances du site.
Les avantages du générateur de site statique sont nombreux : 
- mise en place est rapide et facile
- possible d'héberger le site n'importe où
- coûts sont faibles
- site est facilement modifiable, car il suffit de modifier le code source HTML.

[Générateur de sites statiques](https://fr.wikipedia.org/wiki/Générateur_de_site_statique) 
- pile de fichiers enregistres encodes avec un format comme Markdown 
- generer des templates pour les differentes parties de pages + transformations 

HTMC 

[Static Site Generator](https://staticsitegenerators.net)
simplicité, reduction des dependances, meilleure maintenance parce que moins de pulgin
vise une facilité de deploiment.
fonctionnement d un générateur de site statique SSG

[Jeckyll](https://jekyllrb.com) le plus connu, crée en 2008 
Hugo (2012) 

### Javascript
[langage JavaScript](https://fr.wikipedia.org/wiki/JavaScript) 

JavaScript est un langage de programmation de scripts principalement employé dans les pages web interactives et à ce titre est une partie essentielle des applications web. Avec les langages HTML et CSS, JavaScript est au cœur des langages utilisés par les développeurs web.

 Javascript prend le lead.
1999 Javascript prend le lead. introduction de XML HTTP REqest va revolutionner le web statique puisque permet de faire requetes sans avoir à rechercher la page web. 

[AJAX](https://fr.wikipedia.org/wiki/Ajax_(informatique)) permet maj de la page grace a moteur AJAX, permet interaction plus rapide avec serveur.

modèle asynchrone 

Le [DOM (Document Objet Model)](https://en.wikipedia.org/wiki/Document_Object_Model) est une interface de programmation normalisée par le W3C, qui permet à des scripts d'examiner et de modifier le contenu du navigateur web.

Appariation de multiples frameworks JS 
https://programmingsoup.com/history-of-javascript-frameworks
Frameworks JS :
1997 ECMA
2006 jQuery
2010 KnockOut.js
2010 Backbone.js
2010 AngularJS (Google)
2011 Ember.js
2013 Meteor.js
2013 React (FaceBook)
2014 Vue.js
2016 refonte d AngularJS 

Nv type d'application : les singles pages (applications monopage) [SPA](https://en.wikipedia.org/wiki/Single-page_application)

Libraires qui permettent le developement  de singles pages à l'int de laquelle tout est codé ce qui facilite le chargement de la page et les requêtes. 
applications lourdes mais fluides (lesquelles? les singles pages???) idk lol

[Headless CMS](https://en.wikipedia.org/wiki/Headless_content_management_system) 
dependance aux CMS classiques s'est considerablement reduite, appartition d'un autre modele Headless CMS
permet notamment séparer la production des pages
la plus part de gest de contenu utilise MD  

[jamstack](https://jamstack.org)
https://fr.wikipedia.org/wiki/Jamstack
a reuni toutes sortes outils et a permis d animer le dev web dont Svelte .

Quelques applications qui servent a construire des sites web :
Astro generateur de site statique 
Gatsby 
Next.js
Svelte : Interet du Labo

### Svelte, SvelteKit
fondé par Rick Harris en 2016 

Différence ne travaille sur un virtuel DOM, mais sur un modèle compilé.
propose un lg assez proche d'HTML 
permet d'utiliser de blocs de contenus pour le stylage des pages
pages generee par processeur puis genere stacks de pages, html classique = meilleure conservation. 
pages sont rendues du côte serveur ou client permet d'adopter des solutions adaptées à differents cas de figure


## Présentation
William 

[Fiche mémo : Svelte](https://github.com/ouvroir/atelier-svelte#atelier-sveltekit-de-louvroir-dhistoire-de-lart-et-de-muséologie-numériques)

Cet atelier ne vise pas à vous rendre spécialiste mains introduire à ces notes.
A la fin de la journee, début de blog. 

Poser bases contextuelles ce matin et cet après-midi coder ensemble.

Node 
NPM 
Vite

tout est noté dans le package.js

installation des packages qui se trouvent sur npm registry

app.html = template de base

.d.ts = fichier pour definir types de certains fichiers de l appli

dans dossier lib : dossier composants
Donnees peuvent etre la ou dans static (si besoin d etre dans le build genre logo). 

dossier principal : routes
c'est la qu'on met les fichiers md 
tous les fichiers doivent etre nommé +page.svelte

layout peut etre adressé à son dossier.

style.css

+page.server.js : export fonction asynchrone qui communique donnees dans une page. exectuee en premier.
fonction asynchrone : load independant de l'affichage.

$: reactif statment 
Consol log : permet d afficher la console pendant le dev

CSS que william conseille :
padding 1.5rem 

display: grid
grid-template-columns 


Creation compenents dans lib et fichier card.svelte

pour mettre en ligne : 
https://pages.github.com

