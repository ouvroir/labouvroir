---
title: "Documenting exhibition and collection displays: an ontological approach"
description: "Paper on the Display Project" #desc
author: [davvalent, ZoeRenaudie, emchateau]  #username
date: 2025-01-21 #date [YYYY]-[MM]-[DD]
draft: false
lang: en #lang [en ou fr]
tags: [Display, ontology]

---

# **Documenting exhibition and collection displays: an ontological approach**

Historical research on exhibitions requires the mobilization and exploitation of extensive archival documentation to provide information on the history of collection hangings in art museums. While the reconstruction of exhibition displays is fraught with practical and methodological difficulties, due in particular to the partiality of the documentation preserved and the need to deal with heterogeneous sources of information (exhibition views, loan lists, exhibition room plans, expographic or scenographic projects), this process can greatly benefit from a digital approach that takes advantage of three-dimensional modeling.

The partnership *New uses of collections in art museums* (CIÉCO https://www.cieco.co) brings together a team of some twenty researchers, its laboratory *L’Ouvroir d’histoire de l’art et de muséologie numériques* (https://ouvoir.umontreal.ca) and six Canadian art museums. Within this project, our colleague Marie Fraser is interested in the history of collection displays. To support this work, our team is seeking to develop documentation and visualization processes designed both to ensure the durability and conservation of a documentary heritage on exhibitions, and to use this under-exploited material by museums in different digital contexts. 

Since the 90s, cultural institutions have developed a number of documentation models to account for museum information. The conceptual reference model developed by ICOM’s documentation group, CIDOC, for example, offers a generic, event-oriented ontology for describing the life of cultural objects. Work has also been carried out on provenance and, more recently, on exhibition documentation. But to date, there is no specialized model for the documentation of exhibition or collection displays.

We hypothesize that the use of a documentation model expressed as a computational ontology in OWL, independent of any *a priori* visualization technology, has the advantage of being able to reason about data in a way that guarantees its long-term preservation, while allowing for all kinds of reuse. After presenting the spatial point of view we adopt with regard to the exhibition, we will introduce the structuring elements of this ontology and then present a first use case.

## **1. A spatial perspective on the exhibition**

### 3D for reconstruction

Although we prefer to use abstract modeling rather than 3D modeling, this project adopts a spatial perspective with regard to the exhibition. Historical knowledge of collection hangings can of course benefit from visualization in the form of 3D visualisation. For some years now, several museums have been offering virtual or augmented reality tours of their exhibitions (MOCA, MoMA, etc.). The Städel Museum, for example, presents a 3D reconstruction of one of its historic galleries (http://zeitreise.staedelmuseum.de/vr-app/). While the interest of these approaches is well justified from a mediation perspective, from a research point of view such digital artifacts raise serious problems of technical obsolescence and conservation, but also of interpretation.

Creating 3D models poses significant challenges, particularly in documenting uncertainties and the processes used to establish historical knowledge. Archaeologists have developed various methodologies and reflections that can be valuable in addressing these challenges, especially in terms of modeling and their evidential value, such as in the field of digital anastylosis.

### From documentary model to visualization

Similar to archaeology, the study of exhibitions can benefit from spatial or three-dimensional approaches to formulate hypotheses or propose reconstructions based on incomplete documentation. However, the sources used to examine art exhibition hangings differ significantly from those in architecture and archaeology. Archival and visual sources are more crucial for reconstructing displays. Additionally, the museological field cannot rely on the constructive logics often essential for guiding reconstructions, which largely justify the use of three-dimensional architectural drawing software.

A tool designed to facilitate the reconstruction of art exhibition hangings must support the entire research process, from gathering historical information and formulating hypotheses to generating 3D reconstructions. Our solution involves creating a model independent of any specific visualization technology, ensuring the durability and long-term preservation of the recorded data. By adopting a formal approach and creating an OWL ontology, we integrate our work into a robust methodological framework that addresses the issues posed by the nature of available historical documentation, such as gaps and uncertainties, while aiming for data reuse, durability, and interoperability. This application, which we are currently developing, leverages spatial logic to support researchers’ work.

## **2. The Display ontology**

The Display ontology defines a set of classes and properties for describing exhibitions.  It adopts an expographic perspective based on the concept of exhibit, mobilizing mainly a spatial logic that implies being able to define topological relationships between exhibit and exhibition spaces.

In this respect, we adopt a particular point of view on the exhibition, in the sense that:

- everything takes place in expographic spaces
- all objects located in such spaces are exhibits

### **Creating an Exhibit class for exhibits**

The `display:Exhibit` class is used to bring together elements involved in an exhibition, regardless of their artistic, aesthetic or technical characteristics, through the topological relationships they have with each other within an exhibition space.

### **Reusing the BOT ontology**

When creating a new ontology, it is best practice to identify and reuse existing models whenever possible. This approach relies on the assumption that these models share a similar conceptual framework. In describing exhibition spaces, we examined architectural ontologies. Recently, the extensive use of IT tools in Building Information Modeling (BIM) has driven the development of numerous ontological frameworks.

Recently developed as part of a W3C community group, The Building Topology Ontology (BOT) proposes a minimal ontology for defining the relationships between building's subcomponents, aligning well with our requirements.

This ontology defines the existence of zones (such as site, building, floor, and space) with three-dimensional extents, applicable in both real and virtual contexts. These zones can be related to each other in a mereological manner, similar to Russian dolls.

Thus, the model can effectively describe the relationship between exhibit and space within an exhibition context. Its simplicity allows for significant extensibility, which we leveraged to develop the Display ontology.

However, the BOT ontology is limited to the description of adjacency, partition and intersection relations, lacking a generic framework for topological relationships. Therefore we had to look elsewhere for solutions.

### **Linking strategies with BOT**

The ontological alignment is crafted to enable the application of BOT’s topological properties to the description of exhibits and the application of Display’s topological properties to building elements. This alignment is achieved in four ways.

Firstly, there are two specializations to manage display spaces:

1. The bot:Space class is specialized by a display:ExhibitionSpace subclass, which is designed to describe exhibition spaces and inherits properties for generic mereological relationships.
2. The bot:hasSpace property is specialized by a sub-property display:hasExhibitionSpace.

Next, we establish a class equivalence relation to create two parallel classes, bot:Element and display:Element, allowing us to share topological and mereological relations at the model level.

Finally, the bot:Interface specialization is designed to specify the properties of non-topological relationships between spaces or between spaces and elements.

### **Support for topological relationships**

The ontology employs high-level properties, mirroring the BOT pattern, to define the topological relationships of spaces and building elements. ➜ topo While BOT defines these properties at the building element level (bot:hasElement), Display defines them at the exhibit level (display:hasExhibit).

An abstract space can be linked to an exhibit through either the display:containsExhibit property when considered as an exhibit or the bot:containsElement property if considered as a building element. Building elements, defined by either bot:Element or display:Element, always qualify as exhibits due to class equivalence.

Additionally, super-properties (display:hasTopologicalRelationWith) are defined to enable the hierarchical organization of topological relationships in displays. This hierarchy distinguishes between proximal and spatial relations. Various types of exhibits, as subclasses of display:Exhibit, will inherit all these properties through class inheritance, but are not already implemented.

### **Linkage with CIDOC and other heritage ontologies**

Display prioritizes a spatial perspective, contrasting with the event-oriented approach of the CIDOC conceptual model. The CRMarcheo extension effectively handles stratigraphy through temporal entities, reflecting events over time. However, modeling spatial relationships in an exhibition according to the CIDOC model would be too complex in terms of notation and application. Despite this, describing exhibitions using CIDOC-CRM is essential due to its prevalence in museums and heritage fields. To bridge this gap, we propose linking the Display ontology to CIDOC-CRM in the following ways:

1. Exhibits can be instances of the E18_Physical_Thing class, enabling their description using CIDOC-CRM.
2. Aggregates of exhibits within the display:Display class can be instances of E78_Curated_Holding, representing results of activities described using CIDOC.

This proposal is open for discussion with the museum community.

## **3. Pattern presentation with use case**

To test the Display ontology, we applied it to describe Philippe Thomas’s exhibition *Feux pâles*, organized at the CAPC in Bordeaux in 1990. This exhibition, which functions as an installation, is well-documented thanks to the archives and research conducted by Zoë Renaudie as part of a Master’s in conservation-restoration.

Populating the display:Exhibit class is sufficient to indicate the presence of an exhibit in the exhibition. We can easily declare that the *CAPC* work, a barcode greeting visitors, hangs on the entrance display wall. The bot:Interface class is used to detail the hanging, specifying the relationship between the display wall and the exhibit.

The description of spaces utilizes classes and properties within the bot namespace. The connectivity of exhibition spaces can be described using one of three fundamental properties: bot:adjacentZone, bot:intersectsZone, and bot:containsZone, with the specialized property display:hasExhibitionSpace.

The entrance space connects to the first room via two passages.

This use case is particularly interesting due to the complexity of the space. The exhibition is set in an existing space reconfigured with wall paneling and display walls, creating different rooms that communicate with each other through multiple passages. The ontology enables the description of spatial organization in various ways: by using circulation interfaces,  describing volumetric intersections, or declaring mereological relationships.

In special cases, the location of exhibits can also be described using intersections. For example, the location of the work *Parcelle à céder*, a parquet floor running between the rooms titled *De la propriété littéraire et artistique* and *Mesure pour mesure*, can be specified with two declarations using the property display:intersectingExhibit. 

**Example of Topological Relationships Between Works:**

The arrangement of works in space can be clarified by mapping the topological relationships between exhibits.  In the room entitled *Le cabinet d’amateur*, the two Janssens are hung opposite each other, and described by a symmetrical property (`display:faces`).

**Special Case of Objects in the Showcase:** 

Similar to spaces, exhibits can be contained within other elements of the exhibition. For instance, all works within the showcases in the *Inventaire du mémorable* room can be described as included in that showcase. The busts positioned on either side of this showcase are described as being to its right and left, allowing us to conclude that the showcase is positioned between these two items.

### Topological inference

Using an ontological model allows for leveraging description logics to infer new facts from existing data. For instance, from an initial set of topological statements, several relationships, indicated by dotted lines, can be deduced.

This capability is especially valuable given the often incomplete or supplementary nature of documentary sources in historical research. The Display ontology takes full advantage of OWL semantics, enabling the expression of symmetry and transitivity, and the declaration of property chains.

## **Conclusion**

The use case we presented demonstrates that the ontology developed for this project can describe complex curatorial phenomena in fine detail and offers enough expressivity to leverage the ontological model through inferences. The Display ontology’s application domain is well-suited for an ontological model. The spatial relationships between exhibits and display spaces are particularly suited for description using the second-order logic employed by OWL. Reusing the BOT ontology core has allowed us to develop a concise, flexible, and versatile model.

The ontology mainly comprises three classes derived from BOT and two specific subclasses defined in the Display namespace. Five properties are sufficient to describe the spatial relationships between exhibits and spaces, complemented by a group of around twenty topological and mereological properties. The alignment between BOT and Display allows applying BOT ontology properties to Exhibits.

Other ontological works have addressed art exhibitions but have not considered the spatial dimension of their display. By focusing on the expographic configuration, the ontological perspective adopted for Display partially abandons the use of CIDOC-CRM, which can still be utilized to describe exhibit or exhibition exhibition as an event. This approach results in a more concise and user-friendly model. The direct nature of the description is intended to serve as the basis for developing a computer application for acquiring archival data and producing three-dimensional visualizations. Semantic web technologies thus provide an abstract model for effectively reasoning about incomplete and sometimes contradictory documentation.