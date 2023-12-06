---
title: Atelier sur la ségmentation de corpus
description: Prise de notes collaborative durant atelier sur la ségmentation de corpus 29 novembre 2023
author: labouvroir
date: 2023-11-29
draft: true
tags:
    - atelier
    
---

**Segmentation d'images
Pour une classification sémantique des artefacts culturels.**

Domaine de la vision par ordinateur. 

## Principe de la segmentation 
- segmentation sémantique : 
identifie et classe les pixels d'une image sans distinction de leurs instances

- segmentation par instance :
identifie et classe les objets au sein d'une image en distinguant les instances de chaque classe. 

William: Est-ce qu'il s'agit de 2 opérations distinctes ou bien sont-elles employées l'une après l'autre ?

- segmentation panoptique : 
identifie et classe tous les objets, l'arrière-plan y compris d'une image

la seg peut prendre plusieurs formes : 
- des groupes de pixels 
- des boites englobantes (bonding boxes)
- des lignes
- des cercles
- des polygones

## la segmentation comme opération de classification

classer images en fonction de leur sens et valeur. 
classification vise à identifier des objets représentés dans un ensemble de données et en leur attribuant une étiquette

On leur attribue une étiquette, un nom, une valeur. 

Proche de la détection d'objet (boite autour des objets) mais pas exactement pareil. Seg : les coordonnées de l'objet identifié dans l'image. => Certains outils combinent les deux. 

seg et le détection d'objets sont deux opérations connexes. La différence est située au niveau de la **granularité** de la détection. 



## fonctionnement des modèles

- réseau de neurones
peut apprendre à reconnaître des régions et des caractéristiques précises d'une image. 

- réseau convolutifs
Ce sont les réseaux de neurones convolutifs (CNN) qui sont les plus communément employés pour les taches de seg et de classification d'images.

travail classique : acquisition des images > création d'une bd > annotation des images entraînement perfectionnement de l'algorithme > résultat de la seg et analyse des performances du modèle 

## Données et entrainement des modeles 

- données vérifiées utilisées pour entraîner l'algorithme = vérités de terrain (_ground truths_)

- plusieurs méthodologie : 
    - méthodologie supervisée 
    - méthodologie non-supervisée
    - méthodologie semi-supervisée

Cela dépend de différents facteurs: 
- quantité de données
- temps passé à la notation qui est une étape assez longue 
= trouver un équilibre entre les deux

## Techniques de seg 
### Outils d'annotation

On pourrait le faire sur photoshop mais au secours

Plateformes en ligne : 
- [CVAT](https://www.cvat.ai/)
- [VGG Image Annotator](https://www.robots.ox.ac.uk/~vgg/software/via/) (VIA)
- [LabelStudio](https://labelstud.io/)
- [Roboflow](https://roboflow.com/)

attribution d'étiquettes 
eux-mêmes ont des modèles de reconnaissance pour commencer le travail, processus qui se nourrit lui-même 

**quels modèles de données sont utilisés ?**

### Différents algo de seg 

- [Mask R-CNN](https://github.com/matterport/Mask_RCNN)
réseau de neurones convolutif (CNN) régions au sens des images par instance et par masques (utilise par Léa pour son mémoire)
- [YOLO](https://pjreddie.com/darknet/yolo/)  (you only look once): 
algorithme basé sur une archi de réseaux de neurones, fonctionnant en divisant l'image en grille, dans chaque zone de la grille, les pixels qu'elle contient sont associés à une classe d'objet.
Entraînement sur des images naturelles. 

=> /!/ les modèles répondent en fonction de leurs données d'entraînement. Démuni sur d'autres types de données. Ex : texte compris comme parapluie  

- [Layout Parser](https://layout-parser.github.io/)
bibliothèque python qui s'appuie notamment sur Google Cloud Vision, Detecron2(meta) et PyTorch. 
=> Il faut savoir coder pour pouvoir utiliser ces libraires. 

Ces biblio posent des questions de qui les produit ? Sur quelles données sont-elles entrainées ? 
Sociétés privées qui s'en occupent. 

Alice a cherché des librairies entrainées sur corpus de presse récente. 
Ça n'a pas fonctionné encore. 
On ne perd pas ESPOIR 

Ne fonctionne pas parce que la documentation est assez incomplète et le code proposé ne fonctionne pas quand on essaie de l'appliquer à ces propres données. Modèle difficilement reproductible. 
Même si accessible sur github, pas simple à faire fonctionner. 

Outil qui est conçu soi-disant pour normaliser les pratiques lol. Mais on n'est pas les seuls à rencontrer ces problèmes. 

Layout Parser : fait pour être utilisé par tous et pourtant ne fonctionne pas. 
ECD pense que c'est la chaîne de dépendance qui pose problème, on ne sait pas d'où viennent les erreurs 

### Outils de seg avec une interface UI

- [SegementAnything](https://segment-anything.com/) (meta) : 
outil de création de masques développé par Meta à partir d'un modèle de réseaux de neurones
fonctionnement avec Pyton 
Avec les même biblios
Seg panoptique 

Léa a trouvé les résultats très intéressants. 
possibilité de télécharger le code 
Moins intéressant pour Alice. 
pas même sens que L2a, reconnaissance d'objets, Alice ==> valeur sémantique des différentes parties de sa revue 

ECD est ce qu'on peut raffiner le modèle vu qu'il est générique? 

Il faut ensuite un traitement algorithmique pour analyser les rendus et mettre des étiquettes. 

- [e-Scriptorium](https://www.sofer.info/)
Libre et OpenSource
application fonctionnant avec Kraken pour la seg orientée OCR et la transcription des images. Possible d'y ajouter son propre modèle
cf Alix

- [Transcribus](https://readcoop.eu/transkribus/)
Logiciel pv 
base de modèles publique assez étendu, qui va jusqu'au début du XXe siècle
centré sur les écritures manuscrites

- [Abbyy Fine Reader](https://digital.abbyy.com/en-finereader-pdf-for-windows-request-trial-capterra.html?utm_source=capterra.com&utm_medium=cpc&utm_campaign=fr) :
logiciel pour l'océrisation de doc textuels, qui produit des fichiers ALTO avec les coordonnées de chaque bloc de texte ou graphique ainsi que les coordonnées de chaque lettre reconnue. 


Pas d'outils clefs en main, chacun répond à des besoins spécifiques 

## Evaluation de la perf des modeles 
Plusieurs métriques qui permettent d'évaluer la performance des modèles : 
- f1-score
- le score IoU (intersection over union)


### Identifier les erreurs possibles 
- erreur dans la seg des objets, ne prend pas en compte tous les pixels 
- erreur dans la seg et la classification des objets 
- erreur dans l'organisation des objets reconnus (Arkindex)
- erreurs liées à la multimodalité (textes et images poreux)

a essayé [CorDeep](https://cordeep.mpiwg-berlin.mpg.de/) : réseau cnn. 
plateforme entraînée sur les manuscrit de cosmologie. 
=> pas performant

Essai Scriptorium 
=> pas performant. A carrément généré texte d'une image de tapisserie. 

### Enjeux d'accessibilité, de reproductibiltié et d'interopérabilité 

nombreux outils et analog de seg multiples et tres hétérogenes qui fonctionnent tous dans env différents. Mais ammène à  question de formats de données. Comment faire quand corpus différents? Aussi sont créé dans  **Logique de projet** pour rep a projet spécifiques : enjeu de produire des outils générique, + prise en main rapide. Ce sont des outils qui évoluent rapidement aussi nombreux outils sont ainsi simplement abandonnés. 

les rentre interopérables 

accès restreint aux données d'entrainements et aux vérités de terrain. 

AI

Ne rendent pas public données d'entrainement pour chatgpt. 

question d'éthique des données, quels en sont les biais ? 

## Vers la création de standards pour l'annotation des images ? 

### Différents formats d'enregistrement 
Une fois qu'on a fait la seg on a des coordonnées dans les formats : 
- json 
- xml 
La forme pourrait être en svg, mais pas de standardisation en json. Alors que xml oui. 

### Différents schémas pour l'annotation des images 

VGG Annotator (json)
Tropy (json)

ALTO (xml) : permet de documenter les zones svg resultat et associer transcription. Doc num : faire surbrillance avec transcription dans le temps. 
PAGE XML : developpe specifiquement pour des développments HTR et capable d'integrer des metadonnées propres à la segmentation 
schemas pour les deux

Tentative de faire des standards json : COCO
Description 

- HTR-United
projet d'Alix
Reponds aux besoins de standards
Pas les modèles partagés mais les données de terrain des utilisateurs publiées sur Zenodo

- SegmOnto Documentation
ontology avec vocab controlé pour la mise en page. 

### Besoin de standards uniformisés pour la segmentation des images culturelles

Besoin de standards unifiés pour interopérabilité des modèles. 

Photographies du monde naturel marches mieux que images culturelles.

Pour leur projet font du transfert learning.

pas à partir d'images naturelles, mais de projets plus proches ==> meilleure performativité

standards également pour les annotations ? 

## Conclusion 
- les images culturelles ne peuvent pas être traitées comme des images naturelles 
- réfléchir a une éthique des données 
- besoin de standards de seg pour que des images déjà seg et classifiées puissent être réutilisées pour l’entraînement de nouveaux modèles 

Standards pour la segmentation ou annotation ? Plutôt annotation. 


Plusieurs points sont aujourd'hui centraux concernant la segmentation des images culturelles :
Elles ne peuvent pas être traitées au même titre que des images naturelles;
2. Il faut réfléchir à une éthique des données ;
3. Des standards de segmentation doivent être mis en place pour que des images déjà segmentées et classifiées puissent être réutilisées pour l'entraînement de nouveaux modèles ;
4. Les modèles et architectures doivent être disponibles en open source et en open access pour favoriser l'interopérabilité et la reproductibilité des résultats et de la recherche.
Il est crucial de responsabiliser les musées et les acteurs du domaine de l'histoire de l'art pour prendre en charge sérieusement et collectivement la question, pour que leur expertise soit mobilisée et pour éviter que les données culturelles ne soient appropriées par des acteurs privés.


Stratégie : partage des vecteurs pas seulement les images. partager de l'info sur l'image sans partager l'image. Représentation sous forme de tableau de vecteurs. 

