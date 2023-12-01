---
title: Artistes-femmes dans la collection du MAC
description: "Visualisations de données révélant l’entrée des artistes-femmes (acquisitions par don et par achat) dans la collection du Musée d’art contemporain de Montréal entre 1964 et 2020"
tags: [visualisation de données, JavaScript, web, études féministes, méthode quantitative, CIÉCO]
link: https://observablehq.com/@artistes-femmes-mac
lead: Valentine
team: [valentine, lenamk]
since: 2021-11
draft: false
lang: fr
slug: artistes-femmes-mac
bannerImage: mac-femmes.png # Only for cieco projects
pageImage: mac-femmes.png # "project-image.jpg" 
status: ongoing # planned | ongoing | done
---

## Origines du projet

Ce projet a pour point de départ le mémoire de maîtrise de Valentine Desmorat : *L’entrée des femmes artistes dans la collection du Musée d’art contemporain de Montréal, de 1964 à 2020 : analyses statistiques et facteurs déterminants*. Dirigées par la professeure Johanne Lamoureux (UdeM), ses recherches sont menées dans le cadre du Partenariat « Des nouveaux usages des collections dans les musées d’arts» ([CIÉCO](http://www.cieco.co)). L’objectif principal est d’expliquer la présence comparativement importante d’œuvres d’artistes-femmes dans la collection du MAC. La mise en ligne des données à partir de la collection du MAC à l’automne 2022 a favorisé une telle initiative, mais a requis une certaine littératie numérique.

La [clinique numérique](https://ouvroir.umontreal.ca/fr/services/#clinique-numérique), mise en place à l’automne 2022 par Lena MK dans son rôle de responsable de laboratoire à l’*Ouvroir d’histoire de l’art et de muséologie numériques* (UdeM), a été le point de rencontre à l’origine de cette collaboration. À la suite d’un premier partage de connaissances entre l’approche féministe de Valentine et les pratiques de visualisation de données de Lena, a émergé une véritable complicité, ainsi qu’un projet commun. Celui-ci s’inscrit dans le cadre des activités de l’Ouvroir. 

## Projet

La collaboration a consisté en la production de code et de plusieurs visualisations de données sous la forme de *notebooks* [Observable](https://observablehq.com/@artistes-femmes-mac?tab=notebooks). Ces derniers ont servi d’environnement de travail et de diffusion. Ils sont éditorialisés, le code javascript et les visualisations étant présentés avec des textes en markdown.

- [Données et autres communs](https://observablehq.com/@artistes-femmes-mac/donnees-et-autres-communs) : traitement initial des données et préparation du corpus, avec notamment une fonction qui associe un genre à chaque œuvre étudiée
- [Nombres annuels d’achats/dons/acquisitions d’œuvres d’artistes femmes et d’œuvres d’artistes hommes (1964-2020)](https://observablehq.com/@artistes-femmes-mac/nb-dachats-dons-acquisitions) : histogramme interactif de répartition des dons et des achats d’oeuvres par catégorie de genre et par année (1964-2020), avec une option de tri pour faire apparaître des médiums spécifiques
- [Parts d’achats/dons/acquisitions par catégorie de genre (1964 à 2020)](https://observablehq.com/@artistes-femmes-mac/parts-dachats-dons-acquisitions-par-categorie-de-genre-196) : *piechart* interactif donnant à voir les proportions d’acquisitions (dons, achats) par catégorie de genre en fonction de la période choisie avec le sélecteur de temps
- [Nombres d’oeuvres données/achetées/acquises par médium et par catégorie de genre de 1964 à 2020](https://observablehq.com/@artistes-femmes-mac/nombres-doeuvres-donnees-achetees-acquises-par-medium-et-p) : *sunburst* interactif présentant la répartition des dons et des achats par médium et en fonction des catégories de genre
- [Tops 10](https://observablehq.com/@artistes-femmes-mac/top-10) : histogrammes associant les 10 noms des artistes (hommes et femmes, puis uniquement femmes) les plus représenté·e·s dans la collection avec les nombres d’œuvres conservées correspondant


## Approche choisie

L’approche choisie pour l’étude de la collection du MAC est quantitative, muséologique et féministe. Elle se réfère à l’essai pionnier de Linda Nochlin, «*Why Have There Been No Great Women Artists* ?». Paru initialement en 1971 dans [*ARTnews*](https://www.artnews.com/art-news/retrospective/why-have-there-been-no-great-women-artists-4201/), ce dernier porte sur les structures institutionnelles qui déterminent la faible part de femmes en histoire de l’art, ainsi que dans les institutions artistiques et muséales. 

La [charte de couleurs](https://observablehq.com/d/26cecfbef9723965?collection=@artistes-femmes-mac/htmlles2024) élaborée fait honneur à celle des *Guerrilla Girls*. Le groupe de militantes féministes diffuse dès 1985 à New York des « chiffres choc » qui dénoncent la marginalisation de femmes artistes de la part des institutions et du marché de l’art. En référence à leur démarche, les nombres et les parts d’œuvres d’artistes-femmes sont représentés dans les graphiques en rose fuschia, couleur aussi bien parodique que vive et éclairante. Alors que les œuvres d’artistes-hommes sont largement majoritaires, nous leur attribuons une non-couleur, le noir. Notre objectif est d’inverser les dynamiques visuelles et de centrer l’attention sur les œuvres réalisées par des femmes. 

À la source du processus, les données du MAC, disponibles sur la plateforme [donnéesQuébec](https://www.donneesquebec.ca/recherche/dataset/macrepertoire), ont servi pour produire les visualisations. Ces données représentent, à notre connaissance, 95% de la collection. À leur lecture, nous avons déduit que ce sont les sexes, et non les genres socialement construits des artistes, qui sont renseignés : les valeurs qui répondent à la propriété « genre » sont binaires ( « Féminin » ou « Masculin »). Nous avons ajouté la valeur « Mixte », pour représenter les œuvres produites par des artistes des deux sexes. Dans l’objectif de contribuer à une meilleure représentation des femmes artistes dans les collections muséales, nous avons choisi, pragmatiquement, de mobiliser les catégories sexuées et binaires propres aux sources auxquelles nous avons eu accès, plutôt que de renoncer à compter et à « montrer ». 

La plateforme [Observable](http://observablehq.com), l’environnement choisi pour la production des graphiques, promeut une pratique de code ouvert, avec des *notebooks* en ligne spécialisés en visualisation de données. Nos *notebooks* invitent à une plus grande accessibilité numérique : des cellules de texte décrivent le code et documentent les décisions prises au fur et à mesure du travail effectué. 

## Projets liés

- Mémoire de maîtrise de Valentine Desmorat (en cours) « L’entrée des femmes artistes dans la  collection du Musée d’art contemporain, de 1964 à nos jours : analyse  statistique et facteurs déterminants » 