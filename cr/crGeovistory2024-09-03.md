---

title: Rencontre Stéphane Hart - Geovistory
description: Compte-rendu de la rencontre
author: ouvroir
date: 2024-09-03
draft: false
tags:
    - cr 

---
Présents : Emmanuel Château-Dutier, David Valentine, Zoë Renaudie, Stéphane Hart, Camille Delattre

Stephen Hart, ontologiste. 

https://www.geovistory.org/

Partners : 
LOD4HSS financement de 2 ans pour dev la communauté 
KleioLab : entreprise qui adev l'infrastructure et initiatrice du projet meme si aujourdhui opensource
Larra : dev qui a permit de dev 
Universitat Bern. 

Environment : 
5 composants principale : 
Toolbox (interface des utilisateurs avec vue par projet. Cacher l'ontologie User frindly et vu par projet)
Repository : Apporter des données d'ailleurs.interopérable avec graphe de connaissance
ISO 21127 CIDOC-CRM et SDHSS : Ontologie créé par francesco,  géré sur OntoMe qui peut etre utilisé par d'autres projets. ntologie assez souple
Publication : Sparql end point . Chaque projet peut avoir son entrée sparql. mais on peut aussi requeter l'entierté de l'ontologie. 
Community : discord, newsletter

But : accompagner chercheurs dans processus de recherche. Accompagner les projets. 

Emmanuel demande comment les triplets co-existent. Chq triplet a des statments et des namegraphs. On pourrait faire une réunion avec l'équipe technique. 
Tous les statements sont sourcés, ne sont pas dans les staments, son non visible. 

Pésentation de l'interface. 
Sources, Entities, Digitals, Analysis

Emmanuel parle de Leaf writer. 

Plan de financement pour intégrer Transcribus. L'intégrer au projet de la nouvelle France? Rimouski 19-20 septembre. 

Ont pensé à intégrer zotero : tout mapper parce que pas sémantique.

Metadonné de l'entité et de la repro numerique. 

C'est génial. Caché l'ontologie mais visible en sous texte. 
Saise des champs et configuration des champs (deplacer, ne pas visualiser)

Geovistory ne fonctionne qu'avec leur ontology pour assurer une interoperabilité totale 

Sourcer simple 
Date de naissance : CIDOC CRM bloque le fait qu'il y en ait qu'une. Factoids permet de dire quelle est la plus plausible. On peut commenter. 

Import pas otpimal. Csv : script interne. Financement pour lier avec openrefine. 
Nouveau tableau de bord pour edition des donnees [Open data editor](Open data editor) ~~Data Portal~~

Ontologie recuperer a partir de profils. OntoME profils. permet de selectionné une partie de l'ontologie pour l'afficher da la toolbox. Possiblité d'avoir des microprofils pour avoir des propriétés très restreintes. 

On reprit CIDOC mais à partir de l'ontologie fondationnelle DOLCE. Puis on fait les connexions avec SDHSS au meme niveau. Puis extensions spe pour projets. CIDOC-CRM a 70%. 

DNS descrition and situation ontology Ando Gangemi 

Ont réutiliser CIDOC, on fait quelques doublons quand l'utilisait vraiment pas de la meme mainiere. Puis on ajouter leur entité commeçant par un C. 

Francesco devait travailler sur CRM-SOC. Désaccord entre les dev et au sain du SIC qui ne pensaient pas que ca faisait parti du CIDOC-CRM. Volonté de crée crm-soc qui fasse pond ent sdhss et crm-aaa.

Documentation des personnes dans SDHSS? C9 Intentional Entity. était subclass of E18 Physical thing mais va changer. 
Superclass de C25 Intentionnal Collective. 
Comment gère les lieux et la geographie? Differment de cidoc crm (dif la plus importante) Place dans crm n'est qu'une localisation. Geographical place sous class de geographic Feature. C13 geographical Place subclass de E26. 
La geo devrait pouvoir etre une entité temporelle. Typage des geographical place par : has geographical place kind. 
N'ont pas encore géré les intersections et etendu des leiu geo. Parce qu'on pas encore été confronté a ca. 

Ontologie evolue : font des majs. 
Espere ne pas avoir de changement drastiques. Sont actuellement à la v6.2.1. 
Possible de travailler par version. 

Archi : manifestation. 
essaye ext des sources SHDSS mappé avec RICO (monde des archives) 

Link entre RICO et LMRO

avec Camille et Zoë s'interessent a l'implementation de LRM : voir discussion github. 

Envoyer papier à Stephen. 

Plusieurs peuvent travailler sur la meme personne donc interface parfoit un peu lente. Existe depuis 3 ans. Pas d'images pour une question d'espace.

Pas de gestion des images. url de l'image. Platforme web sur geovistory affiche l'image. 
Pas d'api en dehors de celle pour le Sparql. API JSON classique? Utilisateur construisent leur portail public : Une page sur geovistory mais peut l'avoir à l'exterieur. 

Gestion infra par le public, l'uni
Et accompagnement de projet par l'entreprise Kleolab.

Stage Zoë à Bern? 

Common reorganiser zotero par une interface pour les raccrocher a des projets. Va vouloir publier de la documentation sur une exposition. Devoir les recuperer pour les afficher sur un site web de maniere performante. 

Analysis permet de faire des recherches et export facilement. 
Moyen de faire des exports d'un tableau. A voir si on peut exporter des fichiers structurés json. 

Regarder Omeka S.

Toutes les données sont gerées en base de donnees relationnele et ensuite géré en sparql. Bdd SQL : prosql : tous les triplets; warehouse etiquette et labels; et outil comme redpanda (kafka streams) permet de faire edition simultanée. 

https://github.com/geovistory/dev-stack

Question technique envoyée avec analyse des besoins. 

Stephen nous envoie Presentations. 
Telechargement possible sur ontoME. 
Shema bdd relationnel pas accesible, a demander. 

Pas de roadmap. 

Inférences pas encore bien gérées. 

Pour display : Se situer dans les 3 ontologies. mais pas bon pour display. Et l'implémentation non native.