---
title: Réunion avec CalculQc
description: cr de la réunion du 7 novembre
author: ouvroir
date: 2022-11-07
draft: true
tags:
    - cr

---
# CalculQc

Présences
- Lydia Vermeyden
- Suzanne Talon

Lydia: nouveau poste - développement de nouveaux services à Calcul Québec
- aquisition d’un ordinateur quantique: débroussaillage de ce qu’il faut faire
- quels sont les services à développer pour les SHS? rôle transformateur pour toute la communauté pour démocratiser l’accès au numérique pour ces chercheurs

Somme FCI pour une infrastructure numérique: devis initial avec deux options (un très gros montant, un plus petit)
- nécessite des services de sys admin: on a trouvé un prestataire, coûte cher mais qui connaît le milieu (recherche, CalculCanada) et familier avec le CD/CI
- dépense d’argent doit être justifiée (service qualifié, quantifié et bien déterminé)

Pouvons-nous partir sur une option plus basse avec un service cloud? 
- pas du RAC (pas tant de limite), concours d’allocation [RAS](https://docs.alliancecan.ca/wiki/Cloud_RAS_Allocations) a une limite: accès rapide
- quel est le service dans ce cas? 
- comment le faire pour que ça serve à d’autres?

La chose pas claire pour moi était de savoir si on a réellement besoin d’acheter du matériel, mais on a besoin du service.
Services dont a besoin clairement identifiés.

Cherchent toujours à recruter un sysadmin. Poste toujours en affichage.
Est-ce qu’on pourrait travailler avec Tim? 
> facturation :
> Timothée Guicherd - travailleur indépendant enregistré à Amsterdam, Pays Bas
> Kamer van Koophandel nummer: 66593646

IaaS (infrastructure as a service) chez Google par exemple
Cloud brut chez CalculQc: requiert installation et configuration par les chercheur·se·s, risqué et mal géré

Partage de coûts pour payer Tim? 

Ressources matérielles: 
- requiert une quantification
- ce ne sont pas les ressources cloud qui manquent
- l’argent serait mieux investi dans des services
- ce qui est fait en développement doit pouvoir être rattrapé en maintenance par CalculQc, d’où l’idée d’impliquer Lydia et Sarah
- CalculQc n’a pas le droit de vendre du service pour le FCI
- obligation FCI de fonctionner sur 5 ans et pas 3

Projets Kubernetes, Docker, et Wordpress à l’Alliance
Procédures de déploiement qui utilisent Ansible, etc.

Aller parler au FCI? 
- possibilité de convertir la dépense de matériel en développement logiciel
- quel coût pour l’accès aux ressources sur 5 ans? 
- requiert un accord clair sur l’utilisation de l’argent, les ressources auxquelles ont a accès. Modèle différent car cloud mais équivalent à ce qui était prévu dans le devis

Savoir s’ils peuvent s’engager formellement à promettre les ressources matérielles alors qu’au-dessus du RAC actuel.
Pourrait quantifier les limites en machines virtuelles, etc.

Possible de réattribuer les sommes pour le FCI.
Investir dans le développement logiciel en collaboration avec CQc.

Lydia a travaillé sur un projet avec ACENET l’année dernière pour développer travail avec Sysadmin sur le réseau. Pourrait demander le résultat du projet. 3 projets Omeka, word press et bdd.

Partager ce qu’on a proposé avec Tim: cadre avec objectifs (milestones)
1. première infrastructure plutôt classique type LAMP avec nodejs, java, avec automatisation pour le déploiement + sauvegarde
2. bacs à sable
3. automatisation et amélioration des mécanismes

Créer une instance persistante, recommandation de Félix-Antoine Fortin (qu’on a rencontré en mars). Comme c’est sur un disque physique on peut redimensionner sans tout casser. Il y a moyen d’avoir des volumes de stockage.

évaluer combien au-dessus du RAC on serait
travailler sans avoir à redéposer les données si on a besoin de redimensionner

comment on s’organise pour travailler si on investit l’argent dans du développement pour être efficaces?
déterminer le type d’automatisation le plus approprié au cas d’usage

- [ ] Renvoyer la description des services à Suzanne 
- [ ] Première étape écrire une lettre pour le FCI
Recommandation écrite par Suzanne, qu’Emmanuel relit.
Envoyer à Edna avec Jean-François dans la boucle, pour envoyer au FCI.
- [ ] Organiser une rencontre avec Lydia + Sarah + Tim
- [ ] Mise en place d’une instance persistante en échappant au RAC avec Lydia

Spécifications:
- rubans de sauvegardes
- adresses IP 2 puis sous-ip


Autres sujets: 
- Léa (CNRS; humanum) IA vision automatisée
- Alix HTR eScriptorium (mises à jour régulières)