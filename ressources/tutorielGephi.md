---
title: "**Tutoriel Gephi pour les historiens de l'art**"
desccription: ""
creationDate: ""
lastUpdated: ""
tags:
  - ""
draft: true
contributors:
  - ""
---

# **Tutoriel Gephi pour les historiens de l'art**

Gephi est un outil puissant d'analyse de réseaux qui peut être particulièrement utile aux historiens de l'art qui étudient les relations entre les artistes, les mouvements, les mécènes et les œuvres d'art. Voici un tutoriel complet pour vous aider à démarrer.

## Reste du contenu

**Pour commencer**

**1.**   **Télécharger et installer Gephi**

- Visitez gephi.org et téléchargez la version compatible avec votre système d'exploitation
- Suivez les instructions d'installation

**2.**   **Comprendre l'interface**

- Vue d'ensemble : L'endroit où vous visualisez et manipulez votre réseau
- Laboratoire de données : Où vous gérez vos tableaux de données
- Aperçu : Où vous affinez la visualisation finale

**Préparation des données**

Pour la recherche en histoire de l'art, vous devrez créer deux fichiers CSV :

1. **Fichier de nœuds** : Contient des entités (artistes, œuvres d'art, mécènes, etc.)

   - Chaque ligne représente une entité

   - Doit inclure une colonne « Id » avec des identifiants uniques

   - Peut inclure des attributs supplémentaires tels que « Name », « Type », « Era », etc.

2. **Fichier d'arêtes** : Représente les relations entre les entités

   - Doit inclure les colonnes « Source » et « Target » (référençant les ID du fichier des nœuds)

   - Peut inclure le « Type » (dirigé/non dirigé) et le « Weight » (force de la connexion).

Exemple nodes.csv :

Id,Label,Type,Era

1,Leonardo da Vinci,Artist,Renaissance

2,Mona Lisa,Artwork,Renaissance

3,Louvre Museum,Institution,Modern

Example edges.csv:

Source,Target,Type,Weight

1,2,Created,1

2,3,Housed in,1

**Importation de données**

1. Ouvrez Gephi et créez un nouveau projet
2. Allez dans Fichier > Importer une feuille de calcul et sélectionnez votre fichier de nœuds.
3. Sélectionnez les options appropriées et cliquez sur « Suivant » puis « Terminer »
4. Répétez le processus pour votre fichier d'arêtes (edges)

**Analyse de base des réseaux**

1. **Mise en page** :

   - Allez dans le panneau de mise en page (en bas à gauche)

   - Essayez ForceAtlas 2 pour une disposition initiale.

   - Cliquez sur « Run » pour l'appliquer, puis sur « Stop » lorsque les nœuds s'installent.

2. **Filtrage** :

   - Utilisez le panneau Filtres (à droite) pour mettre en évidence des connexions spécifiques.

   - Par exemple, filtrez par nationalité d'artiste ou par période de temps

3. **Statistiques** :

   - Exécuter des mesures telles que la modularité (pour détecter les communautés)

   - Calculer le degré (nombre de connexions)

**Visualisation des données historiques de l'art**

1. **Apparence des nœuds** :

   - Taille des nœuds en fonction de leur importance (panneau de classement)

   - Colorier les nœuds en fonction d'attributs tels que la période ou le mouvement

2. **Apparence des arêtes** :

   - Ajuster l'épaisseur en fonction de la force de la relation

   - Utiliser différentes couleurs pour différents types de relations

3. **Étiquettes** :

   - Afficher les noms des nœuds importants

   - Ajuster la taille et la couleur de la police pour une meilleure lisibilité

**Exemple d'étude de cas : 
Les réseaux de mécénat de la Renaissance**

1. Créer des nœuds pour les artistes, les mécènes et les œuvres d'art
2. Créer des arêtes pour les relations (commandité, créé, financé)
3. Appliquer la mise en page de ForceAtlas 2
4. Colorier les nœuds par type (artistes, mécènes, œuvres d'art)
5. Dimensionner les nœuds par degré (nombre de connexions)

**Techniques avancées**

1. **Ligne du temps** :

   -  Utilisez la fonction de chronologie pour visualiser les changements au fil du temps.

   -  Idéal pour suivre l'évolution des mouvements artistiques

2. **Disposition géographique** :

   - Placer les nœuds sur une carte géographique

   - Utile pour visualiser les échanges artistiques entre les régions

3. **Détection des communautés** :

   - Exécuter l'algorithme de modularité pour identifier les communautés artistiques

   - Colorier les nœuds en fonction des communautés détectées

**Exporter votre visualisation pour inclure 
 dans vos publications ou présentations**

1. Passez à l'espace de travail Preview
2. Ajustez les paramètres pour les couleurs, les bords, les étiquettes
3. Exporter en SVG, PDF ou PNG

**Ressources pour les historiens de l'art**

·   Exemples de données sur les réseaux artistiques historiques

·   La section « Arts » du forum Gephi

·   Plugins spécifiques à l'histoire de l'art

·   Tutoriels spécifiques à l'analyse des réseaux du patrimoine culturel
