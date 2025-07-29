# IIIF Use Cases

Des centaines d’acteurs impliqués au niveau mondial et une très large communauté d’utilisateurs tant dans le domaine des bibliothèques, des archives que des musées ou de la recherche.

Avec la présentation de trois cas d’usages, l’idée était de pouvoir examiner la manière dont à l’échelle d’une institution, il était possible de s’emparer de ces technologies. Voir comment certaines institutions ont su mettre à profit le protocole ainsi que les logiciels libres disponibles pour construire un ensemble de services intégrés.

Choix de trois institutions, pas nécessairement représentatives du monde muséal, mais qui se distinguent par leur utilisation intensive du protocole d’interopérabilité des images et souvent par leur rôle pionnier dans le développement de l’initiative IIIF.

- Princeton
- Bnf
- ...



## Princeton

### Sites

Digital PUL https://dpul.princeton.edu

https://library.princeton.edu/

vidéo sur la bib https://library.princeton.edu/about

GitHub https://github.com/pulibrary

### Acteurs

Jon Stroop https://orcid.org/0000-0002-0367-1243

https://library.princeton.edu/staff/jstroop

https://github.com/jpstroop

- 2007-2015 – Digital Initiatives Developer, Metadata Analyst
- 2015-2017 – Systems Application Development Manager (Library)
- 2017-2021 – Director of library IT and Digital Services (Library)
- 2021 – Deputy Dean of Libraries (Library)

### Index of Christian Art

2014

https://fr.slideshare.net/slideshow/iiif-for-index-of-christian-art/37063843

### Exposition

2014, Scrolls illustrating a story about the Sagami River, Kyoto [1660?-1670?]. Princeton University Library

https://blogs.princeton.edu/manuscripts/2014/09/22/japanese-scrolls-digitized/

https://catalog.princeton.edu/catalog/9981720703506421#view

Numérisation de trois rouleaux illustrés japonais du 17e. Histoire de la rivière Sagami, anonymes. 18 illustrations. Probablement une commande d’un seigneur de la guerre. Dos en soie pour l’un des rouleaux et décor doré. Dans une boite en laque contemporaine et rouleau autour d’un noyau en ivoire tourné.

- faciliter la consultation grace au zoom et multi tuiles pour expérience de zoom slippy.
- acces accru à un original dont la consultation était limitée pour des raisons de conservation

### Princeton University Art Museum

Princeton University Art Museum IIIF Use Cases, by Cathryn Goodwin - College Art Association 2018 conference

https://fr.slideshare.net/slideshow/princeton-university-art-museum-iiif-use-cases-by-cathryn-goodwin-college-art-association-2018-conference/90099324

Clarence H. White and his World, The arts and crafts of Photography, 1895-1925

Ther Berlin Painter and his world

- Luna Imaging, Luna and IIIF
- Artstor





## Stanford University

Michael keller

2015-2021
Founding member and Chairman, International Image Interoperability Framework (IIIF) Consortium

> In 2002, Stanford Libraries collaborated with Cambridge University to digitize ancient, medieval, and early modern manuscripts in the Matthew Parker Library of Corpus Christi College. That project led Stanford Libraries’ to develop requirements for a digital environment for streaming images of manuscripts and other objects of scholarship and for teaching, resulting in the International Image Interoperability Framework and the Mirador “viewer”. He was inaugural chairman of the IIIF Consortium from 2015 to 2021.
>
> https://creativedestructionlab.com/mentors/michael-keller/

### Modèle sous-jascent, Shared Canvas

https://iiif.io/api/model/shared-canvas/1.0/

- Robert Sanderson, Los Alamos National Laboratory
- Benjamin Albritton, Stanford University

Projet interne mai 2012, version 1.0 en février 2013.

Projet développé à Stanford par le Digital Manuscript Technical Working Group (DMSTech,
Stanford, 2010-2013)

- réflexions et expérimentations autour de l’interopérabilité des manuscrits numérisés
- étude des cas complexes liés au manuscrit médiéval : défis en terme de modélisation
- élaboration du modèle de données *Shared Canvas*

2013 phase d’implémentation par les institutions partenaires. [http://www.shared-canvas.org](https://web.archive.org/web/20140214001519/http://www.shared-canvas.org/)

Digital Medieval Manuscripts Initiatives https://github.com/DMSTech

Financement de 2 ans Mellon Foundation

> Stanford University Library has received two years of funding from the Andrew W. Mellon Foundation to lay the foundation for a generalizable infrastructure for repositories of digital medieval manuscript facsimiles. This is a first step toward a truly interoperable environment that will benefit scholars and other users of digital medieval materials, and provide a cost-beneficial method for repositories to make their medieval materials available to the world.
> https://web.archive.org/web/20150906190021/https://lib.stanford.edu/dmm

Partenaires

- Stanford University
- Los Alamos National Laboratory
- Open Annotation Collaboration
- Mellon Foundation

#### Objet de la spécification

> The SharedCanvas data model specifies a linked data based approach for describing digital facsimiles of physical objects in a collaborative fashion. It is intended for use in the cultural heritage domain, although may be useful in other areas, and is designed around requirements derived from digitized text-bearing objects such as medieval manuscripts. Instances of the data model are consumed by rendering platforms in order to understand the relationships between the constituent text, image, audio or other resources. These resources are associated with an abstract Canvas, or parts thereof, via [Open Annotations](http://www.w3.org/community/openannotation/) and the Annotations are grouped and ordered in [OAI-ORE Aggregations](http://www.openarchives.org/ore/).

>Le modèle de données SharedCanvas spécifie **une approche basée sur les données liées pour décrire des fac-similés numériques d’objets physiques de manière collaborative**. Il est destiné à être utilisé dans le **domaine du patrimoine culturel**, bien qu’il puisse être utile dans d’autres domaines, et est **conçu autour des exigences dérivées des objets numérisés contenant du texte**, tels que les manuscrits médiévaux. Les instances du modèle de données sont consommées par les **plates-formes de rendu** afin de comprendre les relations entre les textes, les images, les sons et les autres ressources qui les composent. Ces ressources sont associées à **un canevas abstrait**, ou à des parties de celui-ci, via [Open Annotations](http://www.w3.org/community/openannotation/) et les annotations sont regroupées et ordonnées dans [OAI-ORE Aggregations](http://www.openarchives.org/ore/).

#### Cas d’usage

- Existence de nombreuses collections numérisées. Identifie deux missions numérisation et accès numérique. 
- Pointe l’intérêt qu’il pourrait y avoir à disposer d’un modèle de données et de mise en œuvre partagé pour faciliter la création d’envrionnement logiciels pour consommer ce modèle.
- Reconnaissance que les référentiels peuvent être distribués plutôt que conservés dans un seul référentiels contenant toute les informations.

> **L’objectif du modèle de données Shared Canvas est de fournir une description normalisée des ressources numériques qui sont des substituts d’objets physiques culturellement importants, principalement textuels, afin de permettre l’interopérabilité entre les référentiels, les outils, les services et les systèmes de présentation.** La ressource modélisée est donc un seul élément physique (un livre, un manuscrit, une peinture) plutôt que l’œuvre intellectuelle qui y est incarnée (le texte ou tout autre contenu). Les exigences de modélisation sont tirées uniquement de cas d’utilisation des systèmes de présentation, et le modèle de données ne tente pas d’inclure des métadonnées descriptives sur le travail intellectuel autres que celles qui sont nécessaires pour afficher à l’utilisateur en tant que contexte immédiat dans une interface utilisateur.

Idée de pouvoir mutualiser les applications de base pour les environnements de visualisation. Réutilisations possible et interopérabilité transparente entre les référentiels qui peuvent contenir du contenu connexe ou même des pages physiques retirées de leur contexte d’origine.

Adoption des principes des données ouvertes et liées et de l’architecture du World wide web.

Reconnaissance de l’importance de la création, de la gestion et de la propriété de cette infromation distribuée.

#### Le modèle de données

La spécification décrit donc **un modèle de données fondée sur un Linked Data Canvas, un espace abstrait qui représente une page de l’élément numérisé, qui porte des ressources figurées de manière distribuée via des Annotations.** 

- Le Canvas reçoit un identifiant sous la forme d’un URI HTTP ce qui permet de lui associer des informations supplémentaires par n’importe quel utilisateur. 
- Les environnements de rendus pouvant déterminer ou non de conserver ces informations pour la présentation à un public donné.
- L’Annotation est liée à la ressource annotée qui est le Canvas et le commentaire est la ressource à afficher. Ces annotations peuvent être rassemblées n’importe où dans des agrégatons pour en faciliter la consommation.

#### Modèle de Canvas

> **Un *Shared Canvas* est un espace rectangulaire bidimensionnel avec un rapport d’aspect qui représente une seule vue logique d’une partie de l’élément physique.** Par exemple, un livre aurait une toile par côté d’une page, une peinture aurait une seule toile et un rouleau pourrait avoir soit une très longue toile représentant l’objet entier, soit plusieurs plus petites s’il était plus logique de le voir en sections.

Le point unique qui peut collecter et mettre en page plusieurs ressources de contenu qui forment un fac-similé.

- une seule page physique peut être représentée dans plusieurs numérisations de différentes qualités (éclairage, format, etc.) alors le Canvas est le point unique où ces images sont alignées
- l’image peut contenir plus que la page et donc une partie de l’image doit être alignée sur l’ensemble du canvas
- modéliser les pages pas encore nuémrisées mais sur lesquelles les informations sont connues (pages perdues, détruites ou hypothétiques qui auraient pu être transcrites avant la perte)

##### Canvas

> **Un Canvas est la substitution numérique d’une page physique qui doit être rendue à l’utilisateur.** Chaque toile a un rapport d’aspect rectangulaire et est positionnée de telle sorte que le coin supérieur gauche de la toile correspond au coin supérieur gauche d’une boîte de délimitation rectangulaire autour de la page, et de la même manière pour les coins inférieurs à droite. L’identifiant de la toile n’est pas un identifiant de la page physique, il identifie sa représentation numérique.

![Schéma du Canvas dans Shared Canvas](https://iiif.io/api/model/shared-canvas/1.0/images/canvasToPage.png)

Les propriétés du Canvas peuvent être exprimées grace à un modèle sémantique. 

##### Zones

Dans un Canvas, il est également possible de délimiter des *Zones*. Des informations pouvant être associées à la ressource Zone afin de manipuler toutes ces ressources dans un seul ensemble pour pouvoir générer des fonctionnalités d’interface utilisateur dynamique telles que la manipulation des plis dans un morceau de papier ou la rotation d’une section de la page pour faciliter la lecture.

![Schéma des Zones dans Shared Canvas](https://iiif.io/api/model/shared-canvas/1.0/images/zone-eg.png)

##### Annotations

Le modèle est conçu pour permettre l’association distribuée des ressources de contenu telles que les images et le texte avec le Canvas. Ainsi une institution peut fournir des images et une autre le texte transcrit, et un troisième un commentaire scientifique sur la page représentée.

Pour ce faire, on utilise un paradigme d’annotation qui permet de modéliser cette assocation, pour la transcription mais aussi pour toute ressource de contenu qui devrait être rendue dans le cadre du fac-similé numérique de la page. Shared Canvas utilise le modèle d’annotation ouverte du W3C [Open Web Annotation](http://www.openannotation.org/spec/core/).

![Schéma des annotations dans Shared Canvas](https://iiif.io/api/model/shared-canvas/1.0/images/canvasAnnoPage.png) 

##### Motivations d’un Canvas

Le modèle définit une nouvelle instance de `oa:Motivation` appelée `sc:painting` qui permet à un client de facilement distinguer les annotations qui doivent être rendues comme faisant partie du facimilé des autres annotations.

##### Mmodèle de Commande

Si un seul Canvas peut être utilisé pour rendre un côté d’une page ou d’un journal ouvert, plusieurs Canvas sont parfois nécessaires pour représenter un objet numérique comme un livre et pouvoir créer une applicationd e feuilletage.

Dans ce cas, l’ordre dans lequel les Canvas s’avère crucial. Dans le modèle de graphe RDF, cet ordre doit être décrit de manière explicite. Pour ce faire Shared Canvas fournit un modèle d’agrégation des données et de représentation des séquences ordonnées.

[Open Archives Initiative Object Reuse and Exchange (OAI-ORE)](http://www.openarchives.org/ore/)

### Spécifications IIIF

Plusieurs acteurs se regroupent à partir d’une réflexion commune sur un mécanisme d’échange des images entre entrepôts numériques, pour donner naissance à l’initiative IIIF.

Premiers partenaires : BnF, BL, Conell, Los Alamos National Laboratory, NL of Norway, Oxford, Stanford)

Publication d’un premier brouillon de l’API Image en 2012.

Editeurs de International Image Interoperability Framework : Image API 1, 17 septembre 2013

- Stuart Snydman, Stanford University
- Simeon Warner, Cornell University
- Robert Sanderson, Los Alamos National Laboratory
- Jon Stoop, Princeton University

+ auteurs de plusieurs institutions.

IIIF Metadata API, versioN 1.0, 16 septembre 2013

- Robert Sanderson,
- Ben Albritton, Stanford University
- Markus Enders, British Library

Premiers adopteurs : ARTstor, Biblissima, Bodleian Libraries, British Library, eCodices Electronici Sangallenses, Harvard University, Johns Hopkins University, Los Alamos National Laboratory, Stanford University, Yale University

Cas d’usage présentant

- intégration logicielle de pratiques savantes sur les ms
- agrégation divers manuscrits
- production d’éditions critiques numériques
- images multispectales
- citation extraits pour argument
- segmentation ms pour analyse visuelle (paléographie)
- annotation d’images

Annonce de Mirador 1

- espace de transcription
- représentation de texte multiple
- partage de workspace
- intégration d’autres médias



### Visionneuse Mirador

Modèle SharedCanvas pour objectif de pouvoir créer des visualiseurs standardisés. Dès le début du projet, développement d’un premier prototype : https://web.archive.org/web/20131104180440/http://www.shared-canvas.org/impl/

DMS Tech Group

https://projectmirador.org

>Open-source, web based, multi-window image viewing platform with the ability to zoom, display, compare and annotate images from around the world.

Mirador est un visualiseur qui permet de présenter dans une interface unifiée des documents provenants de différentes collections numérisées compatible avec les standards IIIF.

Le logiciel propose différentes fonctionnalités permettant de zoomer, de comparer ou d’annoter des images haute-résolutions.

Les images affichées dans l’interface ainsi que les métaodonnées ne quittent pas leur dépôt initial. Les institutions gardent dont le contrôle sur ce qu’elles souhaitent partager.

Mise en pratique de l’interopérabilité avec une visionneuse multi-fenêtre qui permet d’afficher des contenus stockés dans différents répertoires (Snydman et al. 2013).

### Exposition

Ōmi Kuni-ezu -- 近江國絵圖, Japan, 1837 (345 x 504 cm). Stanford University Libraries

https://purl.stanford.edu/hs631zg4177

### Machine Learning

https://stanford.edu/group/texttechnologies/cgi-bin/globalcurrents/galleries/ln.html

https://globalcurrents.stanford.edu

### Mise

An exploratory-stage application aimed at curators, students, and scholars, Mise provides a collaborative environment for annotation-oriented projects using the Mirador IIIF viewer.

https://mise.stanford.edu

### Exhibits

https://exhibits.stanford.edu/exhibits-documentation/about/iiif-introduction

### Bibliothèques

https://library.stanford.edu/iiif

Implémentation de la recherche

https://searchworks.stanford.edu/catalog?f%5Biiif_resources%5D%5B%5D=available

### Parker Library at Corpus Christi College, Cambridge

https://parker.stanford.edu/parker/

Divers 

> Benjamin Albritton is Associate Curator for Paleography and Digital Medieval Materials and is the Digital Manuscripts Program Manager at Stanford University Libraries. He oversees a number of digital manuscript projects, including [Parker Library on the Web](https://parker.stanford.edu/parker/), and projects devoted to interoperability and improving access to manuscript images for pedagogical and research purposes. His research interests include the intersection of words and music in the fourteenth century, primarily in the monophonic works of Guillaume de Machaut; the uses of digital medieval resources in scholarly communication; and transmission models in the later Middle Ages.

### From the page

https://content.fromthepage.com/stanford-university-archives/

https://fromthepage.com/stanforduniversityarchives/sail

## Bibliothèque nationale de France

La Bibliothèque nationale de France est membre fondateur du consortium IIIF (2015). Elle implémente dans Gallica, sa bibliothèque numérique, les API IIIF Images (version 1) et IIIF Presentation (version 2.0).

Ces développement sont initialement intervenus dans le cadre de la publication de ses bases de données de manuscrits numérisés (Mandragore) et de sa participation au projet Biblissima. Dans ce cadre, elle participe dès 2012-2013 aux rencontres ayant conduit à la spécification Shared Canvas.

La bibliothèque avait alors reçu depuis plusieurs années des financements de la fondation Andrew W. Mellon pour la numérisation de manuscrit.

Mandragore, une base iconographique pour les manuscrits de la Bnf

> Les collections de la Bibliothèque nationale de France abritent plusieurs dizaines de milliers de manuscrits dont le décor constitue l’un des plus riches musées de peinture au monde. La base Mandragore vous invite à l’explorer.

Base de données datant de 2003 (créée en 1989, mise en ligne en 2003, puis rénovée en 2022)

- Pas de possibilités de partage
- infrastructure existanctes par upgradable
- pas de modèled e sustanbilité

Interopérabilité entre répertoires

Nbx acteurs : Stanford Parker on the Web, Johns Hopkins, E-Codices, Gallica, BL, Bodelian, etc.

- TILE
- Biblissima, Liber 2013
- Biblissima (2012-2019), 7,1M

Projet Biblissima (Équipex 2012-2019), 7,1M.

Mandragore, échantillon ségmenté https://api.bnf.fr/fr/mandragore-echantillon-segmente-2019

### Mise en place d’identifiant ARK (Archival Resource Key)

À partir de 2006, évaluation des différents systèmes existants. Choix des ARK d’abord pour Gallica, puis l’ensemble des catalogues mais aussi SPAR (2010).

https://www.bnf.fr/fr/lidentifiant-ark-archival-resource-key

https://www.bnf.fr/fr/centre-d-aide/identifiants-internationaux

> ARK (*Archival Resource Key*) est un format d’**identifiant** créé en 2001 par la [*California Digital Library*](https://cdlib.org/) (CDL) qui a vocation à identifier des ressources de tous types – physiques (échantillons destinés à une expérience scientifique, produits éditoriaux, etc.), numériques (livres numérisés, notices de catalogue, etc.) ou même immatériels (concepts). Son but est de fournir des identifiants adaptés aux besoins des producteurs et diffuseurs de données sur le web, mais également capables de durer sur le long terme.

Il s’appuie sur les principes suivants

- Responsabilité d’une organisation dans la **permanence de l’accès** à ses ressources
- possibilité d’infléchir un ARK, c’est-à-dire de l’interroger par l’ajout d’un suffixe afin de fournir l’accès non seulement à la ressource mais également à ses **métadonnées**
- l’opacité de l’identifiant (ne changent pas)
- **la maîtrise** de tous les identifiants déjà publiés afin d’assurer leur **non-réattribution**.

Comme les DOI (Digital Object Identifier) les identifiants ARK sont des identifiants pérennes, à la différence que les DOI sont davantages issus du monde des éditeurs et du e-commerce, et sont fréquemment utilisés pour identifier des articles et des publications en ligne.

Pas d’autorité intermédiaire avec les ARK, il revient à chaque institution de définir sa propre politique et ses propres services, mais elle devra développer ou intégrer elle-même un système de gestion et de résolution d’identifiants.

Cependant, la CDL propose également un service payant, similaire à celui des agences d’enregistrement DOI, pour les identifiants ARK : le service [EZID](https://ezid.cdlib.org/).

Structure d’un ARK

![image](https://www.bnf.fr/sites/default/files/2018-12/nomARK.PNG)

- Qualificatifs de granularité (commençant par `/`)
- Qualificatifs de service (commençant par `.`)

![image](https://www.bnf.fr/sites/default/files/2018-12/qualificatifsARK.PNG)

Choix spécifiques de la Bnf pour l’implémetation des ARK https://multimedia-ext.bnf.fr/pdf/ark_preconisations_bnf.pdf

- Métadonnées minimales `?`
- Qualificatifs de granularité : `/f107`
- Qualificatifs de services : `.epub`, `.pdf`

ARK pouvant identifier tout type de ressource, le choix de celles devant recevoir un ARK est laissé aux autorités nommantes, selon les critères suivants :

- Quelles ressources doivent pouvoir être citées par mes utilisateurs ?
- Puis-je m’engager à maintenir la résolution de ces identifiants sur le long terme (c.-à-d. au-delà des changements techniques de plateforme de diffusion) ? Bien que des ARK puissent être attribués à des ressources dont la durée de vie est limitée, il est préférable de ne les attribuer qu’à des ressources que l’on souhaite pérenniser.
- En fonction des réponses ci-dessus, à quel(s) niveau(x) de granularité attribué-je un ARK ?
- Si j’attribue un ARK à différents niveaux de granularité, vais-je révéler la relation entre ceux-ci par le biais de qualificatifs de granularité ?
  Exemple : si l’on attribue un ARK à un livre et à chacun de ses chapitres, donne-t-on à ces derniers un nom ARK différent de celui du livre, ou utilise-t-on le nom ARK du livre suffixé par un qualificatif de granularité ?
- Si mes ressources identifiées par un ARK sont disponibles sous différentes formes, quels qualificatifs de service vais-je définir ?

**À retenir :** un ARK est un identifiant (le nom officiel de vos ressources, au même titre qu’une cote pour les documents physiques) avant d’être un **permalien**. Sa pérennité résidera dans votre capacité à gérer la ressource sur le long terme et son association avec la chaîne de caractères qui l’identifie.

En 2018, plus de 600 institutions dans le monde inscrites au [registre ARK](https://n2t.net/e/pub/naan_registry.txt). Princiaplement des Bibliothèques et Archives nationales.

- **des musées** : le musée des Augustins, les archives du musée Picasso, la Cité des Sciences et de l’Industrie, le musée d’Histoire naturelle de Toulouse, etc. ;

### Systématisation de IIIF sur Gallica

La première implémnetation de IIIF dans Gallica a été achevée en 2014. L’implémentation complète de l’API et des manifestes sur l’ensemble de la collection a été pleinement opérationnelle en avril 2016.

https://pro.europeana.eu/files/Europeana_Professional/Europeana_Network/Europeana_Network_Task_Forces/Final_reports/Preparing%20Europeana%20for%20IIIF%20involvemenet%20TF%20final%20report/report-on-iiif-task-force-2017-appendixd1.pdf

### Gallica.lol

https://gallica.lol

### Valorisation des APIs (2017)

https://api.bnf.fr

Adoption d’une licence ouverte pour l’ensemble des métadonnées en 2014.

Volonté de simplifier l’accès à ces données et de susciter de nouveaux usages (alimentation d’autres catalogues, créations d’applications innovantes, fouille de données et visualisation de données).

Diversification des publics (développeurs, entrepreneurs, chercheurs et digital humanist)

> **Le portail BnF API et jeux de données a ouvert le 23 novembre 2017 à l’occasion du deuxième hackathon BnF**. Il décrit et documente l’ensemble des API (*Application Programming Interface*, interface de programmation applicative) qui permettent d’interroger et de récupérer les métadonnées des catalogues et les collections numérisées de la BnF. Pour faciliter l’accès aux données et leur utilisation, des jeux de données (images et textes, métadonnées, statistiques) ont également été constitués et sont directement téléchargeables via le portail. Chaque API ou jeu de données y donne lieu à une présentation du contenu, une documentation technique, des précisions sur les droits d’utilisation et un accès direct aux données.

- Outils métiers (SRU, Z39.50, OAI-PMH)
- [data.bnf.fr](https://data.bnf.fr) et SPARQL endpoint (création de 2011 cf. https://data.bnf.fr/releases)
- Diverses APIs spécialisées
- Corpus documentaires

Rapport activité 2016

Utilisation IIIF en hausse. Les sites qui font le plus appels : europeana.eu, jessehurlbut.net, projectmirador.org et retronews.fr 

Rapport activité 2017

> les premiers développements pour la création d’un visualiseur IIIF3 dans Gallica ont été lancés. Ce visualiseur permettra de comparer des documents issus de plusieurs bibliothèques numériques dans une même interface ;
>
> API et jeux de données

Rapport activité 2019

- 2019, décide de faire évoluer son offre, récupération gratuirte HD
- GallicaSnoop et Classifcation d'images patrimoniales (CIP

>	 	 	  Deux équipes Inria ont travaillé sur des collections iconographiques extraites de Gallica et de Mandragore, via l’API IIIF : l’équipe Linkmedia a œuvré à la création de modèles de classifcation d’images dans le contexte des fonds Mandragore présentant une grande variabilité de formes et un faible volume d’images annotées ; l’équipe Zenith a utilisé la collection Gallica Images et les corpus de presse de GallicaPix pour enrichir le moteur d’indexation visuel SNOOP d’une fonctionnalité de recherche incrémentale pilotée par l’utilisateur. La recherche d’une solution de mutualisation de SNOOP au bénéfice des institutions patrimoniales a été discutée par la BnF avec le ministère de la Culture, fn 2019.
>	 	 	  https://www.bnf.fr/sites/default/files/2023-06/rapport_2019.pdf

## Expérimentations IA

Expérimentations à la Bnf au tournant 2017-2018 avec plusieurs prototypes qui ont permis d’identifier que l’utilisation de IIIF constitutait un accélérateur d’idées en permettant d’accéder directement aux images à partir d’URL en partant des entrepôts institutionnels ou en utilisant des outils commerciaux. 

À l’époque indexation d’images, aujourd’hui flux complets d’image ou sélectiond e corpus.

Ex. Projet [rara magnetica](https://www.raramagnetica.de), Early modern magnetism image. Idem pipeline de traitement de l’image. Chaîne de traitement orientée sur la partie textuelle et une bdd compatible IIIF permettant de revenir à al collection pour déployer une activité scientifique.

Pipeline qui s’appuie souvent sur des outils existants, ici comme transkribus, Viskus pour visualisation IIIF. De plus en plus les pipelines s’appuient sur des outils existants.

2023, Utilising IIIF and IIIF and knowledge Bases for searching people within historical newspaper. Recherche patronimes.

Facilite les fonctionnalités offertes aux utilisateurs. 

Mais

- Pression sur les serveursSi les corpus sont massif, éviter les API.
- traitement d’images, si enchaînement d’étapes dans le workflow = faire une copie locale
- traitement du texte et des données : transformer les JSON IIIF

**IIIF aussi boîte à outils**

- outils de transcription automatique, HTR et OCR : Transkribus, eScriptorium
- annotation : Mirado
- CMS pour les HN
- visualiseurs

**IIIF pour la dissémination des jeux de données et jeux de données enrichies**

Corpus et jeux de données

- IIIF comme format de production et d’échange pour les jeux de donnée d’entraînement
- les collections IIIF et les annotations sont utilisées pour décrire les données
- les formats spécialisés deep learnin peuvent être dérivés (COCO, [Pascal VOC](http://host.robots.ox.ac.uk/pascal/VOC/), ...)

[Visual contagions](https://www.unige.ch/visualcontagions/) où annotations partagées en IIIF. Conservation du travail dans un format classique du patrimoine

[NewsEye](https://www.newseye.eu) projet de presse quotidienne. Jeu de données. Accès au dataset et corpus.

[GallicaPix](https://gallicapix.bnf.fr/rest?run=findIllustrations-form.xq) précurseur de Gallica Images. une fois les objets annotés, va avoir envie de fournir ces nouvelles métadonnées appuyées d’outils de consultation. Mais aussi laisser les utilisateurs valoriser ces données. IIIF permet de porter ces annotations.





## Image cropper

https://portail.biblissima.fr/en/mirador?key=Vg5KDD1GMmFkADxkN2OE&version=4

https://gallica.bnf.fr/ark:/12148/btv1b531551881/f1.item.r=toulouse.zoom

https://jbhoward-dublin.github.io/IIIF-imageManipulation/index.html?imageID=https://iiif.ucd.ie/loris/ivrla:10408

Outil d’annotation embarqué dans Mirador (image NGA Washington)

http://lotb.iath.virginia.edu

## Delft TU

https://www.tudelft.nl/en/

TU Delft Library

https://observablehq.com/@tudelft



Travail avec Digirati https://github.com/digirati-co-uk/delft-static-site-generator

> Since 2017, when TU Delft celebrated its 175th anniversary, the university has been raising the profile of its academic heritage by systematically curating its collections, initiating research projects and organising on-campus presentations in collaboration with students and academic staff.

Generates static sites from IIIF Manifests

https://cultural-heritage.digirati.com/showcasing-collections/delft-university-of-technology-library/

2023, Dutch contribution to IIIF enables description of georeferenced maps

> Jules Schoonman and Bert Spaan, creators of the open source map tool Allmaps, have made a major contribution to the International Image Interoperability Framework (IIIF). They collaborated on an extension to describe georeferenced maps within IIIF. They also further improved Allmaps.
>
> https://www.tudelft.nl/en/2023/library/dutch-contribution-to-iiif-enables-description-of-georeferenced-maps
>

## Yale

<https://fr.slideshare.net/AAColaborative/iiif-and-mirador-at-the-ycba-image-based-scholarly-collaboration-and-research?_gl=1*e7qm7g*_gcl_au*MTg1MTY4MDMzLjE3MTY0NDg1NDE.>

https://www.nga.gov/audio-video/video/iiif.html

## Harvard ex

- 2010, bibliothèques de Harvard tracking IIIF
- 2012, focus group (faculty, tech, bib) pour options pour nouveau feuilletage
- 2012, 40M investissement edX et financement développeur IIIF
- 2012, « The Book: Histories Across Time and Space » début dev
- 2014, Harvard Library IIIF services pour 120 000 livres et ms = 5M pages + 10M images fixes
- 2015, « The Book » lancemecnt Art Museums IIIF manifest service pour 250 000 objets d’art
- 2016, lancement de trois applications utilisant Mirador : Harvard Library Viewer, Iamge Media Management LTI-Canvas app, Art museum digital tour builder

<https://fr.slideshare.net/slideshow/iiif-as-an-enabler-to-interoperability-within-a-single-institution/62439873?_gl=1*e7qm7g*_gcl_au*MTg1MTY4MDMzLjE3MTY0NDg1NDE.>

International Image Interoperability Framework https://iiif.harvard.edu

### Medieval scrolls

https://www.edx.org/learn/literature/harvard-university-the-book-scrolls-in-the-age-of-the-book

https://digitalhumanities.fas.harvard.edu/project/medieval-scrolls/

### Remarque

Sanderson donne informations historiques sur la conception de IIIF

https://www.nga.gov/audio-video/video/iiif/iiif-sanderson-7.html

Explique responsable du standards du W3C sur l’annotation web. Un des deux co-chair du groupe de travail du W3C sur les annotations web qui est issu d’un community group au cours des trois dernières années (2016). Issu d’un projet financé par la fondation Mellon : Open annotation collaboration. Alors que à Los Alamos labs, entendu parlé du travail mené par Tom et co. En fait, quelques années avant étape de planifcation. Ma thèse sur les manuscrits médiévaux. Alors parfait orage arose ms médiévaux, annotations, images, linked open data. Les a mis ensemble et fait une belle sculpture, donne IIIF.

11 décembre 2014, premier brouillon annotation. Très proche car pris en charge.

Trianon

https://medium.com/digirati-ch/iiif-manifest-editor-commentary-on-first-round-of-user-group-feedback-eb30cd252157
