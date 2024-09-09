- [pad](https://demo.hedgedoc.org/PAWlYGMWTCKX9WCFf4Ao1w?edit#)

  ## International Image Interoperability Framework (IIIF)

  https://iiif.io/

  « Enabling Richer Access to the World’s Images »

  Initiative communautaire regroupant des musées et des bibliothèques ou des entreprises pour concevoir des entrepôts pour la distribution d’images.

  Dispositif fondé sur la définition d’Interfaces programmables qui encourage le développement de logiciels.

  Exemples de ressources

  - [Awesome IIIF](https://github.com/IIIF/awesome-iiif)
  - [Ouvroir, répertoire de ressources IIIF](https://github.com/ouvroir/labouvroir/blob/main/ressources/iiifResources.yml)

  Communauté

  - https://training.iiif.io
  - https://iiif.io/community/#community-groups-committees
  - https://github.com/ryanfb/iiif-universe

  ## Exemples

  - Visualisation du même contenu dans plusieurs viewers
    https://gallica.bnf.fr/iiif/ark:/12148/bpt6k1047050b/manifest.json

    - [UniversalViewer](https://uv-v4.netlify.app/#?manifest=https://gallica.bnf.fr/ark:/12148/bpt6k1047050b&c=&m=&cv=)
    - [Mirador 3](https://mirador-dev.netlify.app)
    - [Tify](https://tify.rocks/)
    - [IIIF Curation Viewer](http://codh.rois.ac.jp/icp/index.html.en)

  - Hyperzoom et contenus complexes
    
    - 2014, Scrolls illustrating a story about the Sagami River, Kyoto [1660?-1670?]. Princeton University Library
    
      https://blogs.princeton.edu/manuscripts/2014/09/22/japanese-scrolls-digitized/
    
      https://catalog.princeton.edu/catalog/9981720703506421#view

    - Ōmi Kuni-ezu -- 近江國絵圖, Japan, 1837 (345 x 504 cm). Stanford University Libraries
    
      https://purl.stanford.edu/hs631zg4177
    
  - Recadrer et citer zone d’image

  - Assemblage de contenus conservés dans différentes institutions

    - [Demo Biblissima](https://demos.biblissima.fr)
    - https://fragmentarium.ms/overview/F-4ihz
  
  - Visualisation d’images multiples
  
    - [JHNA Journal of Historians of Netherlandish Art](https://jhna.org)
  
  - Expositions numériques
  
    - [Expo Academic Heritage](https://delft-static-site-generator.netlify.app/en), [The Garden of Earthly Delights](https://archief.ntr.nl/tuinderlusten/en.html)
    - [Mesopotamia](https://mesopotamia.getty.edu), [Cogapp, Slow Looking](http://slowlooking.cogapp.com), ou [Storiiies](https://storiiies.cogapp.com/)

  - exemple Annotations

    

  - [Heiji Monogatari Emaki (Tale of the Heiji Rebellion)](http://digital.princeton.edu/heijiscroll/scroll.html), Tom Conlan, Princeton library

  - [Catalogue de la bibliothèque Princeton](https://catalog.princeton.edu/catalog/9981720703506421)

  - [Bodleinan Manifest Editor](https://digital.bodleian.ox.ac.uk/manifest-editor)

  - [Documentation de l'API IIIF Gallica](https://api.bnf.fr/fr/api-iiif-de-recuperation-des-images-de-gallica)

  - https://github.com/ProjectMirador/mirador

  - https://ifilosofia.up.pt/proj/fdtw/fdtw_project

  

  

  ## Les APIs IIIF

  ![image](https://training.iiif.io/iiif-online-workshop/day-one/img/apis.png)

  #### [Image API](https://iiif.io/api/image/)

  L’API Image IIIF spécifie un service web qui renvoie une image en réponse à une requête HTTP(S) standard. L’URI peut spécifier la région, la taille, la rotation, les caractéristiques de qualité et le format de l’image demandée.

  #### [Presentation API](https://iiif.io/api/presentation/)

  L’API de présentation IIIF fournit les informations nécessaires pour permettre un environnement de visualisation en ligne riche pour les objets numériques composés destinés à être présentés à un utilisateur humain, souvent en conjonction avec l’API d’image IIIF.

  #### [Authentication API](https://iiif.io/api/auth/)

  La spécification d’authentification IIIF décrit un ensemble de flux de travail pour guider l’utilisateur à travers un système de contrôle d’accès existant.

  #### [Change Discovery API](https://iiif.io/api/discovery/)

  L’API Change Discovery de IIIF fournit les informations nécessaires pour découvrir et utiliser les ressources IIIF.
  
  #### [Content Search API](https://iiif.io/api/search/)

  La spécification de l’API de recherche de contenu IIIF définit le mécanisme d’interopérabilité pour effectuer des recherches d’annotations textuelles associées à un objet dans le contexte IIIF.

  #### [Content State API](https://iiif.io/api/content-state/)
  
  L’API IIIF Content State fournit un moyen de se référer à une ressource de l’API IIIF Presentation, ou à une partie d’une ressource, dans un format compact qui peut être utilisé pour initialiser la vue de cette ressource dans n’importe quel client.

  ### Distinction Image API / Presentation API

  L’API Image permet d’obtenir des pixels via un service REST. Tandis que l’API de présentation permet de fournir les métadonnées nécessaires pour proposer une expérience de visionnement.

  Les manifeste IIIF et les listes d’annotations définies par l’API de présentation permettent de décrire une collection d’images ou de canvas comme un ensemble ainsi que de référencer des régions particulières d’une image en fournissant des informations complémentaires.

  --> Permet la mise en place d’une véritable narration numérique.
  
  ## Informations sur une image

  ## Paramètres

  ### Informations sur une image

  ```
  {scheme}://{server}{/prefix}/{identifier}/info.json
  ```

  ### Syntaxe des paramètres

  ```
  {scheme}://{server}{/prefix}/{identifier}/{region}/{size}/{rotation}/{quality}.{format}
  ```

  ### Région
  
  region=full

  ![image](https://iiif.io/api/image/3.0/img/full.png)

  ```
  .../full/max/0/default.jpg
  ```

  region=125,15,120,140

  ![image](https://iiif.io/api/image/3.0/img/region_px.png)

  ```
  .../125,15,120,140/max/0/default.jpg
  ```

  ### Rotation

  rotation=22.5
  
  ![image](https://iiif.io/api/image/3.0/img/rotate_22-5.png)

  ```
  .../full/max/22.5/default.png
  ```
  
  ### Ordre des paramètres

  ```
  Region THEN Size THEN Rotation THEN Quality THEN Format
  ```

  region=125,15,120,140 size=90, rotation=!345 quality=gray

  ![image](https://iiif.io/api/image/3.0/img/transformation.png)

  ```
  .../125,15,120,140/90,/!345/gray.jpg
  ```

  ## Informations sur une image
  
  ```
  {scheme}://{server}{/prefix}/{identifier}/info.json
  ```
  
  Réponse en JSONLD
  
  ```
  Content-Type: application/ld+json;profile="http://iiif.io/api/image/3/context.json"
  ```
  
  exemple : https://iiif.io/api/image/3/context.json
  
  ## API présentation
  
  ![image](https://iiif.io/api/assets/images/data-model.png)
  
  https://iiif.io/api/presentation/3.0/
  
  ## Resources
  
  - **[Standards](https://iiif.io)**
  
  - IIIF/awesome-iiif. (2016) 2020. International Image Interoperability Framework. https://github.com/IIIF/awesome-iiif.
  - « The Cookbook of IIIF Recipes ». s. d. Consulté le 27 mars 2022. https://iiif.io/get-started/cookbook/.
  - « IIIF Cookbook ». s. d. Consulté le 3 mai 2022. https://iiif.io/api/cookbook/.
  - Community repository for documenting stories and use cases related to uses of the International Image Interoperability Framework.  : IIIF/iiif-stories. (2014) 2019. International Image Interoperability Framework. https://github.com/IIIF/iiif-stories.


  ### Contenus pédagogiques

  - « Formation IIIF ». 2023. novembre 29. https://doc.biblissima.fr/formation-iiif/.
  - « Introduction à IIIF ». s. d. Documentation Biblissima. https://doc.biblissima.fr/iiif/introduction-iiif/.
  - « IIIF Online Workshop ». 2022. 2022. https://training.iiif.io/iiif-online-workshop/.
  - Robineau, Régis. (2020) 2021. Atelier IIIF DHNord2020. https://github.com/regisrob/Atelier_IIIF_Conference_DHNord_2020.
  - « IIIF Online Workshop ». 2020. septembre 2020. https://training.iiif.io/iiif-online-workshop/September2020.html#sessions.
  - Roddis, Tristan, Jeff Steward, et Richard Palmer. 2019. « Hands-on IIIF ». Workshop at Museums and the Web 2019. Boston, MA. Wednesday 3rd April 2019. Consulté le 12 mai 2019. https://docs.google.com/document/d/1QprIoyCDExcAz6_O6qMr67sYV4F5qsQZpw9ZuiKohs0/edit?usp=embed_facebook.
  - Introduction to IIIF - Tom Cramer, Stanford University. Réalisé par IIIF. 2018. https://www.youtube.com/watch?v=Z3ZgEv4p37o
  - Ronallo, Jason. 2018. « IIIF Technical Workshop [Code4Lib 2018, Washington DC, February 13, 2018] ». *ronallo.com*. http://ronallo.com/iiif-workshop-new/.

## Exemples d’intérêt

- [Accès iconographique de Biblissima+](https://portail.biblissima.fr/fr/iconography)
- [TU Delft Academic Heritage](https://delft-static-site-generator.netlify.app/en)
- [David Rumsey Map Collection - MapTab](https://chrome.google.com/webstore/detail/david-rumsey-map-collecti/fnheacjohhlddiffbmafmpoblbkfgmde?hl=en)
- [David Rumsey Map Collection](https://www.davidrumsey.com)
- [Dee mag](https://resources.digirati.com/iiif/an-introduction-to-iiif/dee-mag.html)
- [Démos Biblissima](https://demos.biblissima.fr)

## Applications logicielles

### Online curation with IIIF

- [Adno](https://adno.app/en/)
- [Annona, annotation library](https://ncsu-libraries.github.io/annona/)
- [Exhibit](https://exhibit.so)
- [Storiiies](http://storiiies.cogapp.com)
- [Range storyboard](https://ncsu-libraries.github.io/annona/range/)
- [IIIF Curation Platform](http://codh.rois.ac.jp/icp/index.html.en)
- [Wax](https://minicomp.github.io/wax/)
- [Juncture](https://juncture-digital.org)
- [Clover](https://samvera-labs.github.io/clover-iiif/docs/slider)
- [Canopee IIIF](https://canopy-iiif.vercel.app/)
- [Yith](https://yith.dev)

### Visionneuses IIIF

- [OpenSeadragon](https://openseadragon.github.io/)
    [OpenSeadragon API](https://openseadragon.github.io/docs/OpenSeadragon.html)
- [Universal Viewer](https://universalviewer.io/)
- [Mirador](https://projectmirador.org/) ou [Tify](https://tify.rocks)
- [Diva](https://diva.simssa.ca/) Canadien!
- [IIIF Curation Viewer](http://codh.rois.ac.jp/software/iiif-curation-viewer/)
- [Tify](https://tify.rocks) fondé sur OpenSeadragon

### Outils

- [Canvas Panel](https://canvas-panel.digirati.com)
CanvasPanel is a component that sits between tile renderers like OpenSeadragon (OSD) or Leaflet, and Manifest viewers like UV and  Mirador. It can be reused in very simple IIIF applications - a few lines of JavaScript - but is sophisticated enough to form the basis of custom applications with complex layout and annotation rendering requirements.
- [OSD, Tile-less IIIF from legacy image pyramid](https://tomcrane.github.io/scratch/osd/iiif-sizes.html)
- https://jbhoward-dublin.github.io/IIIF-imageManipulation/
- « Canvas-panel-cookbook ». s. d. Consulté le 27 mars 2022. https://canvas-panel.digirati.com/#/.
- Delft Static Site Generator. (2018) 2022. JavaScript. digirati-co-uk. https://github.com/digirati-co-uk/delft-static-site-generator.
- [IIIF-manifest-editor](https://github.com/digirati-co-uk/iiif-manifest-editor)
- « IIIF Manifest Editor ». s. d. Consulté le 27 mars 2022. https://digital.bodleian.ox.ac.uk/manifest-editor/#/?_k=cfbepm.
- Robson, Glen. (2015) 2022. SimpleAnnotationServer. JavaScript. https://github.com/glenrobson/SimpleAnnotationServer.
- National library of Norway ngx-mime https://github.com/NationalLibraryOfNorway/ngx-mime/
- 

### Validators                       

- [Image API validator](https://iiif.io/api/image/validator/) - Un service pour valider uen ressource IIIF Image API contre la spécification.
- [Presentation API validator](https://iiif.io/api/presentation/validator/service/) - Un service pour valider une ressource IIIF PresentatioN API contre la spécification.

## Divers

Identificants: 

- ressource
- folio
- extension de fichier
- manifest.json donne les informations sur la présentation du document
- info.json contient les dimensions

## Base

Présentation de Régis Robineau à [DH Nord 2020](https://projet.biblissima.fr/sites/default/files/atelier_iiif_dhnord_robineau_20201118.pdf)

- besoins communs p.16
- interopérabilité pour croiser les données issues de différents serveurs


Labo

- avoir un entrepôt IIIF pour l'ensemble de nos applications
- y connecter des outils qui facilient l'utilisation des images

Exemples: 

- [Heiji Monogatari Emaki (Tale of the Heiji Rebellion)](http://digital.princeton.edu/heijiscroll/scroll.html), Tom Conlan, Princeton library
- [Catalogue de la bibliothèque Princeton](https://catalog.princeton.edu/catalog/9981720703506421)

[Bodleinan Manifest Editor](https://digital.bodleian.ox.ac.uk/manifest-editor)

[Documentation de l'API IIIF Gallica](https://api.bnf.fr/fr/api-iiif-de-recuperation-des-images-de-gallica)

https://github.com/ProjectMirador/mirador

Identifiants

- ressource
- folio
- extension de fichier
- manifest.json donne les informations sur la présentation du document
- info.json contient les dimensions

###   Serveurs d’images

https://iiif.io/get-started/image-servers/

###   Visionneuses IIIF

https://iiif.io/get-started/iiif-viewers/

- OpenSeaDragon
- Mirador
- [mirador Integration](https://github.com/ProjectMirador/mirador-integration) (with react)
- [Diva](https://diva.simssa.ca/) Canadien!


Online curation with IIIF

- [Exhibit.so](https://www.exhibit.so/)
- [Range storyboard](https://ncsu-libraries.github.io/annona/range/)

### Autres

Exemple d’implémentation de l’API authentification Auth Demonstrator https://iiifauth.digtest.co.uk/

## Notes

[^1] White, Jon. 2017. « Innovatively repurposing content across multiple platforms ». *Medium*. 7 septembre. https://blog.cogapp.com/iiif-for-storytelling-1e36ce277f48.