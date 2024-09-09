# Atelier IIIF


retours et questions sur teams

## lundi matin


## formation IIIF

forteresse (coin en haut à gauche): x=3420, y=2494
cercle : x= 2413px, y=1309px

what are we trying to do? digital storytelling
Prototyping phase: we are looking at the available

-  presentation tools
    - juncture
    - exhibit
    - storiiies
- what we could do ourselves?
    - operations that researchers do
    - go beyond a presentation tool, make it into a research tool


1. **What we are doing (specify features of the appication)**

- digital storytelling exhibition of righettino image (smooth zoom in/out, show annotations or note of explanation for the different parts of image, etc)
- installed osd and uv with base example each
- dint installed till now 
    -> canvas panel (react stuff), curation viewer (dint find proper documentation for installation), divajs
- current status 
    -> downloaded the manifest with help of oncs (able to see the image in mirador but not in uv)
- uv -> cross origin request blocked error
- going through the github repo and docs of uv to view our image, how we can add and customize interactivity
- openseadragon (we can look at the plugins and extensions and code file examples)
- how we can show or point out exact parts of image which we are going to point out and show annotations for that part (overlay ?)
- how we can add some text or annotations at the different parts of image?

2. **Presentation API**

- is their compatibility between versions (v2 vs v3) ?
- manifest editor for presentation api ?


### [Project demo](https://docs.google.com/presentation/d/1OZwAKY83B_jD0QYiAZq6zTvpx2wYbuEBwJn2c5fwlkE/) day

[Visual essays tool](https://visual-essays.app/)
- looks a lot like juncture


[use of IIIF](https://jhna.org/articles/jhna-2-point-0/) in [art history scholarship](https://jhna.org/articles/rubens-invention-evolution-fall-of-phaeton/)

[all maps](https://allmaps.org/)

Slack channels
- general - general discussion and announcements
- beginner - beginner questions lots of people to help
- iiif-in-the-classroom - ideas for IIIF in the classroom
- [curators_of_awesome](https://github.com/IIIF/awesome-iiif) - become a curator of awesome by helping to curate
- mirador - ask questions and see the latest developments with Mirador
- technical - ask difficult technical questions :-)

[Community Calls](https://iiif.io/community/call/)

Community groups:
- [3D](https://iiif.io/community/groups/3d)
- A/V
- Archives
- Discovery for Humans
- Manuscripts
- Maps
- Museums
- Newspapers
- Outreach

Technical Groups:
- [3D](https://iiif.io/community/groups/3d/tsg/)
- Discovery
- Maps 
- Authentication
- Content Search


Stay informed
- Join the monthly newsletter
- Join the IIIF Discuss email list



notes for my presentation
- having an image server set up by the library
  - great, but in PresentationAPI v3
  - transparency of the images (jpg vs png)
- bodleian as basis
  - editing the manifest
  - locating the overlay position
- using overlays and annotations 
- using the "pre-existing" annotations in xml 
we were thinking of IIIF as developpers - lets code, code, code. We took a major step back and had fun experimenting with available libraries and tools to familiarize ourselves with all that is available before we continue our experimental approaches


### Annotations
browser compatibility: chrome and firefox should both be fine

Workbench issue: v3 images don't work (v2 will work but the thumbnail image in the bodleian editor won't work)

How to generate the correct metadata for the overlay position? no perfect solution, work in progress

Is the size of the canvas in pixels? I can’t figure out how to compute the position for my overlay image
- standard says that it doesn't have to be pixels but it is almost always pixels
- image size is pixels
for our case: 'real’ width and height because we prepared it that way, wouldn’t usually happen
_canvas size / full image_:
width: 9645
height: 7181

_Turin forteress_
x:	3410
y:	2482
width:	1913
height:	2154


Does IIIF keep the image transparency (png)?
- mirador will request it as a jpg, and jpeg doesn't support 
- info.json → [prefered format](https://iiif.io/api/image/3.0/#55-preferred-formats) in the info.json =  png
- ask on the cantaloupe 

level0 media that is not images? audio.. architecture of the server
- no special av server → just put it as a direct link to the content with the https


[Mirador URL](https://projectmirador.org/embed/?iiif-content=https://manifests.collections.yale.edu/ycba/obj/5005) that we can refresh

[annotations Lena](https://annonatate.herokuapp.com)


### One on one session

Storytelling in IIIF is a rather crowded space
- exhibit: allows using multiple manifests, doesn't require you to make your own manifest
- storiiiies: single image → more basic
- [Cartinal](https://cartinal.leventhalmap.org/documentation/panel-truck.html) maps-related stoytelling tool
- Omeka
- [Annona](https://ncsu-libraries.github.io/annona/range/)

Do we really need to use a manifest? If OpenSeaDragon doesn't use it

Text annotations encoded in XML-TEI, can they stay in this format? Is there a real advantage to have the annotations stored inside the manifest? 
Alto to annotations [examples](https://glenrobson.github.io/iiif_stuff/alto2annotations/)


[annotorious](https://recogito.github.io/annotorious/)

image zoomers:
- openseadragon
- leaflet
- openlayers

https://glenrobson.github.io/iiif_stuff/
- aller voir le projet avec des [memes](https://glenrobson.github.io/iiif_stuff/meme_challenge/) pour le overlay

### Presentation API

presentation API [libraries](https://github.com/IIIF/awesome-iiif#presentation-api-libraries)

#### Questions 2022-06-29
- Is there a manifest editor for presentation API v3 ?
    - should be coming out soon
    - should be more complete
- Compatibility between v2 and v3? Our server (small testing server set up by our library) is in v3 and it seems to be causing many issues and errors (it’s hard to distinguish between our mistakes and compatibility issues). 
    - use the [iiif presentation validator](https://presentation-validator.iiif.io/)
----

    - escaping the / into %2f for cantaloupe to understand that the slashes in the path are the path
- v2 vs v3: [cookbook](https://iiif.io/api/cookbook/recipe/matrix/)
    - v3 supports AV, v2 doesn't
    - v3 manifest can use v2 images but not the contrary (v2 manifest cannot use v3 images)
    - changes in json field
    - [vault](https://github.com/IIIF-Commons/vault) : tool that updates v2 to v3
    - language map
    - no more sequences: list of items

3D and photogrammetry: not yet supported but will be probably in v4 (still early on in the process, x y time and 4th dimension?)
- 3D technical group is open to everybody
- probably couple years before viewers support it
- [UV supports 3D](https://uv-v4.netlify.app/#?c=&m=&cv=&xywh=-2403https://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=-2403%2C-197%2C7373%2C3936&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.jsonC-197https://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=-2403%2C-197%2C7373%2C3936&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.jsonC7373https://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=-2403%2C-197%2C7373%2C3936&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.jsonC3936&iiifManifestId=https%3Ahttps://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=-2403%2C-197%2C7373%2C3936&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.jsonFhttps://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=-2403%2C-197%2C7373%2C3936&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.jsonFbiiif-template-example-3kntb3jpl-mnemoscene.vercel.apphttps://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=-2403%2C-197%2C7373%2C3936&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.jsonF3dhttps://uv-v4.netlify.app/%23?c=&m=&cv=&xywh=&iiifManifestId=https%3A%2F%2Fbiiif-template-example-3kntb3jpl-mnemoscene.vercel.app%2F3d%2Findex.json) already, using a manifest that looks like IIIF but is not (u)
- not officially part of IIIF yet
- exhibit uses UV under the hood and can use the 3D objects that are supported (Ed S.)


TEI: From the page [workshop](https://training.iiif.io/advanced_iiif/modules/FromThePage/)
Image location:
- V&A [Compariscope](https://vanda.github.io/iiif-features/compariscope.html?manifest=img/manifest_constable.json)
- [UCD tool](https://jbhoward-dublin.github.io/IIIF-imageManipulation/index.html?imageID=https://images.eap.bl.uk/EAP922/EAP922_1_5_54/1.jp2)
- [image registration](https://tanc-ahrc.github.io/IIIF-TNC/seminar01.html)
v3 recipe to do overlay in [cookbook](https://iiif.io/api/cookbook/recipe/0036-composition-from-multiple-images/)

#### common errors
- can't go from an https site to an http manifest 
- CORS issue
    - headers in the image server and manifest
    - viewer won't be able to access the image without them
    - without: will work in our own website but not on others
- JSON issues
    - JSONLint
    - Validator

#### manifest _1..*_ sequence _1..*_ canvas _1..*_ content

manifest: json-ld
- label
- metadata and description
- attribution (provider of the manifest)
- licence
- logo (visual branding to indicate the provider of the content)

sequence: ordering

canvas: holder for image contents and other types of annotations
- height and width create and abstract coordinate space

content _1..*_ ressources: images, other types of content annotated onto it

multiple images annotated onto a single canvas: overlay 7:13 [à regarder ensemble!]
<!--terme annotation utilisé pour dire "placé sur le canva"-->

#### Canvas
{
    @type: "sc:Canvas",
    @id: "example.org/canvas/id/1",
    label: "recto, unframed", <!-- display label-->
    height: 2000,
    width: 1500,
    images: [ ...annotations... ] <!-- contains the annotations that paint the image on the canvas-->
}

#### Annotation
{
    @id: "example.org/annotation/id/1",
    @type: "oa:Annotation",
    motivation: "sc:painting", <!-- in the specifications: painting content onto a canvas-->
    on: "example.org/canvas/id/1", <!-- id of the canvas-->
    ressource: { <!-- references an image-->
        @id: "example.org/iiif/123/full/1500,/0/default.jpg",
        @type: "dctypes:Image",
        format: "image/jpeg",
        service: { ...Image API Service...}
        height: 2000,
        width: 1500
    }
}

#### Service
Image API service

reference to the IIIF image API service for the image 
the viewer sees the service and contacts the image API server and requests the content required to be rendered






index --> navigation




#### Questions
- quels types d'annotations textuelles (ie analyse/interprétation, source, notes)
- meilleurs endroit pour stocker les annotations textuelles ? (dans le manifest ou ailleurs ?)
- quels sont les différents layers ? 
- Comment réperer les zones ? 
- Comment repérer ces différents types d'annotation dans le manifest ?



Photoshop → Save Image Pyramid

Preserves multiresolution information. Photoshop does not provide options for opening multiresolution files; the image opens at the highest resolution within the file. However, Adobe InDesign and some image servers provide support for opening multiresolution formats.



people have multiple image servers behind a proxy to serve hundreds and thousands of users. They all work with the same storage. 

- pyramid tif is fastest to load

supports any input format, but some work better than other
- pyramid tif and jpeg2000: getting higher qualities as you zoom in
- pyramid tif  careful: space requirements → creates very large files but faster than other formats
- larger institutions are using jpeg2000 to reduce storage and therefore cost

Processors
kakadu decoding library (paying, but no free one works as well)

functionality for user to download a copy, create links to different resolutions  


### Image API
- best image format ? 
- Good to keep copies in different formats ?
    - archival copy: quality
    - iiif copy: we can compress it
    - all others can be generated on the fly
- minimum resolution ? 
    - no absolute minium
    - problems when the images are small (smallest ok: iphone images), else you don't get the benefit of fast image access
    - way to use a non IIIF image in a manifest (extra)

composite image: 
- one in background, others on top
- overlay requires all images to be iiif (in mirador)
- paint multiple images on a canvas



## Séance de travail 
4 mai 2022

Présences:
- Emmanuel Chateau-Dutier: directeur scientifique - Ouvroir
- Kristine Tanton: directrice scientifique - Ouvroir
- William Diakité: developpeur - Ouvroir
- Lena Krause: responsable du laboratoire - Ouvroir
- Martin Sévigny : Directeur des technologies - Les bibliothèques UdeM
- Emir Chouchane : Conseiller en médiation technologique - Les bibliothèque UdeM
- Philippe Deschamps : Bibliothécaire LRCS
- Jérôme Vogel : Professeur en design, École multidisciplinaire de l'image, UQO 


### Le protocole IIIF

La bibliothèque utilise déjà IIIF dans [calypso](https://calypso.bib.umontreal.ca/) avec Mirador
- un des problèmes: versions de diffusion, l'archive des sources (éventuelle plus haute résoution) ne sont pas (encore) diffusables

Exemple 
- Ledoux BNF: annotations
- TU Delft Library: storytelling, exposition numérique avec Gatsby (générateur de site statique)
- Juncture

Hypothèse svelte + manifeste IIIF + contenus markdown

Créer un outil facile à prendre en main:
- monter des expositions
- prototypage

### Svelte
Framework Javascript:  [documentation](https://svelte.dev/docs)
svelte  = sorte de html (travail en balises)
- balis `<script>` pour tout le contenu js
- reste en html directement
- syntaxe propre
- binder (lier) des valeurs
- générateur de site statique: code est recompilé pour génrer un bundle pour avoir un site full html statique ou SSG (génération côté serveur)

SvelteKit: manière de construire des applications avec svelte, stadards pour la structure (création de composants, pages, routing, store, sessions, ...): environnement de développement autour de svelte

Dossier `static`: contient favicon, images et autre contenus statiques
`app.html`: structure html de base avec %svelte.body% (% appelle le contenu des pages)
`routes` pages .svelte à leur nom ou dans les dossiers
`__layout.svelte`: contient <slot/>, peut contenir par exemple une navigation, 
`.md` interprété en html avec mdsvex (librairie pour le markdown), peut contenir des composants
Possibilité d'utiliser un adaptateur pour l'automatisation avec github actions pour


### Intérêts
- idée de développer un outil *no code* pour les expos numériques
- quels moyens de diffuser l'outil? 

Ouvroir a de l'argent pour réaliser un outil qui pourra être développé, on peut faire un prototype

Mirador: visualiseur, mais pas digital storytelling. Plusieurs existnts, mais dans le cadre de la muséologie numérique, définir une nomenclature des types d'interactions qu'on peut avoir avec des images dans le web, concevoir une typologie qu'on peut implémenter numériquement pour générer des blocs prédéfinis à utiliser librement. 
- expositions en ligne
- cours et conférence

Capacité de faire l'équivalent voire "mieux" que Juncture, base sur laquelle on pourra probablement capitaliser. 

Pourquoi les viewers actuels ne sont-ils pas suffisants? 
Pourquoi ne pas développer un composant générique qui fonctionnerait avec les viewers actuels? 
Habillage des viewers comme OpenSeaDragon. mais aussi assemblage avec du contenu (texte, données, ...) pour former un digital storytelling 
Gagner en possibilités, flexibilité...

Volet expositions virtuelles pour les bibliothèques: rapidement désuet, quel horizon pour la pérénité? 
Limiter les dépendences: svelte est une dépendence mais tempérée, car le site statique généré n'est pas dépendant, ne contient que des pages statiques.
JAM stack pérenne + éditeurs pour connecter à des sites statiques
A-t-on besoin d'un éditeur si on est juste basés sur du markdown? 

Exemple Angular Jérôme
https://github.com/NationalLibraryOfNorway/ngx-mime/wiki/Getting-Started
- viewer openSeaDragon chargé par le module Angular (module national library of norway) + feuille de style
- création de composants, association dynamique à la volée
- chaque composant: js (typescript), css, html
- n'utilise que les trois fondamentaux du web

### Idéation

Comment interfacer la création d'un composant, quels enjeux? 
Que fait ou ne fait pas OpenSeaDragon? 
Quels enjeux dans les choix technologiques? 

approche exploratoire: 
- créer un composant
- essayer de reproduire juncture
démonter les exemples: juncture, gatsby

Démonter gatsby avant la pause
Tentative de le reproduire en svelte

### Gatsby + TU Delft Library
[exemple d'expo](https://delft-static-site-generator.netlify.app/en)
[entrée de blog](https://medium.com/digirati-ch/reaching-into-collections-to-tell-stories-3dc32a1772af)

- grille
- canvas : images composites assemblées
    - basé sur l'information dans le manifeste
- texte
- sous-pages

Est-ce que OpenSeaDragon est capable de composer un canevas avec plusieurs images? C'est le principe de [canvas panel](https://canvas-panel.digirati.com/#/about)

Sorte de manifeste augmenté: [exemples](https://github.com/digirati-co-uk/delft-static-site-generator/tree/master/content/exhibitions)

Documentation : https://delft-static-site-generator.netlify.app/docs
- structure: https://delft-static-site-generator.netlify.app/docs/docz-technical-site-structure

https://canvas-panel.digirati.com/#/about
utilise react

### Expérimentation
[Github ouvroir](https://github.com/ouvroir)

[expérimentations du jour](https://github.com/ouvroir/expot-iiif)
[notes et exemples sur la création de manifestes 2021 lena](https://github.com/publicarchi/cbc/blob/master/testManifeste/Script-manifeste.md)
[test d'intégration de viewers en vanilla javascript](https://github.com/ouvroir/IIIF)

Live session https://prod.liveshare.vsengsaas.visualstudio.com/join?FE1936F652B12443BAD694B11F17FE392D1A


#### OpenSeadragon
```
npm install openseadragon
npm install @types/openseadragon
```

All [required and optional settings](https://openseadragon.github.io/docs/OpenSeadragon.html#.Options) for instantiating a new instance of an OpenSeadragon image viewer




https://svelte.dev/repl/28f4b2e36e4244b8b23cae3d584c4c88?version=3.16.6

Doc svelte component https://svelte.dev/docs#component-format

[UV example](https://codesandbox.io/s/uv-simple-example-1p175?file=/index.html)


IIIF commons

https://iiif-commons.github.io/manifesto/



---


Présentation officielle avec les bilbiothèques
date proposée: 31 mai


Notes de la [première rencontre](https://github.com/ouvroir/labouvroir/blob/main/cr/crAtelier2022-02-22.md)

@lenamk: tester l'affichage l'image servie par mon serveur cantaloupe local avec les viewers mis en place. 



## Séance de travail 9 avril
14h au campus MIL, labo de visualisation

test de viewers et préparation de l'activité du 3 mai

Emir a créé une instance (avec documentation) sur [digital ocean](https://cloud.digitalocean.com) (basé à Toronto, scalable, paye en fonction de ce qu'on utilise), reliée au nom de domaine [img.humanitas.digital](https://img.humanitas.digital/)
- s’efface le 1er juin 
- problème du certificat 
- [cantaloup](https://img.humanitas.digital:8182)
- [éditeur de manifest](https://img.humanitas.digital/manifest/public/)

Viewers: [tests](https://github.com/ouvroir/IIIF)
- Emir a déjà fait un exemple avec VISP (découpe l'îmage), servie avec un viewer OpenSeaDragon dans une page html
- [Universal viewer sandbox](https://codesandbox.io/s/uv-simple-example-1p175?file=/index.html) cdn dans une page html


Cantaloupe est compliqué à cause de https, voir si on peut régler ça
Sinon essayer d'autres serveurs? 

Exemple d'intégration (OpenSeaDragon) par [media arts center](https://mcid.mcah.columbia.edu/search/fieldwork-bauhaus). Chouettes [thumbnails](https://learn.columbia.edu/) qui ont un effet de zoom ou pan quand passe la souris dessus


## Discussion du 7 avril 2022

- serveur d’image chez [digital ocean](https://try.digitalocean.com/freetrialoffer/) (100$ offert, 60 jours) pour un VPS (virtual private server)
- nom de domaine, A name, webmanager pour faciliter les certificats de sécurité
- installation cantaloupe
- requiert config pour ajouter d'autres formats que du tiff

Emmanuel a demandé l'accès à la formation IIIF à Johanne, sinon possibilité de le passer dans le FEI.  

### Présentation du 3 mai
Sensibiliser les gens à l'intérêt de IIIF → centré côté utilisateur
Intérêt interne: se faire la main, avoir un serveur d'image à nous
- manifeste
- viewer
- applications (exhibit)

Pour garder la forme d'un hackathon interne, écrire à Danny et [Maryna](maryna.beaulieu@umontreal.ca), [Camille](camille.veillette.peclet@umontreal.ca) (directrice d'Emir) en cc: 
- 1-2 heures de démo
- suite: séance de travail en mode hackathon

Espace de coworking: soit au campus MIL, soit à la bibliothèque des livres rares, soit chez nous (mais le 4 mai)


## Discussion du 30 mars 2022
https://calypso.bib.umontreal.ca/ → avec IIIF

- travailler avec des serveurs d'images existants vu qu'il y en a 

Option 1: Former des gens (Démonstration)
- présenter IIIF
- monter une expo type exhibit
- créer des annotations etc

**Option 2**: se former nous (hands-on /hackathon: approfondir nos connaissances)? 
- arriver à avoir un dispositif assez facile (avec des composants svelte) pour assembler du contenu: md + IIIF
- Quel documents, quelles collections? 
    - udem calypso: documents sur l'architecture de l'université`
    - Righettino, avec Denis
    - autre source
- prototype: quelques images
    - structure de base (répétable) + composantes faciles d'accès
    - afficher une image, la recadrer, volume multipaginé
    - faire un moodboard type [Delft](https://delft-static-site-generator.netlify.app/en/exhibitions/rise-of-a-campus)

Option 2: 4 mai, toute la journée
- préparer un use case pour le hackathon
- durée, communication, forme 
    - coorganisation ouvroir x laboratoire de visualisation
    - au MIL
    - avec les bibliothèques, inviter d'autres bibliothécaires

À suivre: 
- bibliothèques et IIIF
- membership au consortium
- formations IIIF (formation IIIF.io du consortium)


Divers
- taskforce IIIF ?
Directrice d’Emir : camille.veillette.peclet@umontreal.ca


Invités potentiels (format hackathon)
- Kristine K (ouvroir)
- Emmanuel Chateau-Dutier (ouvroir)
- Lena Krause (ouvroir)
- William Diakité (ouvroir)
- Danny Letourneau (bib)
- Philippe Deschamps (bib)
- Ève Paquette-Bigras (bib)
- Emir Chouachane (ouvroir)
- Denis Ribouillault (selon le sujet)

## Explorations du 15 mars 2022

Présentation de Régis Robineau à [DH Nord 2020](https://projet.biblissima.fr/sites/default/files/atelier_iiif_dhnord_robineau_20201118.pdf)
- besoins communs p.16
- interopérabilité pour croiser les données issues de différents serveurs


Labo
- mettre en place un entrepôt IIIF pour l'ensemble de nos applications
- y connecter des outils qui facilient l'utilisation des images

Exemples explorés : 

- [Heiji Monogatari Emaki (Tale of the Heiji Rebellion)](http://digital.princeton.edu/heijiscroll/scroll.html), Tom Conlan, Princeton library
- [Catalogue de la bibliothèque Princeton](https://catalog.princeton.edu/catalog/9981720703506421)

[Bodleinan Manifest Editor](https://digital.bodleian.ox.ac.uk/manifest-editor)

[Documentation de l'API IIIF Gallica](https://api.bnf.fr/fr/api-iiif-de-recuperation-des-images-de-gallica)

https://github.com/ProjectMirador/mirador

Identificants: 
- ressource
- folio
- extension de fichier
- manifest.json donne les informations sur la présentation du document
- info.json contient les dimensions

Visionneuse IIIF
- OpenSeaDragon
- Mirador
- [mirador Integration](https://github.com/ProjectMirador/mirador-integration) (with react)
- [Diva](https://diva.simssa.ca/) Canadien!
- [Universal Viewer](https://universalviewer.io/)


Online curation with IIIF
- [Exhibit.so](https://www.exhibit.so/)
- [Range storyboard](https://ncsu-libraries.github.io/annona/range/)


## Resources

### Standards

https://iiif.io

- IIIF/awesome-iiif. (2016) 2020. International Image Interoperability Framework. https://github.com/IIIF/awesome-iiif.
- « The Cookbook of IIIF Recipes ». s. d. Consulté le 27 mars 2022. https://iiif.io/get-started/cookbook/.
- Community repository for documenting stories and use cases related to uses of the International Image Interoperability Framework.  : IIIF/iiif-stories. (2014) 2019. International Image Interoperability Framework. https://github.com/IIIF/iiif-stories.


### Formations

- « IIIF Online Workshop ». 2022. 2022. https://training.iiif.io/iiif-online-workshop/.
- Robineau, Régis. (2020) 2021. Atelier IIIF DHNord2020. https://github.com/regisrob/Atelier_IIIF_Conference_DHNord_2020.
- « IIIF Online Workshop ». 2020. septembre 2020. https://training.iiif.io/iiif-online-workshop/September2020.html#sessions.
- Roddis, Tristan, Jeff Steward, et Richard Palmer. 2019. « Hands-on IIIF ». Workshop at Museums and the Web 2019. Boston, MA. Wednesday 3rd April 2019. Consulté le 12 mai 2019. https://docs.google.com/document/d/1QprIoyCDExcAz6_O6qMr67sYV4F5qsQZpw9ZuiKohs0/edit?usp=embed_facebook.
- Introduction to IIIF - Tom Cramer, Stanford University. Réalisé par IIIF. 2018. https://www.youtube.com/watch?v=Z3ZgEv4p37o

### Outils

- https://jbhoward-dublin.github.io/IIIF-imageManipulation/
- http://slowlooking.cogapp.com
- « Canvas-panel-cookbook ». s. d. Consulté le 27 mars 2022. https://canvas-panel.digirati.com/#/.
- Delft Static Site Generator. (2018) 2022. JavaScript. digirati-co-uk. https://github.com/digirati-co-uk/delft-static-site-generator.
- « IIIF Manifest Editor ». s. d. Consulté le 27 mars 2022. https://digital.bodleian.ox.ac.uk/manifest-editor/#/?_k=cfbepm.
- Robson, Glen. (2015) 2022. SimpleAnnotationServer. JavaScript. https://github.com/glenrobson/SimpleAnnotationServer.
- « Storiiies ». s. d. Cogapp. Consulté le 29 mars 2019. http://storiiies.cogapp.com/.
- « Exhibit ». s. d. Consulté le 27 mars 2022. https://exhibit.so/.
- Robson, Glen. (2015) 2022. SimpleAnnotationServer. JavaScript. https://github.com/glenrobson/SimpleAnnotationServer.
- https://universalviewer.io


### Collections d’art publiées avec IIIF (sélection)

https://iiif.io/guides/finding_resources/

cf. fichier dans labouvroir https://github.com/ouvroir/labouvroir/blob/main/ressources/iiifResources.yml


#### Bibliothèques

- [Bitish Library (some collections)](https://www.bl.uk/collection-guides/iiif)
- [Endangered Archives Programme](https://eap.bl.uk)
- [Gallica](https://gallica.bnf.fr)
- [The MDZ](https://www.digitale-sammlungen.de)
- [Qatar Digital Library](https://www.qdl.qa/en)
- [David Rumsey map collection](https://www.davidrumsey.com)
- [University of Washington Libraries](https://content.lib.washington.edu)
- [University of Toronto Libraries](https://library.utoronto.ca/digital-collections)
- [University of St Andrews Libraries](https://www.st-andrews.ac.uk/library/special-collections/photographs/)

https://www.bl.uk/collection-guides/iiif
Philadelphia Museum of Art

Duke University/Digital Art History Research Lab

exploiter
https://www.library.universiteitleiden.nl/binaries/content/assets/ul2ub/bijzondere-collecties/list-of-iiif-collections.pdf


https://openseadragon.github.io/examples/tilesource-iiif/