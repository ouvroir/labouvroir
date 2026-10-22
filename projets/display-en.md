---
title: Display
description: "Tool for documentation des accrochages de collection et de visualisation 3D"
tags: [CIÉCO, documentation, 3D visualisation]
github: https://github.com/ouvroir/display-ontology
projectLink: https://github.com/ouvroir/display
otherLinks: [https://linked.art/model/exhibition/]
lead: Ouvroir
team: [emchateau, lenamk, ZoeRenaudie, dvalentine]
since: 2021-11
draft: false
lang: en
slug: display
cieco: true
bannerImage: # leave empty if no special banner
pageImage: display.png
status: done
---

# Display

The historical research carried out by the first axis of the CIÉCO partnership involves the mobilization and exploitation of numerous archival sources in order to document the history of collections displays in art museums and to be able to proceed with their reconstitution.

A tool is needed to support the entire research process, from the collection of historical information to the formulation of hypotheses and the recording of results.

The software solution we are developing is based on the creation of a documentary model independent of any _a priori_ visualization technology, in order to guarantee the durability and long-term conservation of the recorded data and to allow for possible reuses in different digital contexts. This model consists in the production of a computer ontology intended to describe in an explicit and formal way the features of a collection display or an exhibition (identification of the exhibition, proximity and contiguity of the works, vis-à-vis, etc.).

This ontology facilitates the recording of historical information about hangings and proposes solutions to account for uncertainty and documentary gaps. It will be compatible with the CIDOC-CRM ontology, a conceptual reference model promoted by the International Organization of Museums, of which it will form an extension to cover the specific domain of hangings and exhibitions. The developed model will be published for comments (Request for Comments) within the museum documentation community (LinkedArt, CIDOC, CHIN).

The functionalities offered by the data model and the application are based on a spatial approach and the use of 3D modeling to facilitate the reconstruction of collection hangings. The system exploits the digitization of data to propose calculated reconstructions based on the analysis of the spatial constraints of the exhibition spaces and information on the works exhibited (dimensions, weight, lighting).

This tool, developed by an external service provider, offers an ergonomic graphical interface to work from the documentary model expressed in the form of an OWL ontology for the recording of historical information on hangings defined by the person in charge of developing the digital infrastructure based on the work of researchers. Easy to use, it can be used by art historians without any particular technical skills. It facilitates in particular :

- the creation or automated import of lists of works
- recording or defining the geometry of an exhibition space
- the location of works in this space

Thanks to the documentary model used, this information can be qualified by level of proof and sourced, but also shared in the form of open and linked data. The tool allows to generate three-dimensional visualizations from the recorded spatial information. Several rendering engines are implemented to produce restitution hypotheses in the form of light tables or 3D browsable spaces in a web browser. The software developments are free and open. The application data must be serialized in JSON-LD, respecting the data model expressed in OWL for interoperability purposes. The developments allow to generate 3D visualizations on the fly based on the WebGL standard.

To achieve the design of this research tool, two design stages are planned (realization of a pilot in year 2, followed by a practical implementation and evaluation, and a second iteration in year 3) which will be extended by a dissemination stage associated with subsequent funding research depending on the interest of museum partners.

References : 
- Renaudie, Zoë, Valentine, David, Château-Dutier Emmanuel (2026, juillet 27-31). Documenting Exhibition’s Display Digital Humanities 2026 DH. Corea. https://ouvroir.github.io/atelier-display/dh2026/
- Renaudie, Zoë, David Valentine, et Emmanuel Château-Dutier. 2026. « Display : Une Infrastructure Sémantique Pour La Documentation Structurée Des Accrochages d’exposition ». In Actes de La Conférence Humanistica, édité par Serena Crespi, Simon Gabay, Martin Grandjean, Ariane Pinche, et Marie Puren et Léa Saint-Raymond. Anthology of Computers and the Humanities. https://doi.org/10.63744/ju117YgD6qgM.
-Renaudie, Zoë, Valentine, David, & Château-Dutier, Emmanuel (2025, juin 17). *Présentation du développement de l'interface de Display*.  CIECO, Montréal. https://ouvroir.github.io/atelier-display/interface/
- Renaudie, Zoë, Valentine, David, Château-Dutier Emmanuel (2026, mai 19-22). Display : une infrastructure sémantique pour la documentation structurée des accrochages d’exposition. Humanistica 2026, Paris. https://ouvroir.github.io/atelier-display/humanistica2026/
- Renaudie, Zoë, Valentine, David, Fraser Marie, Château-Dutier Emmanuel, (2025, novembre 5). Présentation de l’outil Display pour la documentation de l’accrochage. Midi-causerie L’Ouvroir, Montréal. https://ouvroir.github.io/atelier-display/midicauserie/
- Château-Dutier, Emmanuel, Valentine, David, & Renaudie, Zoë (2024, décembre 17). Documenting exhibition with Semantic Web. Journée d’étude La documentation des expositions. L’Ouvroir, Montréal. https://ouvroir.github.io/atelier-display/documenting/
- Renaudie, Zoë, Valentine, David, & Château-Dutier, Emmanuel (2024, mai 27–31). Display, ontology and database for exhibition documentation. DHNB 2024 Conference – From collections as data experiments to sustainable data services: Experiences at the intersection of cultural heritage and digital humanities, Reykjavik, Islande. https://ouvroir.umontreal.ca/actualites/blog/displayOntology-fr
- Renaudie, Zoë, Valentine, David, & Château-Dutier, Emmanuel (2024, octobre 28). Atelier Display : documenter des accrochages de collection à l’aide d’une approche ontologique, Ouvroir, Udem https://ouvroir.github.io/atelier-display/atelier/
- Château-Dutier, Emmanuel, Valentine, David, Renaudie, Zoë, & Krause, L. (2024, août 7). Documenter les accrochages d’exposition ou de collection muséales : une approche ontologique. DH2024, Washington, D.C. https://ouvroir.github.io/atelier-display/dh2024/

\*_Display is designed by the laboratory in the framework of the Partnership [New uses of collections in art museums](https://www.cieco.co/). Project manager: Lena Krause (2022-2023), Zoë Renaudie (2023-). Scientific director: Emmanuel Chateau-Dutier. Ontologist : David Valentine_
