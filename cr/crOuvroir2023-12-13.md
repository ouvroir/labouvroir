---
title: Réunion du laboratoire 2023-12-13
desc : réunion de la réunion hébdomadaire du 13 décembre 2023
author: Ouvroir
date: 2023-12-13
draft: false
tags:
    - cr

---

# Réunion hébdomadaire

## Admin

### Achats et matériel

Faire les achats tant qu'Emmanuel est là. 
- Acheter cartes sd (INSO)
- Meta Quest (sur la carte du labo)
- Cartouche (autre fournisseur qu’INSO)

Johanne va emprunter l'enregistreur cet hiver.

Planning achat : 
- William réécrit à Josianne de Trium pour obtenir l
- faire baisser prix Meta Quest? 

Régler soucis écrans Sony : 
- accéder au compte (gestion des apps)
- installer Zoom
- refaire mini formation 

Emmanuel a changé les droits de la biblio zotero de l'ouvroir a les droits pour joindre des fichiers

### Trium

Contacter Josianne, problème avec le tiroir de Katrina, ne ferme pas  : @ecd à vérifier

Clef tiroir, garder une des clefs au labo par sécurité. 

### Présence de membres au labo

Horaires de cet hiver ?

Horaires William en présentiel: 
- lundi 13-18h (1 semaine sur 2)
- mercredi 9-13h
- jeudi 16h-21h (possibilité: 9-12h + 16-18h à confirmer)

Horaires Zoë présentiel : 
- lundi toute la journée
- mardi pm
- mercredi toute la journée
(Séminaire le jeudi 14h-17h)

On garde les mercredis matin pour la réunion hebdo. 


### Veille, rencontres, collaborations

projet PerVisum : [Invisu](https://invisu.cnrs.fr/) avec l'INHA pour faire du numérique : enrichir article scientifique avec image par IIIF

collaboration possible
Web designer dans le projet: Jean Christophe Carius. Ex : Plateforme d'édition de source : [PENSE](https://pense.inha.fr/)

>"Le projet PerVisum explore les formats éditoriaux mettant l’image au cœur de la démonstration scientifique en utilisant les potentialités des technologies IIIF. Il s’inscrit dans la continuité d’activités de publication de corpus et de données menées au sein de l’Institut national d’histoire de l’art explorant les possibilités offertes par les technologies IIIF en matière éditoriale et en promouvant leur utilisation. Il s’inscrit dans l’écosystème de la science ouverte en s’appuyant sur des principes FAIR, maintenus et portés par des institutions scientifiques et culturelles.
>PerVisum se donne comme objectif de fournir un dispositif et une méthodologie éditoriale innovantes dédiées à la publication d’articles scientifiques visuels et de données structurées de commentaires de sources numérisées. Le projet articule une étude expérimentale de nouvelles formes d’éditorialisation d’articles scientifiques orientées image et la création d’un outil de génération de manifestes IIIF développé sur mesure pour permettre à un éditeur d’organiser en séquences un ensemble de visuels, d’annotations et de données, afin de composer une éditorialisation numérique visuelle d’un contenu scientifique. Par ailleurs, une attention particulière est également apportée à la diffusion et la promotion du dispositif et de la méthodologie développés afin de permettre à des communautés scientifiques étendues de pouvoir s’en emparer.
>Les résultats de cette expérimentation s’inscriront dans les flux éditoriaux de l’édition scientifique publique. Le projet s’inscrit par ailleurs dans l’offre de service proposée par les pépinières de revue et coordonné par le réseau Repères."

Envisager collaboration, Emmanuel est dans le comité de pilotage. 
- déterminer le calendrier du projet
- identifier le budget
- les acteurs

Collaboration envisageable à plusieurs niveaux.

### Reframe

Poursuite du travail sur les conteneurs pour explorer la manière dont on peut définir la taille des images. Il y a plusieurs difficultés concernant la réalisation de cette tâche. D’une part les images ont des ratios variables, il n’est donc pas seulement possible de confier au navigateur le soin de régler la question. Quelle stratégie utiliser pour définir les dimensions des images. Déclinaison avec les légendes : au survol ou en dessous.

Pour pouvoir appliquer des contraintes sur les dimensions de l’image, il serait plutôt nécessaire de sortir les légendes du container. Se pose la question de savoir comment on redéfinit la taille de l’image pour régler les problèmes de hauteur des images.

C’est en réalité au container de dire quelle doit être la taille des images. Une approche qui est plutôt différente de la stratégie habituelle du web. Impliquerait de définir la zone générale. Faut-il que CSS fasse tout, et limiter JavaScript à la mise en place des composants. Ou bien JavaScript vient-il styliser les données ?

Une complexité qui laisse penser que le ratio de l’image détermine l’espace dont on a besoin.

Autre essai pour repenser le problème en partant du CSS. N’arrive pas à trouver de solutions pour définir des tailles égales aux images. L’idée est que les composants puissent fonctionner sur plusieurs formats d’écrans. Cad qu’ils soient responsive et qu’ils se déclinent. Or, plus on applique de contraintes à la grille, moins il y a de déclaration. L’idée est donc être le moins spécifique possible. En n’utilisant pas de ratio et en essayant de faire en sorte que les légendes ne soient pas dans le même container. Mais ne trouve pas d’autres solutions que l’utilisation du ratio pour définir la taille naturelle des images.

On pourrait également avoir une liste de trois images, et extraire les images et les légendes, et raisonner pour la construction de l’affichage. 

Avoir une image comme composant de base avec ses attributs : légendes, container, etc.

Pour l'implémentation d'image : spécifier dans le cahier des charges comment on souhaite que ça fonctionne et nous n'avons pas de solution OU trouver solution qui fonctionne à proposer au développeur.

William a commencé le cahier des charges. 
Session de travail workshop programmée le 23 décembre 10h-16h. 

MAJ calendrier du projet à faire en fonction des nouvelles en janvier. 

Développeur quebecois envisageable : Principle


### Display

Zr sur dossier cahier des charges Display. 

## Réunion d'équipe

### Présentation Jean François Palomino
Jean François Palomino, historien sur géographie historique et a été bibliothécaire (BanQ notamment)
à l'UQAM au département d'histoire
impliqué dans le projet [Nouvelle france numérique](https://nouvellefrancenumerique.info) 

Éloigné des musées mais travail tout de même avec le quai Branly sur la cartographie de la Louisianne. 

Nouvelle France, histoire du Canada
Aspect très fort géographie et cartographie, thèse portée sur la circulation des savoirs géographiques entre le Canada et la France 
Cartothécaire de métier, notamment à la BanQ

#### Deux projets en HN a la BanQ, orientés bibliothéconomie 

Comment rendre plus efficace de sources icono urbaines ? 
- solution comme cartothécaire :  géolocaliser les documents, solution utile et intuitive pour la majorité des chercheurs et chercheuses
- application de géolocalisation. Gallica : géolocalisation du terme. (ce que voulait la BAnq mais pas eu le temps avant de partir)
A terme, souhaiter pour BanQ numérique, mais parti

Pb, question de la carence des données géographiques fines. 

Dans les protocoles de géographie, dans les cartes géographiques :
[historypin](https://www.historypin.org/en/)
passer par historypin, plusieurs collections et travail sur l'icononographie pour régler ce problème de carence 
Volonté à terme de récupérer les métadonnées pour la BanQ

##### [Collection d'albums de rues Massicotte](https://lhpm.uqam.ca/programmation-scientifique/humanites-numeriques/geolocaliser-les-images-des-albums-de-rues-massicotte/)
Edouard-Zotique Massicotte (1867-1947)
appel à la plateforme [Schema](https://lhpm.uqam.ca/programmation-scientifique/humanites-numeriques/systeme-de-cartographie-de-lhistoire-de-montreal-schema/) pour travailler sur son corpus d'images. 
Collection de milliers d'images de Mtl, plus de 6000 images. 
Albums spicilèges classés par nom de rue
Maintenant conservés aux Archives nationales à Mtl 
par exemple : coupures de presse, photographies originales et non-originales, cartes postales 

Certaines personnes avaient une mauvaise perception de cette collection car sources hétérogènes

Il voulait documenter l'aspect physique de mtrl qui allait disparaître. 

Images annotées (altérées)
En plus du nom de rue il y a aussi l'adresse 
Interface avec Schema de géolocalisation des images de la collection 

Tant qu'à refaire travail de géolocalisation autant faire Correction des métadonnées 

Ajouter public : dispendieux. 
Travail avec des étudiants 

Début travail avec GoogleSheet, Excel puis extraction du catalogue.
Les coordonnées sont un point, comme un point du bâtiment. Si trop grand : favoriser le point de vue du spectateur. 

Ont réussi à noté le degré d'incertitude. 

Ensuite, intégration sur la plateforme Schema, de plans anciens

Ont utilisé une mosaïque de plans anciens très précis pas google maps.
1870-1970

Validation avec les collègues archivistes, pour ensuite à terme reverser les métadonnées à la BanQ

Recherche par rue, thématiques, etc. 

[Interface pro et public](https://numerique.banq.qc.ca/p/cartographie_massicotte.html) sur https://www.mapgears.com/fr/



##### Georeference les plans d'assurance incendie 
- carte index 

Projets de recherche actuels 
- Histoire environnementale de la Nouvelle France et cartographie des territoires autochtones du Canada, e l'Acadie et de la Louisane 1603-1763, avec le Quai Branly
Autochtones qui veulent en savoir plus sur leur territoire. Documentation par le quai Branly puis peut-être en faire une exposition 
- Toponymes de la NF une étude de cas en HN spécialisées
CRIHN ?
- Colonisation et portée géographique du pouvoir colonial 
CRIHN ?
- Naviguer, décrire, et cartographier le fleuve St-Laurent au XVIIIeme ; les savoirs locaux au service des empires
Beaucoup de cartes au 17e 18e


**Toponymes de la NF une étude de cas en HN specialisées**
consigne des toponymes sur les cartes géographiques. Voulait savoir qui a copié qui ? 

existence de bases de données de toponymes anciens 
Mais pas aspect historiques

Pourquoi étudier la toponymie 
- se renseigner sur les origines et l'évolution des noms, leur usage, leur signification et l'histoire d'un territoire à l'échelle locale 
- documenter environnement physique dans lesquels s'inscrivent les populations autochtones

Objectifs de la recherche 
- mieux évaluer de façon globale le degré de connaissances géo et la fluide de la circulation de savoirs 

Classeur avec plusieurs feuilles :
une ligne par toponyme et une colonne par document dépouillé/lu
Comment dépouiller de façon systématique ? 
Méthode peaufinée au fil des années :
suivre les cours d'eaux  pour ne pas oublier de toponymes sur les cartes
Enrichissement progressif : coordonnées géo si possibles (recherches sur d'autres bds, liens vers d'autres répertoires géo (Wikidata, Geonames ?)
distinguer types d'entités topographiques, variantes (6/7 noms différents pour un même lieu ?), nombre d’occurrences, ID unique, langue autochtone si connue, traduction française + provenance de la source 

19241 nombres d'occurrence. Fait à la mitaine.

Corpus (2eme phase) dans transcribus. 

Beaucoup de rivières, îles, lacs etc. 
toponymes ou ethnonymes autochtones 
Description aussi du portage

toponymes à partir de la faune nord-américaine. 
Noms identiques ?

comment consigner les marques d'une disparition ? 
comment consigner les mentions ? Témoignes d'une appréciation du territoire. 

Méthode d'extraction : artisanal vs OCR/HTR
[David Rumsey](https://www.davidrumsey.com/) map collection le fait depuis quelques mois. 
Le projet living with machine malheureusement plus financé. 
On peut corriger soi-même ce que la machine a lu. 

Outils à examiner pour faire cette manipulation : 
MapKurator vs Transkribus
OpenSeaDragon
Luna
Annotorious
Protocole IIIF
Recogito
World Historical Gazetteer voir la liste des jeux de données dans la liste. 

Questions : 
Comment avez vous noté les sources des infos commentés ? Infos liées aux cartes étudiées donc on sait quelle localisation est sur quelle carte.

Comment avez-vous géré l'incertitude ?
il ne sait pas comment faire. Groupe de recherche à Poitier sur l'incertitude dans la géo: ICAR
Aller voir l'incertitude temporelle