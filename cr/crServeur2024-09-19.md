---
title: Rencontre avec Calcul Québec du 19 septembre 2024
description: Compte-rendu de la rencontre
author: ouvroir
date: 2024-09-19
draft: true
tags: 
    - serveur
    - FCI
    - cr
---

## Cr Réunion avec Calcul Qc pour les serveur 23 septembre 2024

Réunions précédentes

- octobre 2023 : Emmanuel + Suzanne FCI Innovation
- 29 septmbre 2023 : FCI innovation Michael + Suzanne + Emmanuel
- 30 novembre 2022 : Rdv BRDV modification budget FCI
- **10 novembre 2022 : Projet de lettre modification demande FCI**
- 7 novembre 2022 : Rencontre avec Calcul Québec : Lydia Vermeyden et Suzanne Talon
- 26 octobre 2022 : Rencontre avec Calcul Québec : Pier-Luc St-Onge, Meghan Landry
  Sarah Cameron-Pesant
- 2 septembrre 2022 : Rencontre avec Koumbit (infogérance)
- 3 mars 2022 : Rencontre de suivi avec Félix-Antoine Fortin
- 6 janvier 2022 : Emmanuel Château, Jean-François St-Pierre, Pier-Luc St-Onge, Lydia Vermeyden, Suzanne Talon, Lena Krause

Lettre de novembre 2022, dont la formulation avait été rejetée par Edna

> Lors de la préparation de la proposition, il avait été envisagé de faire l’acquisition d’un serveur de calcul (30 554 $), qui serait intégré à l’infrastructure infonuagique de Calcul Québec, afin d’héberger les applications, de la plateforme collaborative et des données de recherche. Ce serveur devait également permettre la création de machines virtuelles, destinées à servir de « bac-à-sable » pour le développement de nouveaux logiciels.
>
> Suite aux discussions récentes avec Calcul Québec, nous aimerions reprofiler cette **somme afin d’embaucher une personne qui développera les intergiciels (*middleware*) requis pour l’exploitation efficace de l’infrastructure**. Les ressources infonuagiques seront obtenues via le service d’accès rapide de l’Alliance de recherche numérique du Canada (ARNC), ou via le concours d’allocation annuel lorsque les besoins grandiront. Les premières machines virtuelles sont déjà disponibles pour débuter le projet. Le développement des intergiciels sera fait en collaboration avec l’équipe de Calcul Québec, sous la direction de la Directrice du développement des nouveaux services à la recherche. Les axes de développement seront choisis afin de répondre aux besoins du projet tout en s’assurant de la compatibilité avec les outils développés par Calcul Québec et l’ensemble des partenaires de la fédération canadienne. L’équipe de Calcul Québec continue à s’engager à offrir une pérennité des infrastructures matérielles et logicielles de base hébergeant la plateforme ainsi que de l’aide ponctuelle et des services-conseils tout au long de la durée de vie du projet. 

 

Engagement sur fournisseur des ressources
30000 - 2600 pour nas local 


Lina Marie nouvelle reccrue analyste avec chercheurs. 

- Lydia congé prolongé
- Sarah congé prolongé 

Lina débuté au mois d’avril. Sarah et Lydia reviennent au mois de janvier.

Demander une prestation de service admin.
La lettre de Suzanne avait bloqué de notre coté. 

Besoin de taille d’infrastructure : Rack de base : probleme d’adresse IP. 
On veut ajouter une recopie à distance. 
On va faire tourner des app java, mais l’idée est d’avoir aussi des bacs à sable. 
Docker ajoute aujourd’hui plus de complexité que necessaire pour nous. Super outil pour deployer mais effet boite noire cad facile de ne plus savoir ce qui est dans ton image. 

Création d’images Docker, mais difficile de savoir ce que contient l’image. Facile de perdre le contrôle.

Quelque chose qui va très bien dans la philosopohie du projet GDR. Ne veulent pas gérer les VM à la place des chercheurs pour ne pas prendre la responsabilité 

Par contre, on aimerait vous donner les recettes complètes pour tester vous même les choses. Ce que l’on voudrait faire pour les HN. Vous donne des recettes éprouvées, vous envoie des courriels pour les mises à jour. Puis devenir plus confortable en même temps que l’on peut vous appuyer.

Rester dans l’environnement que l’on supporte. Ne pas commencer à tout démonter. Peut s’assurer d’avoir les versions compatibles.

C’est exactement ce que nous voulons. Pour héberger : 
- bases de données
- dispositif deployable depuis git

Actuellement déménagement infra de backup de Sherbrooke. Cet automne.

Si résume (faire un point avec Aurélien, Sophie et Marie-Jean), Semaine prochaine

Liste de logiciel supportés par Calcul Quebec (envisage Git hub)
Voir comment interagir ensemble
- Projet pilote Emmanuel et Doris (GDR) outils speech to txt
- [LibreQDA](https://cirst.uqam.ca/activites/midi-bin-phun-demonstration-du-projet-logiciel-libreqda-pour-lib/) (invivo), CIRST

FCI devrait avoir une facture physique. Jean-François revient lundi.
- Acheter un seveur 10-15000
- Avec le reste dépenser embauche étudiant pour travailler avec Aurélien (UdeM), Lina et Sophie

Payer du salaire passé en offrant du service futur. Embauche beaucoup d’étudiants pour force de travail.

Avoir qqun pour dev avant que Sara revienne. Aurélien fera le dev principal, Sarah pour l’accompagnement. 

- soumission pour le stockage avec entretien
- écriture comptable pour les salaires étudiants. 

Aurélien payé sur différents fonds. Alliance, MEIE, etc. Sans recoupement avec autres enveloppes.

- Faire une liste des spécifications techniques
- Rencontre avec Lina et Marie-Jean/Aurélien et Sophie / Caroline + Pierre Luc
- Tester la possibilité avec Edna (salaire rétro UdeM)
- Mail récap à Edna avec Suzanne en cc (expliquant situation congés, )

Faire un ticket sur
- support@tech.alliancecan.ca