---

title: Réunion hebdomadaire
author: ouvroir
date: 2023-09-06
draft: 
tags:
     - cr

---

# Réunion hebdomadaire
## admin
Horaire William:
- Lundi: 13h - 18h (présentiel au besoin)
- Mercredi: 8h - 13h (présentiel)
- Jeudi: 16h - 21h (présentiel au besoin)

proposition de faire la clinique numérique le lundi pour pouvoir alterner William 

déplacer les portes ouvertes au 23 octobre pour que william puisse être là? 
à confirmer la semaine prochaine

relance INSO faite
réponse FEI, qu’on accepte en demandant des précisions sur la réserve de 20%

Coût poste CIÉCO
Nous nous apprétons à faire les transferts du compte du Partenariat vers celui du FCI. 
Michael a versé 4 000 sans demande de précision. Mais pour être absoluement clair avec tout le monde, j’aurais aimé pouvoir indiquer le coût réel d’un poste de travail et le détail de l’opération.

Date rencontre IIIF
Martin Sévigny indique que la Bibliothèque a choisi sa solution pour un serveur IIIF. Il s’agit de la solution DSPace bien établie dans les bibliothèques et connue pour sa robustesse. Celle-ci devrait, selon lui, permettre de servir nos besoin en terme d’API. Toutefois la solution ne supporte pas la dernière version du protocole (que les bibliothèques aimeraient développer) ni les manifestes. Il reste par ailleurs à préciser la mission des Bibliothèques. Notre projet pouvant constituer un pilote mais c’est à négocier.


Licence Adobe
Le compte Adobe a été créé avec l’adresse ouvroir@umontreal.ca Il restait à Colin de lier le compte avec la commande pour pouvoir faire l’installation.


## Coordo

Display: projet de documentation d'accrochages de collection CIÉCO+Ouvroir
Ontologie CIDOC-CRM: modèle conceptuel avec des notions formalisées par l'ICOM

Zoë: études en conservation, mémoire sur la restauration d'une exposition «Feux pâles» 2017
réalisée par l'artiste Philippe Thomas
- questinner si une exposition est un médium
- mettre à l'épreuve la restauration/conservation
- utilisation des techniques de conservation pour les œuvres immatériels et les time-based media art. 
- considérer l'exposition dans sa globalité hors-temps, cartographie en réseau des traces et informations retrouvées
- Feux pâles considéré comme un réseau qui sortait du temps
- toute activation, dont parler de l'exposition (incluant le mémoire), fait partie de l'exposition
- rapport documentaire : recherches physiques, entrevues ect. 
    - plan d'exposition: pas à jour, a re-produit un plan à partir des photos
    - gestion incertitude, diachronie
    - document utilisable mais difficilement exploitable dans ce format
    - contient également des constats d'état à partir des informations recuellies 
    - aide à la prise de décisions pour les activations 

Responsable du LUMA Arles
- pas d'archives d'exposition
- archives sur un serveur disparates: excel, word, feuilles, ...
- a créé une bd relationnelle avec FileMaker Pro
- pensé comme un prototype, coûte moins cher à produire
- base de données comme outil de gestion, qui alimente les archives

Prototype Novart produit avec l’entreprise [Novarem](https://www.novarem.com)
Intégration des informations logistiques. Production du PSO. 
Gestion des prêts, outil de documentation des constats d’état. Arrivée et départ, informations sur le transport des éléments (composantes des œuvres). Douane, et assurances, etc. Gestion des profils pour les droits.
danger: donner des informations qui ne sont pas à jour à des gens qui pourraient s'en servir. Expot en pdf pour contrôler l'information.

David
- entités et relations à présenter dans le modèle
- début du développement de l'ontologie, phase d'exploration
- qu'est-ce-qu'une exposition ? 
- définir les types de relations topologiques qu'on veut définir entre les expôts

parti pris sort de CIDOC pour tester un modèle davantage centré sur la topologie. 
- comment on prend en compte la diachronie ? 
- chronologie de l'accrochage est complexe, orientation événement compliquerait beaucoup la description. 

Extension de CIDOC pour l'archéo => travail sur les strats. Utilisation ou non ? 

À quel point l'outil doit-il être lié au modèle? 
- gestion distincte dans l'outil puis modèle de diffusion et export? ou utilisation du modèle pour l'outil 

Modèle porrait servir pas juste à documenter mais aussi à planifier des expositions