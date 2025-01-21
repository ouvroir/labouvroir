---
title: "Documenter les accrochages d’exposition ou de collection muséales : une approche ontologique"
description: "Article sur le développement de l'ontologie Display" #desc
author: [davvalent, ZoeRenaudie, emchateau]  #username
date: 2025-01-21 #date [YYYY]-[MM]-[DD]
draft: false
lang: fr #lang [en ou fr]
tags: [Display, ontologie]

---

# **Documenter les accrochages d'expositions et de collections : une approche ontologique**

La recherche historique sur les expositions nécessite la mobilisation et l’exploitation d’une documentation archivistique étendue pour fournir des informations sur l’histoire des accrochages de collections dans les musées d’art. La reconstruction des accrochages d'exposition est cependant semée de difficultés pratiques et méthodologiques, notamment en raison du caractère partiel des documents conservés et de la nécessité de traiter des sources d'information hétérogènes (vues d'exposition, listes de prêts, plans des salles d'exposition, projets expographiques ou scénographiques). Ce processus peut néanmoins bénéficier grandement d'une approche numérique exploitant la modélisation tridimensionnelle.

Le partenariat *Nouveaux usages des collections dans les musées d’art* (CIÉCO, https://www.cieco.co) réunit une équipe d’une vingtaine de chercheurs, son laboratoire *L’Ouvroir d’histoire de l’art et de muséologie numériques* (https://ouvoir.umontreal.ca) et six musées d’art canadiens. Dans ce cadre, notre collègue Marie Fraser s’intéresse à l’histoire des accrochages de collections. Pour soutenir ce travail, notre équipe cherche à développer des processus de documentation et de visualisation conçus à la fois pour garantir la durabilité et la conservation d’un patrimoine documentaire sur les expositions, et pour exploiter ce matériau sous-utilisé par les musées dans divers contextes numériques.

Depuis les années 1990, les institutions culturelles ont élaboré plusieurs modèles de documentation pour rendre compte des informations muséales. Le modèle conceptuel de référence développé par le groupe de documentation de l’ICOM, CIDOC, offre par exemple une ontologie générique, orientée événement, pour décrire la vie des objets culturels. Des travaux ont également porté sur la provenance et, plus récemment, sur la documentation des expositions. Mais à ce jour, il n’existe pas de modèle spécialisé pour la documentation des accrochages d’expositions ou de collections.

Nous faisons l’hypothèse que l’utilisation d’un modèle de documentation exprimé sous forme d’ontologie computationnelle en OWL, indépendant de toute technologie de visualisation *a priori*, présente l’avantage de pouvoir raisonner sur les données d’une manière qui garantit leur préservation à long terme, tout en permettant toutes sortes de réutilisations. Après avoir présenté le point de vue spatial que nous adoptons à l’égard des expositions, nous introduirons les éléments structurants de cette ontologie, puis nous présenterons un premier cas d’usage.

## **1. Une perspective spatiale sur l’exposition**

### La 3D pour la reconstruction

Bien que nous préférions utiliser une modélisation abstraite plutôt qu’une modélisation en 3D, ce projet adopte une perspective spatiale à l’égard des expositions. La connaissance historique des accrochages de collections peut bien sûr bénéficier de visualisations sous forme de modèles 3D. Depuis quelques années, plusieurs musées proposent des visites virtuelles ou en réalité augmentée de leurs expositions (MOCA, MoMA, etc.). Le musée Städel, par exemple, présente une reconstruction 3D de l’une de ses galeries historiques (http://zeitreise.staedelmuseum.de/vr-app/). Si l’intérêt de ces approches est bien justifié d’un point de vue médiationnel, ces artefacts numériques soulèvent de sérieux problèmes de recherche, notamment en termes d’obsolescence technique, de conservation et d’interprétation.

Créer des modèles 3D pose des défis significatifs, notamment pour documenter les incertitudes et les processus ayant permis d’établir des connaissances historiques. Les archéologues ont développé diverses méthodologies et réflexions qui peuvent être utiles pour relever ces défis, en particulier dans le domaine de la modélisation et de leur valeur probante, comme dans le cas de l’anastylose numérique.

### Du modèle documentaire à la visualisation

À l’instar de l’archéologie, l’étude des expositions peut bénéficier d’approches spatiales ou tridimensionnelles pour formuler des hypothèses ou proposer des reconstructions basées sur une documentation incomplète. Cependant, les sources utilisées pour examiner les accrochages d’expositions d’art diffèrent sensiblement de celles employées en architecture et en archéologie. Les sources archivistiques et visuelles sont plus cruciales pour reconstruire les accrochages. De plus, le domaine muséologique ne peut s’appuyer sur les logiques constructives souvent essentielles pour guider les reconstructions, qui justifient largement l’utilisation de logiciels de dessin architectural en 3D.

Un outil conçu pour faciliter la reconstruction des accrochages d’expositions d’art doit soutenir l’ensemble du processus de recherche, depuis la collecte d’informations historiques et la formulation d’hypothèses jusqu’à la génération de reconstructions 3D. Notre solution implique la création d’un modèle indépendant de toute technologie de visualisation spécifique, garantissant la durabilité et la préservation à long terme des données enregistrées. En adoptant une approche formelle et en créant une ontologie OWL, nous intégrons notre travail dans un cadre méthodologique robuste qui répond aux enjeux posés par la nature de la documentation historique disponible, tels que les lacunes et incertitudes, tout en visant la réutilisation, la durabilité et l’interopérabilité des données. Cette application, que nous développons actuellement, exploite la logique spatiale pour soutenir le travail des chercheurs.

## **2. L’ontologie Display**

L’ontologie Display définit un ensemble de classes et de propriétés pour décrire les expositions. Elle adopte une perspective expographique basée sur le concept d’élément d’exposition (*exhibit*), mobilisant principalement une logique spatiale impliquant la capacité à définir des relations topologiques entre les éléments d’exposition et les espaces d’exposition.

Dans cette optique, nous adoptons un point de vue particulier sur l’exposition, en ce sens que :

- tout se passe dans des espaces expographiques ;
- tous les objets situés dans de tels espaces sont des éléments d’exposition.

### **Création d’une classe Exhibit pour les éléments d’exposition**

La classe `display:Exhibit` regroupe les éléments impliqués dans une exposition, indépendamment de leurs caractéristiques artistiques, esthétiques ou techniques, à travers les relations topologiques qu’ils entretiennent les uns avec les autres au sein d’un espace d’exposition.

### **Réutilisation de l’ontologie BOT**

Lors de la création d’une nouvelle ontologie, il est recommandé d’identifier et de réutiliser les modèles existants lorsque cela est possible. Cette approche repose sur l’hypothèse que ces modèles partagent un cadre conceptuel similaire. Pour décrire les espaces d’exposition, nous avons examiné les ontologies architecturales. L’utilisation accrue d’outils numériques dans la modélisation des informations sur les bâtiments (BIM) a récemment conduit au développement de nombreux cadres ontologiques.

Développée récemment dans le cadre d’un groupe communautaire du W3C, l’ontologie Building Topology Ontology (BOT) propose une ontologie minimale pour définir les relations entre les sous-composants d’un bâtiment, répondant bien à nos besoins.

Cette ontologie définit l’existence de zones (telles que site, bâtiment, étage et espace) avec des étendues tridimensionnelles, applicables dans des contextes réels comme virtuels. Ces zones peuvent être reliées entre elles de manière mérologique, à l’image des poupées russes.

Ainsi, le modèle peut décrire efficacement la relation entre un élément d’exposition et un espace dans un contexte d’exposition. Sa simplicité permet une extensibilité significative, que nous avons exploitée pour développer l’ontologie Display.

Cependant, l’ontologie BOT se limite à la description des relations d’adjacence, de partition et d’intersection, sans fournir de cadre générique pour les relations topologiques. Nous avons donc dû chercher des solutions ailleurs.

### Stratégies de liaison avec BOT

L’alignement ontologique a été conçu pour permettre l’application des propriétés topologiques de BOT à la description des œuvres exposées et l’application des propriétés topologiques de Display aux éléments du bâtiment. Cet alignement s’opère de quatre manières.

Tout d’abord, deux spécialisations ont été créées pour gérer les espaces d’exposition :

1. La classe `bot:Space` est spécialisée par une sous-classe `display:ExhibitionSpace`, destinée à décrire les espaces d’exposition et héritant des propriétés pour les relations mérologiques génériques.
2. La propriété `bot:hasSpace` est spécialisée par une sous-propriété `display:hasExhibitionSpace`.

Ensuite, une relation d’équivalence de classe a été établie pour créer deux classes parallèles, `bot:Element` et `display:Element`, permettant de partager des relations topologiques et mérologiques au niveau du modèle.

Enfin, la spécialisation `bot:Interface` a été conçue pour préciser les propriétés des relations non topologiques entre les espaces ou entre les espaces et les éléments.

### **Support pour les relations topologiques**

L’ontologie utilise des propriétés de haut niveau, reflétant le modèle BOT, pour définir les relations topologiques des espaces et des éléments du bâtiment. ➜ topo Alors que BOT définit ces propriétés au niveau des éléments du bâtiment (`bot:hasElement`), Display les définit au niveau des œuvres exposées (`display:hasExhibit`).

Un espace abstrait peut être lié à une œuvre exposée via la propriété `display:containsExhibit`, lorsqu’il est considéré comme une œuvre, ou via la propriété `bot:containsElement`, s’il est considéré comme un élément de bâtiment. Les éléments de bâtiment, définis par `bot:Element` ou `display:Element`, sont toujours qualifiés comme œuvres grâce à l’équivalence des classes.

De plus, des super-propriétés (`display:hasTopologicalRelationWith`) sont définies pour permettre l’organisation hiérarchique des relations topologiques dans les expositions. Cette hiérarchie distingue entre les relations proximales et spatiales. Différents types d’œuvres, en tant que sous-classes de `display:Exhibit`, hériteront de toutes ces propriétés par héritage de classe, bien qu’elles ne soient pas encore mises en œuvre.

### **Lien avec CIDOC et autres ontologies patrimoniales**

Display privilégie une perspective spatiale, contrastant avec l’approche centrée sur les événements du modèle conceptuel CIDOC. L’extension CRMarcheo traite efficacement la stratigraphie à travers des entités temporelles, reflétant des événements dans le temps. Cependant, modéliser les relations spatiales dans une exposition selon le modèle CIDOC serait trop complexe en termes de notation et d’application.

Néanmoins, décrire les expositions à l’aide de CIDOC-CRM reste essentiel en raison de sa prévalence dans les musées et les domaines patrimoniaux. Pour combler cet écart, nous proposons de lier l’ontologie Display à CIDOC-CRM de la manière suivante :

1. Les œuvres exposées peuvent être des instances de la classe `E18_Physical_Thing`, permettant leur description à l’aide de CIDOC-CRM.
2. Les agrégats d’œuvres au sein de la classe `display:Display` peuvent être des instances de `E78_Curated_Holding`, représentant les résultats des activités décrites à l’aide de CIDOC.

Cette proposition est ouverte à discussion avec la communauté muséale.

## **3. Présentation du modèle avec cas d’utilisation**

Pour tester l’ontologie Display, nous l’avons appliquée pour décrire l’exposition *Feux pâles* de Philippe Thomas, organisée au CAPC de Bordeaux en 1990. Cette exposition, qui fonctionne comme une installation, est bien documentée grâce aux archives et aux recherches menées par Zoë Renaudie dans le cadre d’un Master en conservation-restauration.

Il suffit de peupler la classe `display:Exhibit` pour indiquer la présence d’un objet exposé dans l’exposition. Par exemple, on peut facilement déclarer que l’œuvre *CAPC*, un code-barres accueillant les visiteurs, est suspendue sur le mur d’exposition de l’entrée. La classe `bot:Interface` est utilisée pour détailler l’accrochage, en précisant la relation entre le mur d’exposition et l’œuvre.

La description des espaces utilise les classes et propriétés du vocabulaire `bot`. La connectivité des espaces d’exposition peut être décrite grâce à l’une des trois propriétés fondamentales : `bot:adjacentZone`, `bot:intersectsZone` et `bot:containsZone`, ainsi que la propriété spécialisée `display:hasExhibitionSpace`.

L’espace d’entrée est relié à la première salle via deux passages.

Ce cas d’utilisation est particulièrement intéressant en raison de la complexité de l’espace. L’exposition est installée dans un espace existant reconfiguré à l’aide de panneaux muraux et de murs d’exposition, créant différentes salles qui communiquent entre elles par plusieurs passages. L’ontologie permet de décrire l’organisation spatiale de diverses manières : en utilisant des interfaces de circulation, en décrivant les intersections volumétriques ou en déclarant des relations mérologiques.

Dans des cas spécifiques, l’emplacement des œuvres peut également être décrit en utilisant des intersections. Par exemple, l’emplacement de l’œuvre *Parcelle à céder*, un parquet traversant les salles intitulées *De la propriété littéraire et artistique* et *Mesure pour mesure*, peut être spécifié avec deux déclarations utilisant la propriété `display:intersectingExhibit`.

**Exemple de relations topologiques entre les œuvres :**

L’agencement des œuvres dans l’espace peut être précisé en cartographiant les relations topologiques entre elles. Dans la salle intitulée *Le cabinet d’amateur*, les deux Janssens sont accrochés l’un en face de l’autre, décrit par une propriété symétrique (`display:faces`).

**Cas particulier des objets dans la vitrine :**

Tout comme pour les espaces, les œuvres peuvent être contenues dans d’autres éléments de l’exposition. Par exemple, toutes les œuvres situées dans les vitrines de la salle *Inventaire du mémorable* peuvent être décrites comme incluses dans cette vitrine. Les bustes positionnés de chaque côté de cette vitrine sont décrits comme étant à sa droite et à sa gauche, permettant ainsi de conclure que la vitrine est placée entre ces deux éléments.

### Inférences topologiques

L’utilisation d’un modèle ontologique permet de tirer parti des logiques descriptives pour déduire de nouveaux faits à partir de données existantes. Par exemple, à partir d’un ensemble initial de déclarations topologiques, plusieurs relations, représentées par des lignes en pointillé, peuvent être déduites.

Cette capacité est particulièrement précieuse, étant donné la nature souvent incomplète ou complémentaire des sources documentaires dans les recherches historiques. L’ontologie Display exploite pleinement les sémantiques OWL, permettant l’expression de la symétrie, de la transitivité et la déclaration de chaînes de propriétés.

## **Conclusion**

Le cas d’usage que nous avons présenté démontre que l’ontologie développée dans le cadre de ce projet permet de décrire avec précision des phénomènes curatoriaux complexes et offre une expressivité suffisante pour exploiter le modèle ontologique via des inférences. Le domaine d’application de l’ontologie Display est particulièrement adapté à un modèle ontologique. Les relations spatiales entre les œuvres exposées et les espaces d’exposition se prêtent particulièrement bien à une description basée sur la logique de second ordre utilisée par OWL.

La réutilisation du noyau de l’ontologie BOT nous a permis de développer un modèle concis, flexible et polyvalent.

L’ontologie se compose principalement de trois classes dérivées de BOT et de deux sous-classes spécifiques définies dans le namespace Display. Cinq propriétés suffisent à décrire les relations spatiales entre les œuvres et les espaces, complétées par un ensemble d’une vingtaine de propriétés topologiques et mérologiques. L’alignement entre BOT et Display permet d’appliquer les propriétés de l’ontologie BOT aux œuvres exposées.

D’autres travaux ontologiques se sont intéressés aux expositions artistiques, mais sans prendre en compte la dimension spatiale de leur présentation. En mettant l’accent sur la configuration expographique, la perspective ontologique adoptée pour Display délaisse partiellement l’usage de CIDOC-CRM, qui peut encore être utilisé pour décrire une œuvre ou une exposition en tant qu’événement. Cette approche aboutit à un modèle plus concis et convivial. La nature directe de la description vise à servir de base pour le développement d’une application informatique permettant l’acquisition de données d’archives et la production de visualisations tridimensionnelles.

Les technologies du web sémantique fournissent ainsi un modèle abstrait permettant de raisonner efficacement à partir d’une documentation parfois incomplète et contradictoire.