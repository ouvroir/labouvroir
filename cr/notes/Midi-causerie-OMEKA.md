---
title: Midi causerie : De la bibliothèque numérique à modélisation de connaissances : Omeka S et sa communauté
author : ouvroir
date : 2023-11-01
draft: false
tags:
     - cr

---

De la bibliothèque numérique à modélisation de connaissances : Omeka S et sa communauté

Philosophe de formation. 
Archives Point Carré

## Omeka

### Présentation

logiciel libre GPL, pour faire des bibliothèques numériques, des expositions virutelles. Pas d'usages véritablement recommandés, assez versatile. On l'utilise pour faire des bases de données historiques.
N'est pas conçu pour effectuer une seule chose. 

Equipe de dev au USA au Center for History Etait affiliée à l'uni George Mason mais maintenant une Digital scolar (but non lucratif) a repris le dev avec la même équipe.  Les meme qui dev Zotero. Licence libre donc tout le monde peut le dev. 

Deux versions:
- Omeka classic 2008
- et OmekaS 2017

Pourquoi deux versions ? Classic orienté vers l'individu (chercheur) basé sur un framework Php (Zend). OmekaS est basé sur les institutions avec séparation des contenus et de leur exposition. Utilise le Web sémantique. Utilise un autre framework php (Laminas)

### Avantages
*Quels avantages à utiliser l'un ou l'autre ?*

ref de la cathédrale et du bazar... Omeka entre les deux. 

- Logiciel très facile a prendre en main. Mais omeka ne peut être utilisé directement. (sauf par le bac à sable...)
Très facile d'alimenter la base de données
Concurrents : Eurist (logiciel bdd) accessible en quelques clics; archX; 
- Décrire et mettre en relation des entités intellectuellles (item), illustrées ou non (media)
- en respectant des standards (DC, vocabulaires du web sem, etc) et sans enfermer les données. 

Omeka fait bcp de choses ET pour les humanités numériques. Permet de tester à peu de frais mais aussi aller plus loin. 

Omeka S : gestion multisites

Visualisation de données : 
voir dans les modules. https://omeka.org/s/modules/Datavis/
mais parfois il vaut mieux le faire à l'extérieur. 


### Démo

Site de test. Accessible en fr. 
Saisie par formulaire. Utilise vocab ds format web sem. Propose des vocabs mais permet d'importer les notre du moment que c'est au bon format standardisé. 

Possibilité de placer ressources sur des cartes. 

fonctionne avec des modules. 
création de modules de ressources à partir du vocab. 
Piocher informations dans bases de ref. 
Pour personnes : idref
Permet de remplir completement les données. 

Importation : installer module import csv. 
aller sur le site de modules d'omeka. 
Telecharger zip. Envoyer ce zip dans le serveur au bon endroit. 
Installer sur la fenetre d'omeka et bam. 

#### digital muret 
travaille sur Omeka. 
Peut importer tout les contenus dans sa propre biblio. Filtre possible. 
Add Import
mettre la root. 
possibilité de mettre un filtre. 
liste des contenus. 
=> interopérable et ouvert. 

#### archives bourbaki
Module pour definir les relations: 
typer relation : module itemrelation
projet débuté en latek. 
Pas de TEI parce que l'équipe n'est pas formé pour et parce que l'objectif est la modélisation du contenu non d'edition. Pas une priorité. Bien que la tei aurait permit de dire où est la citation dans le texte + transcription aurait été directe. 
- Creation ontology
- Importation dans Omeka
- Recreation d'une bdd en rdf

Coeur du projet : pouvoir importer de manière fine le corpus. Sparql permet de faire des recherches complexes. 
Nicolas Lassol a créer cet outil : dev l'extrapolation des résultats. 

**Est-ce qu'on peut utiliser OmekaS comme un headless CMS ?**

On peut utiliser conjointement Tropy.org (pour le travail individuel sur les images) qui se connecte bien à Omeka

*problème de conciliation TEI et logique BDD*
Prob techniques mais on va vers cette solution. Communautés dissociées donc diffucltés. 
Item développe un module TEI pour Omeka C. 

*Envisager Omeka pour Display.* Omeka : mise à plat de l'ontology. Synthaxe des dates non confirmées pour notre fuziness? 

### Editorialisation

Création d'un site super simple.
Selectionner dans notre bdd les contenus qu'on souhaite. 
En fonction des modules on peut aussi faire des chronologie etc.
Création de blocs. 
Possibilité de styliser le texte
Permet de publier sur le web sans compétance web. 

Peut creer site sans base de données et récupérer les information d'autre part. 

*Peut-on gérer manifeste IIIF?*
Oui. add media : importer en IIIF image ou IIIF presentation 
Peut être modéliser grâce à modules. 

### Communauté

Association liée à la pérennité des projets numériques. 
Les projets meure, ne sont plus accessibles. Que faire? 
- preserver les meta données et les fichiers
- preserver le code ( fonctionnalité)

Doivent etre de qualité et reutilisable. 
- alignement sur des schémas de meradonnées standardisés
- usage de ref d'autorités
- entree et sortie libres des meta données : API, OAI-PMH, SPARQL, IIIF, CSV....
- traitements tech interopérable et reproductibles (ex: IIIF)

Mais il faut aussi sauv le logiciel : 
comment gerer transition entres les deux versions omeka S et C
- on peut archiver le code (software heritage)
- logiciel evoluent ineluctablement 
- evolution plus complexe que le simple remplacement d'un outil obselete
- projets orphelins
- plusieurs versions cohabitent

Réponse : créer communautées
- autour logicel, outils, technologie
    - comme lien entre des usagers aux profils variés
    - transdisciplinaire
    - facteur de résilience et d'adaptabilité face au changements

Association AUFO : 
- creation d'evt : journées. Présentation de projets omeka
- structuration asso loi 1901
- bureau de 6 personnes
- réseau de 198 personnes. 
- n'importe que peut poser questions à un réseau

abonnement à la liste : omekafr-asso@groupes.renater.fr
=> objet "suscribe" à envoyer à omekafr-asso-request@groupes.renater.fr

### Liens 
[Modules officiels d'OmekaS](https://omeka.org/s/modules/)
[Modules libres](https://github.com/orgs/omeka-s-modules/repositories)
[Module d'importation CSV](https://github.com/omeka-s-modules/CSVImport)
[digital muret](https://digitalmuret.inha.fr/s/accueil-muret/page/accueil)
Site en Omeka C [archives bourbaki](http://archives-bourbaki.ahp-numerique.fr/) 
[Tropy](https://docs.tropy.org/) Tropy is free, open-source software that allows you to organize and describe photographs of research material. 
[OmekaS REST API](https://omeka.org/s/docs/developer/api/rest_api/)
[records in context ontology](https://www.ica.org/en/records-in-contexts-ontology)
[archX]()
[reserch space by British Museum](https://researchspace.org/)
[AUFO - Association des Usagers Francophones d'Omeka](https://omeka.fr/)
https://omeka.org/classic/plugins/AvantRelationships/
https://omeka.org/s/modules/Datavis/?fbclid=IwAR1_CmaaGSN5oIQNE_1msJWXX4YB-ULc4pDaAGDX4MrJ1wng6Ta4DW61VVQ 


