---
title: collaboratoires2024-01
description: emchateau UdeM
theme: presentation/theme/remark-dark-em.css
name: inverse
layout: true
class: inverse

---

name: index

class: center middle

# Le cadre international d’interopérabilité des images (IIIF) pour la valorisation des collections muséales

### Partenariat *Des nouveaux usages des collections dans les musées d’art,* Collaboratoire du 8 mars 2024

---

class: center middle

# Introduction

???

Présentation des collaboratoires

Comme l’année dernière, le Partenariat *Des nouveaux usages des collections dans les musées d’art* organise une série de collaboratoires dans le cadre de son axe 4, « la collection partagée ». Ces ateliers collaboratifs avec les professionnel·le·s des musées en charge du numérique parmi les musées partenaires, sont destinés à mutualiser les expériences et développer des compétences autour de problématiques numériques. Conçues comme des lieux d’échange et d’expérimentation, ces rencontres débouchent sur la rédaction de tutoriaux et de guides de bonnes pratiques sur la promotion et la diffusion des contenus et des données libres et ouverts.

L’année précédente ces collaboratoires étaient consacrés aux portraits statistiques des collections. Un court document de synthèse est en cours de préparation. Nous proposons pour 2024 de nous intéresser particulièrement au protocole d’interopérabilité des images IIIF. Quatre collaboratoires se dérouleront de mars à juin 2024. Il s’ s’agira d’aller ensemble à la découverte de ce protocole encore peu connu au Québec et au Canada et de son potentiel pour les musées et la valorisation de leurs collections.

---

layout: false

## Programme des rencontres

- .red[8 mars 2024] – Séance 1 : Le protocole d’interopérabilité des images IIIF
- .red[26 avril 2024] – Séance 2 : Première exploration de l’API Présentation et cas d’application
- .red[24 mai 2024] – Séance 3 : IIIF et Digital storytelling
- .red[7 juin 2024] – Séance 4 : Déploiement dans les musées québécois : freins et opportunités

???

Collaboratoire 1 : Le protocole d’interopérabilité des images IIIF

- Présentation générale du protocole
- Exemples paradigmatiques
- Première approche des APIs
- Un panorama sur les outils disponibles

Collaboratoire 2 : Première exploration de l’API Présentation et cas d’application

- L’API Présentation et les manifestes (EC)
- Retours d’expérience sur Righettino et le travail en cours au Labo (WD)
- Demo : Exploration de plusieurs outils (1 ou 2 outils faciles de prise en main)

Collaboratoire 3 : IIIF et Digital storytelling

- Exemples d’utilisation pour le storytelling numérique
- Annotation
- Régis Robineau ? Delft ?

Collaboratoire 4 : Déploiement dans les musées québécois : freins et opportunités

- 3D, Vidéo, API Authentification
- Martin Sevigny
- Discussion sur l’implémentation au Québec
- Synthèse

---

## Présentations et tour de table

--

## Pad collaboratif

https://demo.hedgedoc.org/s8du5-K6St2rVjE9qune-Q

---

background-image: url(imagesMSL/Logo_Stacked.png)

# Le cadre international d’interopérabilité des images (IIIF)

*IIIF, prononcer « triple-EYE-eff »*

.footnote[https://iiif.io/demos/]

???

*L’International Image Interoperability Framework* (IIIF) réunit un ensemble de normes techniques qui facilitent la publication de contenus patrimoniaux sur le web en s’appuyant sur des outils standardisés. Adopté par de nombreuses institutions patrimoniales à travers le monde, ce protocole est encore peu mobilisé au Canada et au Québec. Les collaboratoires du partenariat *Des nouveaux usages des collections dans les musées d’art* seront consacrés en 2024 à l’exploration des riches possibilités offertes par ce protocole d’interopérabilité pour la valorisation et l’éditorialisation des collections d’art. À travers quatre séances collaboratives, les principes généraux du protocole, ses différentes briques technologiques, et de nombreux exemples d’application dans le secteur muséal seront présentés ainsi que des logiciels libres et facilement utilisables pour démontrer l’intérêt de IIIF et favoriser son adoption parmi les musées partenaires.

IIIF est un ensemble de normes ouvertes permettant de fournir des objets numériques de haute qualité ainsi que leur attribution à grande échelle. C’est aussi une communauté internationale qui développe et met en œuvre les API de IIIF. IIIF est soutenu par un consortium d’institutions culturelles de premier plan.

Ces normes et standards sont destinés à assurer :

- une interopérabilité des images
- la création de standards pour diffuser les images
- le développements d’outils basés sur ces standards (serveurs d’images, visionneuses, outils d’annotation, création d’expositions numériques)

IIIF propose des modèles pour présenter et annoter des contenus numériques (images et fichiers audiovisuels), mais c’est aussi une communauté qui développe des APIs ouvertes et implémente des outils qui consomment ces APIs sur le web. Une communauté vivante et dynamique. 

---

## Bénéfices de l’utilisation de IIIF

- Accélérer le développement de sites web en utilisant des outils basés sur des standards
- Accroître la flexibilité de la présentation des images
- Proposer les images en haute résolution de façon enrichie
- Faciliter la citation et le partage de contenus numériques
- Résoudre des problèmes communs

???

Plusieurs musées importants ont depuis quelques années commencé à implémenter la spécification IIIF pour leurs ressources en ligne parmi lesquels : la U.S. National Gallery of Art, le J. Paul Getty Trust, le Yale Center for British Art, l’Art Institute of Chicago, l’Art Gallery of Ontario, le Harvard Art Museums, le Carnegie Museum of Art, le Paul Mellon Center, The Frick Collection. IIIF est aujourd’hui un composant stable et important de la mise à disposition des ressources numériques dans le secteur patrimonial et culturel.

Typiquement le recours aux technologies IIIF permet au producteur de données de diffuser des images en permettant aux utilisateurs d’afficher et de manipuler des contenus audiovisuels et leur description dans une même visionneuse à partir d’URI. Les utilisateurs peuvent créer des collections d’images ou de contenus issus de différentes sources, zoomer, comparer ou encore annoter tout ou une partie de ces images afin de créer de nouveaux documents ou corpus de recherche à différentes fins (publications savantes numériques, expositions virtuelles, outils de médiation...).

Les bénéfices associés à l’utilisation de IIIF sont nombreux. Pour les musées, ils permettent notamment :

- D’accélérer le développement de sites web en utilisant des outils basés sur des standards. Les visionneuses IIIF proposent de nombreuses fonctionnalités pour la visualisation de contenus qui faciliternt la publication et le partage de contenus audiovisuls

- Accroître la flexibilité de la présentation des images
  Facilement ajouter de nouvelles fonctionnalités. Réutilisation possibles dans des contextes d’exposition, etc.
- Proposer les images en haute résolution de façon enrichie
  Ajouts dynamiques : deep zoom, comparaison d’image côté à côte, changement des paramètres de visualisations, etc.
- Faciliter la citation et le partage de contenus numériques
  Les collections d’images ou des portions d’image deviennent citable pour un usage amateur ou académique.
- Résoudre des problèmes communs en bénéficiant de développements partagés
  Communauté de développeurs logiciels actifs qui développent de nouvelles fonctionnalités

---

## Historique de l’International Image Interoperability Framework (IIIF)

- .red[2010] – Plusieurs efforts pour poser les bases d’un cadre de travail pour l’interopérabilité des images
- .red[2011] – Création de l’International Image Interoperability Framework” (**IIIF**) par Stanford University
- .red[2012] – Création de Groupes Google IIIF et premières rencontres
- .red[2015] création du Consortium IIIF

???

*L’International Image Interoperability Framework* (IIIF) propose un modèle pour la publication de contenus numériques (images et fichiers audiovisuels).

Principalement conçu à destination des institutions patrimoniales et culturelles il rassemble une large communauté d’utilisateurs et de développeurs autour de la mise au point de standards et d’outils logiciels.

L’initiative lancée autour de 2011 rassemble aujourd’hui plus d’une centaine d’utilisateurs à travers le monde qui sont issus du monde des bibliothèques, des archives, des musées, mais aussi des agrégateurs de contenus ou d’autres utilisateurs. 

---

## Le Consortium IIIF

10 membres en 2015, aujourd’hui 67 membres, réunis autour d’objectifs partagés :

- fournir aux chercheurs un accès riche et uniforme aux images, sons et ressources vidéos numérisées à travers le monde
- définir et maintenir de manière communautaire un ensemble d’API supportant l’interopérabilité entre des entrepôts
- développer, cultiver et documenter des technologiqes partagées pour offrir une expérience utilisateur de haute qualité pour la visualisation, la comparaison, la manipulation et l’annotation d’images et de contenus audiovisuels numérisés

https://iiif.io/community/consortium/

???

Le Consortium IIIF (*IIIF Consortium* ou IIIF-C) créé en 2015 autour d’une dizaine de membres principalement issus du monde des bibliothèques réunis aujourd’hui 67 membres incluant des musées, des archives et des sociétés de design web ou des services d’images qui offre de nombreuses opportunités d’échanges et de collaboration.

Membres fondateurs : 

- Oxford University
- Stanford University
- Die Bayerische Staatsbibliothek
- Cornell University
- The National Library of Norway
- Artstor
- La Bibliothèque nationale de France
- The British Library
- Princeton University
- The Wellcome Trust
- Yale University

Rassemble aujourd’hui 67 membres, signataire du *Memorandum of Understanding* autour d’objectifs partagés

- fournir aux chercheurs un accès riche et uniforme aux images, sons et ressources vidéos numérisées à travers le monde
- définir et maintenir de manière communautaire un ensemble d’API supportant l’interopérabilité entre des entrepôts
- développer, cultiver et documenter des technologiqes partagées pour offrir une expérience utilisateur de haute qualité pour la visualisation, la comparaison, la manipulation et l’annotation d’images et de contenus audiovisuels numérisés

Le consortium est gouverné par trois comités

- Comité exécutif
- Comité d’opération
- Comité de révision technique 

https://iiif.io/community/consortium/

---

## Une organisation communautaire

### Community Groups

- 3D
- Archives
- Intelligence artificielle
- Musées
- ...

### Technical Specification Groups (TSGs)

- 3D TSG
- Maps TSG
- Authorization Flow
- Content Search

https://iiif.io/community/groups/

### Community call calendar

https://calendar.google.com/calendar/ical/1hnm5h86n94ore0vnoo188ter8%40group.calendar.google.com/public/basic.ics

???

IIIF est principalement organisé en groupes communautaires ouverts à tous rassemblés autour de domaines d’application ainsi que de groupes de spécification technique spécialement chargé de mettre à jour les spécifications. 

https://iiif.io/community/groups/

---

## Memorandum of Understanding

« Enabling Richer Access to the World’s Images »

https://iiif.io/community/consortium/mou/

### Exemples de ressources

- [Awesome IIIF](https://github.com/IIIF/awesome-iiif)
- [Ouvroir, répertoire de ressources IIIF](https://github.com/ouvroir/labouvroir/blob/main/ressources/iiifResources.yml)

???

La vision de IIIF « Enabling Richer Access to the World’s Images »

créer un framework global dans lequel les ressources visuelles ou temporelles peuvent être partagées sur le web...

Dispositif fondé sur la définition d’Interfaces programmables qui encourage le développement de logiciels.

L’initiative vise notamment à résoudre le problème de silos, où les données sont réparties entre des institutions séparées sans qu’il soit possible de partager facilement ces contenus en raison de barière technologique. IIIF souhaite faire advenir un réseau de partage basés sur des APIs. Remote environnement... third party application annotation, outil de présentation, gestionnaire de contenu pour proposer de riches interactions distribuées avec des contenus visuels, offrir un cadre de travail avec les images qui permette leur citation, leur recadrage ou leur annotation, et proposer des expositions numériques.

Exemples de ressources

- [Awesome IIIF](https://github.com/IIIF/awesome-iiif)
- [Ouvroir, répertoire de ressources IIIF](https://github.com/ouvroir/labouvroir/blob/main/ressources/iiifResources.yml)

---

name: exemples

class: inverse center middle

# Exemples paradigmatiques

???

Camille 20 min

---

name: api

class: inverse center middle

# Les APIs IIIF

???

20 min

---

## Une modélisation fondée sur des standards

Le cadre de travail pour l’interopérabilité des images repose sur la définition de standard techniques qui encouragent le développement de logiciels.

Une **API** (*application programming interface* ou « interface de programmation d’application ») consiste en un ensemble de définitions et de protocoles qui facilitent la création et l’intégration des applications. Une API permet souvent de « connecter » un logiciel ou un service à un autre logiciel ou service afin d’échanger des données et des fonctionnalités.

- définition du service
- définition des points d’accès
- définition des comportements attendus
- modèle de données

---

## Les APIs IIIF

#### [Image API](https://iiif.io/api/image/)

> L’API Image IIIF spécifie un service web qui renvoie une image en réponse à une requête HTTP(S) standard. L’URI peut spécifier la région, la taille, la rotation, les caractéristiques de qualité et le format de l’image demandée.

#### [Presentation API](https://iiif.io/api/presentation/)

> L’API de présentation IIIF fournit les informations nécessaires pour créer de riches environnements de visualisation en ligne pour les objets numériques composés destinés à être présentés à un utilisateur humain, souvent en conjonction avec l’API d’image IIIF.

#### [Authentication API](https://iiif.io/api/auth/)

> La spécification d’authentification IIIF décrit un ensemble de flux de travail pour guider l’utilisateur à travers un système de contrôle d’accès existant.

---

## Les APIs IIIF (suite)

#### [Change Discovery API](https://iiif.io/api/discovery/)

> L’API Change Discovery de IIIF fournit les informations nécessaires pour découvrir et utiliser les ressources IIIF.

#### [Content Search API](https://iiif.io/api/search/)

> La spécification de l’API de recherche de contenu IIIF définit le mécanisme d’interopérabilité pour effectuer des recherches d’annotations textuelles associées à un objet dans le contexte IIIF.

#### [Content State API](https://iiif.io/api/content-state/)

> L’API IIIF Content State fournit un moyen de se référer à une ressource de l’API IIIF Presentation, ou à une partie d’une ressource, dans un format compact qui peut être utilisé pour initialiser la vue de cette ressource dans n’importe quel client.

---

## Modèle de mise à disposition des contenus

<img src="https://iiif.io/assets/images/zeplin/delivery@3x.png" width="800">



---

## L’API Image et l’API Présentation

<img src="https://training.iiif.io/iiif-online-workshop/day-one/img/apis.png" width="800">

???

Afin de mieux comprendre comment fonctionne IIIF, nous vous proposons pour commencer de nous intéresser aux deux seules API Image et API Présentation.

L’API Image permet d’obtenir des pixels via un service REST. Tandis que l’API de présentation permet de fournir les métadonnées nécessaires pour proposer une expérience de visionnement.

Les manifeste IIIF et les listes d’annotations définies par l’API de présentation permettent de décrire une collection d’images ou de canvas comme un ensemble ainsi que de référencer des régions particulières d’une image en fournissant des informations complémentaires.

--> Permet la mise en place d’une véritable narration numérique[^1]

---

## L’API Image

[Image API](https://iiif.io/api/image/)

> L’API Image IIIF spécifie un service web qui renvoie une image en réponse à une requête HTTP(S) standard. L’URI peut spécifier la région, la taille, la rotation, les caractéristiques de qualité et le format de l’image demandée.

???

[Image API](https://iiif.io/api/image/)

> L’API Image IIIF spécifie un service web qui renvoie une image en réponse à une requête HTTP(S) standard. L’URI peut spécifier la région, la taille, la rotation, les caractéristiques de qualité et le format de l’image demandée.

Consulter la page de l’API et présenter la structure de la norme

- version, éditeur cf. standards du W3C ou normes professionnelles
- objet de la norme
- Audience
- présentation du schème d’URI

---

## L’API Image

![image](https://iiif.io/api/image/1.0/images/iiif-order.png)

???

L’API image définit comment un serveur d’images délivre les pixels d’une image à une visionneuse. À l’aide de paramètres insérés dans l’URL de l’image, il est possible de renvoyer une image de pleine-taille, ou de plus petite taille, ainsi qu’une portion recardée ou encore une rotation. Il est également possible de récupérer différentes qualités d’images.

---

## Informations sur une image

### Paramètres

#### Informations sur une image

```
{scheme}://{server}{/prefix}/{identifier}/info.json
```

#### Syntaxe des paramètres

```
{scheme}://{server}{/prefix}/{identifier}/{region}/{size}/{rotation}/{quality}.{format}
```

---

## Région

region=full

<img src="https://iiif.io/api/image/3.0/img/full.png" width="500">

```
.../full/max/0/default.jpg
```

---

## Région

region=125,15,120,140

<img src="https://iiif.io/api/image/3.0/img/region_px.png" width="500">

```
.../125,15,120,140/max/0/default.jpg
```

---

## Rotation

rotation=22.5

<img src="https://iiif.io/api/image/3.0/img/rotate_22-5.png" width="400">

```
.../full/max/22.5/default.png
```

---

## Ordre des paramètres

```
Region THEN Size THEN Rotation THEN Quality THEN Format
```

region=125,15,120,140 size=90, rotation=!345 quality=gray

<img src="https://iiif.io/api/image/3.0/img/transformation.png" width="500">

```
.../125,15,120,140/90,/!345/gray.jpg
```

---

## Informations sur une image

```
{scheme}://{server}{/prefix}/{identifier}/info.json
```

Réponse en JSONLD

```
Content-Type: 
	application/ld+json;profile="http://iiif.io/api/image/3/context.json"
```

exemple : https://iiif.io/api/image/3/context.json

---

## Ex. Image API playground

https://www.learniiif.org/image-api/playground

Exemples d’URL (API Image 2.1) :

- https://api.digitale-sammlungen.de/iiif/image/v2/bsb00021200_00038/full/562,800/0/default.jpg (image entière, retaillée à 562x800 pixels)
- https://api.digitale-sammlungen.de/iiif/image/v2/bsb00021200_00038/654,2223,2996,2200/800,/0/default.jpg (région d’intérêt au sein de l’image, retaillée à 800 pixels de largeur)
- https://api.digitale-sammlungen.de/iiif/image/v2/bsb00021200_00038/654,2223,2996,2200/600,/!0/gray.png (région d’intérêt retaillée à 600 pixels de largeur, retournée sur l’axe vertical, passée en niveau de gris et au format PNG)

---

## Ex. Requête d’informations sur une image

- https://iiif.library.ucla.edu/iiif/2/ark%3A%2F21198%2Fzz00090nmj/info.json (API Image 2.1)
- https://iiif.io/api/image/3.0/example/reference/59d09e6773341f28ea166e9f3c1e674f-gallica_ark_12148_bpt6k1526005v_f19/info.json (API Image 3.0)

---

## L’API Présentation

> L’API de présentation IIIF fournit les informations nécessaires pour créer de riches environnements de visualisation en ligne pour les objets numériques composés destinés à être présentés à un utilisateur humain, souvent en conjonction avec l’API d’image IIIF.

???

[Presentation API](https://iiif.io/api/presentation/)

> L’API de présentation IIIF fournit les informations nécessaires pour créer de riches environnements de visualisation en ligne pour les objets numériques composés destinés à être présentés à un utilisateur humain, souvent en conjonction avec l’API d’image IIIF.

L’API Présentation permet d’attacher des métadonnées de base et des informations sur la structure des objets numériques en définissant la manière dont ceux-ci doivent apparaître dans les visionneuses.

Ces informations sont fournies dans un *Manifeste* qui consiste en un fichier JSON qui détaille toutes les informations de l’objet IIIF (image simple, série d’images), leurs méétadonnées (titres, description, informations sur les droits), et des informations structurelles (comme l’ordre des pages).

---

## Composantes d’un fichier manifeste

<img src="https://doc.biblissima.fr/assets/schema_manifeste_iiif.svg" width="700">



---

## Contenus servis par l’API Image

<img src="https://doc.biblissima.fr/assets/mirador-iiif-api-image.png" width="700">

---

## Contenus servis par l’API Présentation

<img src="https://doc.biblissima.fr/assets/mirador-iiif-api-presentation.png" width="700">

---

## Structure de données

<img src="https://iiif.io/api/assets/images/data-model.png" width="400">

https://iiif.io/api/presentation/3.0/

---

## Ex. de manifestes

#### Archives :

- Archives départementales de la Vienne : *La Nouvelle République du Centre-Ouest : 8 septembre 1944-30 décembre 1945*([Manifeste JSON](https://archives-deux-sevres-vienne.fr/ark:/28387/vta563c56f414a055ae/manifest) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://archives-deux-sevres-vienne.fr/ark:/28387/vta563c56f414a055ae/manifest))
- Archives fédérales suisses : *Procès-verbal(-aux) des décisions 08.05.1945* ([Manifeste JSON](https://api.chgov.bar.admin.ch/manifests/32328752/32328752.json) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://api.chgov.bar.admin.ch/manifests/32328752/32328752.json))

#### Bibliothèques :

- Bibliothèque Mazarine : *La Bible de Gutenberg* ([Manifeste JSON](https://mazarinum.bibliotheque-mazarine.fr/iiif/1703/manifest) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://mazarinum.bibliotheque-mazarine.fr/iiif/1703/manifest))
- Ghent University Library : *[map] Gent* ([Manifeste JSON](https://adore.ugent.be/IIIF/manifests/archive.ugent.be:8ED9BD60-2689-11E6-BB79-D668D43445F2) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://adore.ugent.be/IIIF/manifests/archive.ugent.be:8ED9BD60-2689-11E6-BB79-D668D43445F2))
- Bayerische Staatsbibliothek : *Logbook of a Ship of Sir Francis Drake’s Last Voyage* ([Manifeste JSON](https://api.digitale-sammlungen.de/iiif/presentation/v2/bsb00110131/manifest) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://api.digitale-sammlungen.de/iiif/presentation/v2/bsb00110131/manifest))

#### Musées :

- Getty Museum : *Irises* ([Manifeste JSON](https://media.getty.edu/iiif/manifest/53be857e-41e8-4198-b45d-2e0f52d3051b) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://media.getty.edu/iiif/manifest/53be857e-41e8-4198-b45d-2e0f52d3051b))
- Statens Museum for Kunst : *View of the Interior of the Colosseum* ([Manifeste JSON](https://api.smk.dk/api/v1/iiif/manifest/?id=KMS1776) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://api.smk.dk/api/v1/iiif/manifest/?id=KMS1776))
- The Royal Collection Trust : *Raphael Collection portfolio 26* ([Manifeste JSON](https://rct.resourcespace.com/iiif/970585/) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://rct.resourcespace.com/iiif/970585/))

???

Dublin City Library and Archive : *Royal charters to the city of Dublin* ([Manifeste JSON](https://by2022.adaptcentre.ie/iiif/v1/160821/manifest) – [Ouvrir dans Mirador](https://portail.biblissima.fr/m3/?theme=dark&context=collection&iiif-content=https://by2022.adaptcentre.ie/iiif/v1/160821/manifest))

---

name: api

class: inverse center middle

# Un panorama sur les outils

---

## Awesome IIIF

https://github.com/IIIF/awesome-iiif



---

## Serveurs d’images

https://iiif.io/get-started/image-servers/

- ex. [Cantaloupe](https://cantaloupe-project.github.io/)

« Museum Community Letter to Digital Asset Management (DAM) Software Vendors ». 2017. mai 1. https://iiif.io/news/2017/05/01/letter-to-dams/.

Solution intégrée à (cf. https://iiif.io/get-started/vendors/)

- **[eMuseum](https://www.gallerysystems.com/international-image-interoperability-framework-iiif/)** de GallerySystems supporte l’API Image et l’API Présentation et prévoit d’implémenter d’autres fonctionnalités prochainement (ex. : [Fricks Collection](https://collections.frick.org/collections), [Österreichische Galerie Belvedere](https://sammlung.belvedere.at/), [The Nelson-Atkins Museum of Art](https://art.nelson-atkins.org/collections))
- **[Gallery Systems / TMS](https://www.gallerysystems.com/international-image-interoperability-framework-iiif/)**
- **[Axiell collections](https://www.axiell.com/fr/solutions/product/axiell-collections/)**
- **[Axiell DAMS, PICTION](https://www.axiell.com/solutions/product/digital-asset-managent/)**
- **[CollectiveAccess](https://collectiveaccess.org/)**
- **[Omeka-S](https://omeka.org/s/modules/IiifServer/)**
- ...

???

Attention aux qualités d’implémentation variables. Version API présentation notamment.

Serveur d’image, pyramidage ?

https://groups.google.com/g/iiif-discuss/c/IxGn5eUNhrU

*Exploration, comparaison et zoom, grâce au IIIF, d'oeuvres du catalogue des collections (Art Gallery of Ontario à Ottawa). Deux vues de la Rome antique de Giovanni Paolo Panini. [Notice 1](https://ago.ca/collection/object/62/32). [Notice2](https://ago.ca/collection/object/62/32).[ ](https://ago.ca/collection/object/62/32 Notice 2. https://ago.ca/collection/object/62/32 )[Manifeste IIIF](https://ago.ca/mirador/compare?objects=47900,44422)*

Selon les cas, le zoom profond et l’import des métadonnées sont associés à la possibilité d’annoter l’image en détourant une zone ([Harvard Art Museums](https://harvardartmuseums.org/collections)).

*Albrecht Dürer, The Lamentation of Christ, encre brune sur papier, 1521, Harvard Art Museums. Photo © President and Fellows of Harvard College. [Notice](https://hvrd.art/o/299883). [Manifeste IIIF](https://iiif.harvardartmuseums.org/viewers/mirador?manifest=https://iiif.harvardartmuseums.org/manifests/object/299883)*

---

## Visionneuses

https://iiif.io/get-started/iiif-viewers/

https://iiif.io/api/cookbook/recipe/matrix/

- [Mirador](https://projectmirador.org/) ou [Tify](https://tify.rocks)
- [Universal Viewer](https://universalviewer.io/)
- [Diva](https://diva.simssa.ca/) Canadien!

---

## Outils pour les expositions

- [Exhibit](https://exhibit.so)
- [Storiiies](http://storiiies.cogapp.com)
- [Wax](https://minicomp.github.io/wax/)
- [Adno](https://adno.app)

---

## Éditeur de manifestes, annotations

[Digital Manuscripts Toolkit](http://dmt.bodleian.ox.ac.uk)



---

# Références

---

## Contenus pédagogiques

  - « Formation IIIF ». 2023. novembre 29. https://doc.biblissima.fr/formation-iiif/.
  - « Introduction à IIIF ». s. d. Documentation Biblissima. https://doc.biblissima.fr/iiif/introduction-iiif/.
  - « IIIF Online Workshop ». 2022. 2022. https://training.iiif.io/iiif-online-workshop/.
  - Robineau, Régis. (2020) 2021. Atelier IIIF DHNord2020. https://github.com/regisrob/Atelier_IIIF_Conference_DHNord_2020.
  - « IIIF Online Workshop ». 2020. septembre 2020. https://training.iiif.io/iiif-online-workshop/September2020.html#sessions.
  - Roddis, Tristan, Jeff Steward, et Richard Palmer. 2019. « Hands-on IIIF ». Workshop at Museums and the Web 2019. Boston, MA. Wednesday 3rd April 2019. Consulté le 12 mai 2019. https://docs.google.com/document/d/1QprIoyCDExcAz6_O6qMr67sYV4F5qsQZpw9ZuiKohs0/edit?usp=embed_facebook.
  - Introduction to IIIF - Tom Cramer, Stanford University. Réalisé par IIIF. 2018. https://www.youtube.com/watch?v=Z3ZgEv4p37o

---

## Resources

- **[Standards](https://iiif.io)**

- IIIF/awesome-iiif. (2016) 2020. International Image Interoperability Framework. https://github.com/IIIF/awesome-iiif.
- « The Cookbook of IIIF Recipes ». s. d. Consulté le 27 mars 2022. https://iiif.io/get-started/cookbook/.
- « IIIF Cookbook ». s. d. Consulté le 3 mai 2022. https://iiif.io/api/cookbook/.
- Community repository for documenting stories and use cases related to uses of the International Image Interoperability Framework.  : IIIF/iiif-stories. (2014) 2019. International Image Interoperability Framework. https://github.com/IIIF/iiif-stories.

---

## Articles d’intérêt

- « Museum Community Letter to Digital Asset Management (DAM) Software Vendors ». 2017. mai 1. https://iiif.io/news/2017/05/01/letter-to-dams/.
- « IIIF à l’INHA ». 2019. *Institut national d’histoire de l’art*. https://iiif.inha.fr/.
- « IIIF pour les musées de France ». 2024. *Ministère de la Culture*. Consulté le mars 8. https://www.culture.gouv.fr/Thematiques/Musees/Pour-les-professionnels/Travailler-en-reseau/IIIF-pour-les-musees-de-France.
- Mallory, Gavin. 2019. « IIIF for Museums, Explained ». *Medium*. juillet 1. https://blog.cogapp.com/iiif-for-museums-explained-49fd0560e1ba.
- Mallory, Gavin. 2018. « Deeper, More Meaningful Art-Experiences with Digital ». *Medium*. juillet 24. https://blog.cogapp.com/deeper-more-meaningful-art-experiences-with-digital-8afd7bdeb35b.
- Cullins, Isoke, et Serena Parr. 2021. « A New Way to Experience Art Online. Getty’s new digital project brings ancient artworks out from behind the glass ». décembre 7. http://www.getty.edu/news/get-closer-to-ancient-mesopotamia-than-ever-before/.
- Carini, Luca. 2017. « Easy Image Alignment with IIIF ». *V&A Blog*. août 23. https://www.vam.ac.uk/blog/digital/easy-image-alignment-with-iiif.
- White, Jon. 2017. « Innovatively Repurposing Content across Multiple Platforms ». *Medium*. septembre 7. https://blog.cogapp.com/iiif-for-storytelling-1e36ce277f48.
