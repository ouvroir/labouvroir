---
title: Introduction à l’édition critique avec la TEI
author : Ouvroir
date : 2023-11-02
draft: true
tags:
    - TEI
---

- XML n'est pas un langage sémantique mais utilise des balises sémantiques. 
- la sémantique se fournit en langage naturelle.
- Sert à vehiculer des données (comme Jaaason, enfant des annees 80...)
- caractéristiques d'XML à l'égard du texte : 
    - modèle hiércharchique aka arborescent 
    - opération de modélisation du texte, rpz informatique du texte ==> choisir un pdv, est qu'on rpz telle ou telle chose ?
    

- syntaxe d'xml : balise ouvrante fermante, definies par chevrons, /, attributs (nom="valeur"). 
    - Declaration XML 
    - element racine xmlns="déclaration d'espace de nom"
    - plusieurs espaces de nom : xmlns:mpam="URI"
    - Noeuds de 7 types :
        - Root node (nœud racine): à ne pas confondre avec l'élément racine. Il est au contraire le nœud parent virtuel (parent node) de l'élément racine.
        - Element node (nœud élément)
        - Attribute node (nœud attribut)
        - Text node (nœud texte)
        - Namespace node (les espaces de noms déclarés dans un élément)
        - Processing instruction node (nœud qui contient le texte de l'instruction)
        - Comment node (nœud qui contient le texte du commentaire)

## Rudiments d'encodage des sources manuscrites  
modules : 
transcr 
msdecription (description des manuscrits)

- decrire aussi finement que besoin des phenomenes textuels

### Macrostructure du texte et teiHeader
Composition d'un fichier TEI 
TEI ==> element racine
 TeiHeider ==> metadonnées sur le texte
  text ==> texte lui même 

Document composé d'au moins deux parties :TeiHeader + text
espace de no; de la tei = xmlns 

MacroStructure du "text" composite
front = avant texte (sommaires etc)
back = annexes

structures generiques
celles obligatoires = body ou group si regroupement de textes

teiCorpus : certains docs commence par teiCorpus non Tei pour grouper ensemble de documents. 

TeiHeader minimal :
  fileDesc obligatoirement composé de : 
    titleStmt
    publicationStmt
    sourceDesc

body
div
head
p 
seg

head doit être le premier element de div, ne peut pas flotter. 
paragraphe, unite minimal de la TEIm si pas body
p et div sont pas copains

structures de listes 
list peuvent avoir des labels

list
    label (etiquette)
    item (item de liste)
    label (etiquette)
    item (item de liste)
soit label+item soit item seul

lg = groupe de lignes 
    l = ligne 

attribut n utilisable presque partout et très pratique. 

Structures de tableaux
Elements d'usage courant 
- hi mise en valeur ==> highlight 
- quote : citation longue, q pour les citations courtes
- foreign : passage de langue étrangère
- term, gloss termes et gloses    
- date
- name, persName; placeName : nom de personne, lieu
- <pb/> indications des changements de page
- fw : permet d'encoder un titre courant, une reclame, une autre info = permet inserer dans flux du texte ce qui n'appartient pas au texte. 
    
Editeur edite le texte pas la mise en page
   
Attributs globaux (toujours disponibles)
- @n : numero ou label (pas unique)
- @rend indication sur l'apparence
- xml:id fournit un id unique
- xml:lang indique langue du contenu textuel de l'element
    
balise foreign utilise quand il n'y a pas
    
 Attributs fréquemment employés   
 - @type pour typer un element
 - @target lien interne
 - @ref reference
 - @key reference canonique  : lien, id dans syteme de nommage

Elements de type milestone

designe un point dans le flux textuel. Des elements XML vides.
 - pb/ : saut de page
 - cb/ : saut de colonne
 - lb/ : saut de ligne
 - milestone/ : elt borne permettant de délimiter une partie de texte selon un autre système que les div. 
 - anchor/ : élément ancre  
Permettent de marquer chevauchement avec deux balises autofermantes encadrant le texte. 
    
Structures complexes
- addSpan partie du tex ajouté, avec @spanTo qui pointe vers une cible 
- anchor 


### L'inscription du texte sur le support

Prise en charges des lacunes 
- gap : passage ne pouvant pas être restitué pour des raisons materielles
- unclear : qualifie travail editorialisation 
- supplied : restitution d'un passage manquant

Ajouts et surplus
- add : texte ajouté
- del : texte supprimé

Description des mains 

- @hand : ds corps texte
- @handDesc : ds teiheader
- handNote : repetable et peut contenir une locanisation avec @locus

### Les corrections éditoriales
    
Passages fautifs
- sic : passage fautif, ou segment syntaxiquement incorrect
- orig : texte original
- corr: correction du scripteur
- utilisation de : choice : 
"ori mais je fais le choix de reg"

Abréviations
- abbr : abreviation 
- expan : abreviation developpee

## Exos

Bare = schema minimum associé à la TEI 


Analyse du document : caracteristiques pour la modelisation 

Q/R
deux mains 
Se poser la question des differents cas de figures. Être assew generique.
Indications du traitement archivistique 
Regrouper les questions et les réponses 
Restituer le texte ou la mise en page ? Depend des choix et des pdvs editoriaux.

## L'en-tête (le teiHeader)
Pourquoi fournir des métadonnées ?
- documenter la source 

Plusieurs choix des modèles descriptifs, à définir selon : 
- la politique de votre etablissement 
- bonnes pratiques
- mapping avec d'autres modèles

ex stratégie : Weboai
 portail consortium autour données numériques. 

Sous composant du TeiHeader
- fileDesc : descritpiton fichier
- encodingDesc : endroit pour renseigner info sur notre facon de faire
- profileDesc : profile informatique utilisé pour travailler le fichier. informations classificatoires
- revisionDesc : description des révisions. 

- TitleStmt est repetable : permet de mettre titre en plusieures langues, sous titres, etc
- publicationSmt : mention publi du texte electronique
- SourceDesc : renseignments sur la source dont est issu le fichier numerique
- editionStmt ; informations relatives à l’édition
- extent : taille du fichier
- seriesStmt : informations relatives à la collection
- noteStmt : notes fournissant des informations sur le texte

Dans titleStmt : 
- title
- principal, author, editor, funder 
- respStmt : contributeurs et leurs roles exacts

Pour aller plus loin : 
msdesc : décrire le manuscrit 
produire des bdd, catalogue de manuscrit, lister des témoins et les decrire, instrument pour la codicologie quantitative

**Faire un TeiHeader complet et un index dans le doc final**

## Personnaliser la TEI

Beaucoup de modules

ODD : generer d'autres docs en fonction de votre facon de votre utilisation de la TEI
TEI est gentil : Roma genère des schemas de tei

**Utiliser Roma.**

