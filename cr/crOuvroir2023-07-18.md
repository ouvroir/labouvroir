---
title: Réunion hébdomadaire du 18 juillet 2023
description: Compte rendu de la réunion
author: ouvroir
date: 2023-07-18
draft: false
tags:
    - cr
    
---
# Réunion hebdomadaire


## Admin

### common

- BDRV: rdv s'est passé comme attendu
- BRDV va contacter les autres bureaux de la recherche: rencontre avec les membres du projet prévue


- identifier ce qui peut être fait sans dépendances, commissions par lot
- prioriser des éléments noyeaux bénéfiques pour l'encyclopédie
@lenamk: repasser dans le cahier des charges pour voir

- rechercher un prestataire apte à faire la prestation
    - Faire un message sur un forum javascript local : meetup + Svelte, idéalement spécialiste SVELTE
    - Paul M n’a sans doute pas assez de disponibilités
    - Contacter agences
        -  libre Qc
        -  [libeo](https://libeo.com/notre-approche)
        -  [LINAGORA Canada](https://www.linagora.com)
        -  [Drave Développement](https://drave.dev)
        -  [eleven labs](https://eleven-labs.com), car [entrée de  blog sur svelte](https://blog.eleven-labs.com/fr/a-la-decouverte-de-sveltejs/)
    - Pierre Choffet peuc@wanadoo.fr : dev C++, mais fait aussi javascript et php

@lenamk: continuer recherche prestataire (suivre piste https://nousappre.com/formations/svelte/montreal)

Serveur IIIF, recontacter les bibliothèques
- retour de vacances de Martin Sévigny le 31 juillet
- Emmanuel le recontacte à ce moment


### encyclo 
- document pour l'équipe LEAF
- notes

Références à Zotero: c'esst mieux de stocker un identifiant, mettre en forme pourrait être compliqué à faire dans LW
- comment fonctionnent les identifiants, spécifiquement dans une bibliothèque partagée? 
- voir si on peut utiliser un plugin pour avoir un identifiant signifiant ex: auteurDate

@lenamk: 
- faire des tests pour vérifier comment fonctionnent les identifiants (bibliothèque vs collection, modification, déplacement...)
- si l'identifiant Zotero est pérenne, on pourrait s'en servir mais il faudrait gérer l'affichage pour le rendre lisible dans l'interface
- identifiants auteur-date: pourrait servir de clef sans avoir de mise en forme de la référence

Pour le moment il n'y a pas de description des fonctionnalités, seulement des besoins. Seul le formulaire pour les headers en est potentiellement une.
- lookup entre articles: zone de sélection, drop sur le plan
- lookups doit se faire dans un ensemble de répertoire cibles, aller chercher les fichiers en fonction de l'arborescence (sur github ou aillers), mais renseigner les liens relatifs
- sinon, système d'identifiants pour les articles: règles de nommage

Exemple dans le repo: teiCorpus → teiHeader → 
- include → fait en sorte que le fichier inclut tous les autres = accès à tous les sous-fichiers
- sourceDesc id = 


relier des documents pas édités, pas publiés: travailler à partir des sources
- orienté XML (préférable): lookup devrait se connecter au corpus et voir tous les fichiers disponibles dans l'arborescence xml, compatible avec xi:include ?
- orienté web: avoir une API qui génère la liste des identifiants (mais ça crée une dépendence)


hooks sur le DOM pour alimenter
- sauvegarde automatique
- gros du travail dans LEAF s'effectue dans le DOM 
- injecter des éléments qui seront ensuite validés

