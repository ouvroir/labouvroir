---
title : CR réunion labo
author: ouvroir
date: 2023-02-21
draft: false
tags:
    - cr
    
---

## Admin

### organisation

Lena peut envoyer la lettre.
ECD est là entre 10 avril et début Mai. 

### Francis Lavigne

responsable du laboratoire de jeu vidéo au département. quelques questionnements à propos de deux principaux trucs au labo en ce moment. 

1) J'avais commencé avec Emmanuel à évaluer les possibilités pour faire fonctionner des logiciels de musées sur CD-ROM. On a commencé à partager des ressources, mais j'aimerais pouvoir en discuter de vive voix avec vous si cela est possible (et si vous êtes bien les bonnes personnes à l'Ouvroir pour ce projet);
2) Je travaille présentement avec Valérie Rioux pour changer notre logiciel et méthode de catalogage des oeuvres. Je voulais savoir s'il y a un potentiel de partenariat à ce niveau.

De manière plus générale, je me demandais si vous les membres du laboratoire seriez ouverts à une rencontre au labo de jeu pour échanger sur nos sujets de recherche respectifs.
 
idée de travailler sur les CD ROMS artistiques
orga atelier pour présenter ces cd-roms. 
Attendre le retour d'ecd pour organiser ca : Au mois d'avril? 
Si on organise quelque chose au mois d'avril : reu zoom avant. Mais si on peut se rencontrer en avril c'est mieux. 

Répondre en disant qu'on est intéressés, on pourrait faire quelque chose en avril (quand emmanuel sera là: entre le 10 et la fin du mois d'avril), mettre Emmanuel en cc.

### Display

Retour constructif de David sur le cahier des charges.
Réunion avec David le 28 de 9h à 11h.

Tentative de schéma avec ViewSonic nous a fait réalisé qu'on n'avait pas la même vision pour l'outil. Zoë a développé sa vision dans le [MIRO](
https://miro.com/app/board/uXjVNzCVdjo=/). En parler pour voir si c'est ce qu'on attend

### Common

Josselin, communiqué le CCP. Rencontre bientôt pour chiffrer et plannifier le travail.

Validation avec Johanne sur le principe de valider nos besoins et aller de l'avant. Elle a commencé à parler de common à d'autre partenaires.

Nada documente des projets de mobilisation des collections autour de questions identitaires et de diversité. Répertoire d'initiatives muséales dans le domaine. Se traite peut-être d'avantage avec Zotero? Pas nécessairement l'application la plus directe de common. Voudrait surtout avoir des données de recherche à présenter pour l'évaluation du projet à l'automne 2024.
Emmanuel l'a rassurée que l'axe 4 a aussi des données à présenter, comme la bilbiographie de la 3D dans les musées par exemple.

### Reframe

Analyse des sites web: établir une grille de lecture. Faut-il étendre ou non la liste à d'autres types de sites web? Traiter uniquement d'expositions numériques ou plutôt d'aller traiter des publications savantes plus élargies (sans savoir exactement comment délimiter)

La question est qu'est-ce qu'il y a réellement à traiter? Ont posé des notions qui permettent de décrire beaucoup de choses qu'essaient de faire reframe. Composants: layouts.

Deux questions: 
- interactions avec ces layouts: une fois qu'on a une grille sur une page, qu'est-ce qu'on peut faire avec? 
- est-ce qu'un composant, quand il se dégrade, devient un autre composant? Et est-ce que c'est prédéterminé à l'avance? Une grille qui deviendrait une pile d'images, ou une liste. Si la galerie sert à la navigation, est-ce qu'avec une dégradation, il y a encore une navigation. 


Les dégradations viennent après. D'abord définir les types, ensuite déterminer la dégradation pour définir la substance du type. La question du panorama est intéressante mais doit arriver en second lieu. 

Périmètre: les expositions numériques avec la désignation exposition est un peu pauvre et répétitive.Emmanuel pense au web documentaire mais peut-être ailleurs aussi.

Zoë a bien fouillé la question de l'image et son rapport au contexte. Il reste la question du légendage, des séquençage entre image et texte. Sur les interactions, il manque peut-être les processus de parallax: comment se comporte la lecture dans le contexte du navigateur (navigation verticale intercalée avec horizontale, effets parallax). Souvent les expos numériques des musées utilisent le feuilletage comme processus. Permet de marquer les sections et structurer le propros dans des chapitres (identifier des éléments de chapitrage).

Chercher ailleurs : web documentaire

parallax : type d'interaction de lecture
Parallax scrolling websites play with space and depth, yet technically speaking this design technique is actually a lot simpler than it may seem. Most parallax scrolling websites simply move content in the foreground at a faster rate than content in the background. Through this juxtaposition of movement, parallax scrolling websites create the illusion of three-dimensional space.

[recherches Zoë](https://docs.google.com/presentation/d/1ZbWHkWfATxSfg0qFvZl099_Yy5nxdOPUkCw2Ne28ElA/edit#slide=id.p)
Ajouter le comportement des légendes. Et les comportements de navigation. 

Surtout essayé d’explorer des cas de figure qui poseraient des difficultés de réalisation ou seraient intéressants en terme de description des composants.

[Zotero](http://zotero.org/groups/2480242/collections/I26IMN33)

Est-ce que reframe, plutot que d'être juste une librairie de composants javascripts, serait aussi un modèle de description de contenu (un peu comme l'API présentation de IIIF? ) Peut-être représenter, de manière formelle, une exposition numérique? 

Les termes qu'on emploie en travaillant sur reframe : est-ce qu'une chose est une interaction, un layout ou autre chose? Complexité d'aller modéliser ça. Certaines instances où la définition est cruciale

En pensant au cahier des charges de common, William a commencé lundi un benchmark des viewers IIIF, les librairies JS de composants d'image. A peur de s'embourber là-dedans. À quel point en a-t-on besoin? 
Entre les stagiaires et le projet Righettino, un benchmark peut servir à se rafraichir les idées mais prend du temps sans réellement avoir l'impression d'avancer. 
On n'est pas obligés d'avoir un benchmark : l'intérêt serait surtout d'identifier ce que les produits actuels ne font pas. 

Valdier les idées en regardant les outils qu'on connait déjà mais aussi ceux qui viennent d'être développés. On ne veut pas donner une liste exhaustive des outils IIIF/JS qui existent déjà

Pour revenir à l'idée d'une spécification qui serait comme un modèle de description. Souvent les librairies JavaScript sont définies par des APIs qui déterminent la manière dont on interagit avec les ressources. Dans IIIF,  l’API présentation définit un modèle très abstrait et très générique dans lequel on se contente de définir l’expo comme séquence de canvas avec annotations. L’idée serait d’être plus spécifique sur ce que sont les types de composants d'une expositions, comment ils sont liés entre eux et comment ils doivent se dégrader de manière responsive.

Où intervient le modèle? 
1. Penser à la possibilité de l'obsolescence technologique de reframe, en ce cas, l'intérêt serait le modèle de description qui pourrait y survivre.
2. Question de l'interfaçage avec les composants: où est-ce qu'on paramètre son modèle? sachant qu'on fait des web components, est-ce qu'on utilise à 100% le web component (custom tags reframe dans une page HTML, construire les composants à partir des attributs HTML) ou est-ce que, dans le style de Observable et la libraire Plot: décrire les objets grâce à un modèle (ex JSON) ? ← cet aspect concerne d'avantage l'implémentation
3. logique de conception de la libraire: point de vue sur la librairie et sur les données. 

Emmanuel ne veut pas que l'utilisateur ait à se plier à un ordre de définition de contenus pour pouvoir le créer. C'est une décision qu'on aura en aval.
Il faut définir le vocabulaire, l'idéologie et le point de vue sur le sujet. Les paramètres et variables de composants doivent être compréhensibles. Cela va probablement définir une grosse partie de l'API.

Nécessite des réunions de travail collectives?
Il faut discuter de définitions, William a besoin d'en parler en continu pour avancer à sur le CDC. Une réunion pour penser un modèle formel ce serait autre chose. Pas besoin d'être aussi drastique d'une ontologie, le besoin est d'avantage descriptif: quels sont les objets et leurs définitions? Quel statut, quelles conséquences en matière de design?

Continuer à regarder des exemples avec Zoë
- vocabulaire qui se développe à partir des exemples → ferait commencer à émerger les bases d'un modèle



### écran View Sonic
les questions de connexion d'écran sont réglées normalement.

on ne peut pas se connecter sans fil pour prendre contrôle de l'écran
besoin de [Thierry](thierry.maxime@viewsonic.com) (ViewSonic) pour créer un identifiant

## Club de lecture
Tabea Thietz, Junior Researcher at FIZ Karlsruhe – Leibniz Institute for Information Infrastructure, Germany https://www.fiz-karlsruhe.de/en/ueber-uns/ueber-uns

Oleksandra Bruns
PhD student/Junior Researcher, FIZ Karlsruhe – Leibniz Institute for Information Infrastructure and Karlsruhe Institute of Technology (KIT), Institute of Applied Informatics and Formal Description Methods (AIFB)
O. Bruns “The Persistence of Temporality: Tracing Time in Cultural Heritage Knowledge Graphs”, Proc. Of the 22nd International Semantic Web Conference, ISWC 2023, Doctoral Consortium, Springer (to be published)

Harald Sack: spécialiste adulé du web sémantique, a formé beaucoup de gens avec son cours en ligne.

Intérêt pour l'article: 
- recherche de Camille
- Comment est-ce qu'on écrit sur un modèle? (pour Display)

Question du minima: penser l'ontologie en pensant aux requêtes pour qu'elle soit utilisable. Camille avait jusqu'à présent omis cette question. 

La performance des requêtes est (juste?) un enjeu d'optimisation. 

Requirements: très larges, utiles pour avoir un cadre. Plan de travail. Transaction entre demandeurs et équipe de recherche s'énonce dans ces requirements.

Les choix dans la modélisation à faire est un étape importante de ce genre de travail. 
David a développé un modèle pour décrire des bâtiments historiques diparus à Montréal. A pris l'axe de tout décrire au plus fin, complexifie le modèle et les requêtes, requiert d'imbriquer les choses.
Il le dise dans le Requirement 8 : cible simple. 

Mapping pour repasser du modele simplifié au modèle complexe? 

Question de la simplification, noeuds vides.
Stratégie de minimiser les précisions et doubler les relations. 

Ne parle pas de LRM (n'est pas fini)

SPA : https://www.bfh.ch/dam/jcr:78a5e853-3c03-4ed8-8e28-86e2791a5829/SPA_Data_Model_v0-51_20170926.pdf

https://github.com/ISE-FIZKarlsruhe/LinkedStageGraph

Point de départ: un jeu de données mal structuré, avec plein d'ambiguités. 

https://slod.fiz-karlsruhe.de/vikus/ pas Rdf juste visualisation. 

Parle du projet : https://slod.fiz-karlsruhe.de/about


Si on souhaite poursuivre dans l’analyse de modèle sémantique :

Guillem, Anais, George Bruseker, and Paola Ronzino. 2017. “Process, Concept or Thing? Some Initial Considerations in the Ontological Modelling of Architecture.” International Journal on Digital Libraries 18 (4): 289–99. doi:10.1007/s00799-016-0188-0. 
- où intervient la documentation dans le modèle? outre la représentation de l'objet (archi, perf, ...)

Camille va proposer la modélisation d'une perf au labo. David peut aussi nous présenter son boulot. Organiser session de comparaison de modèle, peut-être le 20 mars