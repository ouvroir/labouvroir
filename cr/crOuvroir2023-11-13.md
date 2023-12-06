
---
title: Réunion laboratoire
author: emchateau
date: 2023-11-15
draft: 
tags:
    - cr
    
---

## Reframe

Discussion sur le prototype.

Calcul du ratio à partir de la dimension. Permet ensuite de pouvoir conserver les ratio. Pouvoir distinguer des ratio abstraits permet de déterminer une position et attribuer un espace à l’image.

Dans le cas où deux images ont le même ratio, elles peuvent être affichées côte à côte. Mais si le ratio est différent l’alignement ne règle pas qui doit prendre le plus d’espace dans la page.

On peut donc se dire que l’on a une librairie de composants qui pourra faire plusieurs choses à l’avance sans avoir à trop paramétrer de choses pour gérer un affiche par défaut.

Le ratio peut donc être une bonne stratégie car la dimension en pixel est moins pertinentes.

Comment gérer les images qui n’ont pas de ratio standard ? on calcule le ratio réel de l’image puis on catégorise l’image en définissant un conteneur adapté.

Dès lors qu’on a un ratio optimal, regarde les fractions d’espace que les images pourront prendre dans le container.

Deux questions
- Faut-il gérer les propriétés CSS sur les contenus ou séparément ?
- Pour le moment pas de prise en charge de responsive

Pour avoir la dégradation, on va devoir indiquer une taille minimale. Se pose la question de savoir si c’est à Reframe de la déterminer. Savoir où doit être défini.

Continuer les expérimentation
- voir comment fonctionnent grid et flex
- valider ou pas l’approche par défaut
- réfléchir aux interfaces
- faire un point sur les specs

## Labo

Trium, faire un suivi

NAS 
- valider la dimension des fichiers vidéo
- Joel voir les méthodes de travail

Adobe, la licence peut être installée sur deux postes simultanément.

Finalisation de la configuration des écrans. 
- jeudi 16h30
- lundi 13h


