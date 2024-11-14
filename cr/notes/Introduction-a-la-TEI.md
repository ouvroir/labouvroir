---
title: Introduction à l’édition critique avec la TEI
author : Ouvroir
date : 2023-10-26
draft: true
tags:
    - TEI
---

# TEI 
cours sur le traitement des sources anciennes.
utilisation de l'informatique pour modéliser texte. 
TEI cadre de travail personnalisable
Norme : 600pages

md pour le web


eXtensible Markup Language

## 1.1 Edition critique
_Qu'est-ce-qu'une edition critique ?_
Sert à désigner le caractère savant d'un texte.

L'objectif général d'une édition critique est de reconstruire le plus justement possible le texte d'une œuvre tel que désiré originalement par l'auteur, grâce à l'ensemble des données et des documents disponibles, tout en présentant les choix faits à travers les époques par les différents éditeurs. De manière générale, une édition critique donne accès aux états primitifs et successifs d'une œuvre qu'il serait difficile de consulter autrement en raison de leurs supports, souvent anciens et fragiles, ou de leur disponibilité restreinte (ces documents sont rares et parfois conservés dans des dépôts protégés dans divers pays). 

essai de reconstitution d'un texte et qui justifie ses parti-pris ==> imputable 

comment rendre compte le plus fidèlement possible de la source ?

Produire un texte
Ce n'est pas la repro d'un texte mais résultante d'un ens de choix.
necessite de se conformer a un certain nombre de texte
tenir compte des versions, le rendre intélligble pour les contemporains
choix en fonction des documents, de leur kalitey et du public visé

investissement important
bcp de temps, des grosses équipes 
interoperabilite x stabilisation 
production de metadonnées normalisés
prob de pérennité : obsolescence technique, information encodée et nécessite des opérations de desencodage, 
couche d'encodage multiple = accès à l'info problématique car elle est dépendante de logiciels 

Avantage d'un balisage semantique

_Peut-on sérieusement  utiliser un log de traitement de texte?_

Word c'est le demon ==> assez limité, idem pour la mise en page, documenter proprement les images
abrevations = pb d'expressivité pour rendre compte de toute l'information, idem pour le versionnage 

- forme/ contenu 
- expressivite
- documentation de l edition 
- controle de la production 
- obsolescence et interoperabilite

Definiton des documents structures 

un document dont la structure logique est d'écrire plutot que sa mise en forme physique, idee d un encodage descriptif 

La notion d'encodage 
- encodage descriptif vs presentationnel 

superiorite  du balisage descriptif sur les autres balisages du texte
presente l'avantage d'une meilleure distinction entre le contenu et la forme
permet une meilleure maitenance du texte encode et portabilite des artefacts 

International Resource Identifier (IRI)a remplacé URI pour pouvoir intégrer les encodages UTF8 dans les URI

Balisage opération tres bête : procedure mise en oeuvre lors du balisage 
- reconnaissance des elements 
- selection des balises 
- realisation du balisage, marquage de l'element 

annotations sur le texte
seulement une convention graphique 

Modelisation du texte :
- **hiérarchie ordonnée d objets contenus** (OHCO Ordered Hierarchy of Content Objects en english pour les bilingues)
- structure hiérarchique
- relations linéaires

choisir un type de rpz du texte qui est un modele hierarchique d'objets contenus les un dans les autres. 
il existe aussi d'autres manires de faire' Celle-ci presente l'avantage d'être processable = lisible par la machine"

## 1.2 avantage d'un balisage senantique 

avantage sur un balisage présentationnel ;
- reduction d'etablisement d un texte simplifié 
- reduction des pbs de maintenance
- meilleure portabilité

ballec la forme que ca va prendre, on se concentre sur le contenu

offre un certain nombre d avantages pour l'editeur ==> plusieurs présentations du même fichier
pas de contrainte de logiciels avec ce balisage 

Qualiteyyy des documents

## XML <3
- metalangage XML 
- permet le developpement de vocabulaires descriptifs de balisages interoperables specifiques a certains domaines (genre TEI, XML-RDF lol)
- un modele de contenu arborescent 
- pas de reelle semantique 
- large utilisation dans le domaine culturel (metadonnees)
- grammaire lisible par la machine


C'est une information structurée qui décrit la sémantique mais qui n'est pas semantisée
_telle chose un paragraphe, mais on dit pas ce qu'est un paragraphe_ 

Important stock de donnees decrit en XML 
Format le plus commun au MONDE

##  Historique de XML

1986 ; def du SGML
1989 : Definition du HTML, derive du SGML et naissance de Zoe Renaudie
1998 : XML 1.0m publication par le W3C des specifications d un metalanage de balisage du texte et naissance de Camille Delattre
2004 XML 1.1 (amelioration)
pour memoire: la spe de HTML5 en 2011 renonce a xml et c'est **dramatique**. du coup : copie xml mai plus complexe


xml cousin du html : donc vocab commun

## principes de conception de XML 
- applicable a tout type de tx 
- extensible 
- definition par un schema ==> XML Schema (xmls)
- hypertextualité
- simple, universel
- modele hierarchique, 
- arbre inversé, une racine (_root_), des noeuds qui amenent des infants
- les enfants héritent des proprietes des parents 

compatible avec CSS : Les feuilles de style en cascade, généralement appelées CSS de l'anglais Cascading Style Sheets, forment un langage informatique qui décrit la présentation des documents HTML et XML. Les standards définissant CSS sont publiés par le World Wide Web Consortium

## Syntaxe XML 
En 4 points 
- tout seul ça fait rien
- ne sert pas afficher les données mais a les decrire
- le nom des balises nest pas predefini 
- on peut utiliser une grammaire de balises (schema)
- auto-descriptif 
- c'est que du texxxxxte, et ca c'est super.

faire des balises pas des betises
<titre pays="France">Cam-est-la-plus-intellIgente</titre>
balise ouvrante
balise fermante 
attribut : nom+valeur 
<date from="1989">en 1989</date>

contenu mixte 

document XML avec son prologue 
Specification de l encodage
UTF-8 par default
construction syntaxique construit sur chevrons (c est pas un animal)
syntaxe des elements vides : <date> </date> =<date/>
corps du doc est un arbre d elements
element racine englobe tous les elements

Attributs
XML est sensible a la casse !
JSON est un langage structure (comme ma vie lolilol)


## Contraintes syntaxiques

Entites internes : entites caracteres pour predefinies pour saisir certains caracteres aue l on doit obligatoire;ent coder 
les notations &lt; (signe inférieur), &gt; (signe supérieur), &amp; (et commercial), &apos; (apostrophe) et &quot; (guillemet) qui sont tous prédéfinis
Entites externes

&amp; = &

Les commentaires 
- commencent par 

Les instructions de traitement servent à fournir dans le document des instructions pour un programme (feuille de tranformationm utilisation d une feuille de style CSS)
commencent par <? et se terminent par ?>

CDATA
- sections CDATA : sections de caract8res non parsees
- les donnees comprises entre ces balises ne doivent pas être interpretees comme XML 

Espaces de nom 
- formelle defini par son namespace-iri
- declare avec **xmlns** pour xml namespace
- declaration par defaut

Espace de nom (prefixe)
- raccourci pour espaces de nom 
- declarer le prefixe avec xmlns:prefix

Document bien formé = respect d'un certain nombre de contraintes

## Notion de schema 
- le modele de donnees de xml ==> sept types de noeuds 
- modele de documents = definissent les contraintes que doit respecter une certaine classe de documents. On utilise schemas xml et/ou schema RelaxNG 
Permet la validation des documets XML 

## TEI 

- on peut produire des schemas de documents 
- ontologie generale du texte 
Les versions de TEI sont des Propositions P 
TEI choisit SGML avant XML 
On est dans la P5

TEI indépendant de solution technique.