# Collaboratoire IA, 2e séance 23 mai 2025

## Introduction

Bienvenue à toutes et tous à cette 3e séance des collaboratoires du Partenariat *Des nouveaux usages des collections dans les musées d’art*. Nous poursuivons l’exploration des enjeux liés à l’utilisation de l’intelligence artificielle dans les musées avec une séance consacrés à la question du catalogage et de la documentation des collections.

On l’a vu avec la présence de nombreux secteurs lors du premier collaboratoire, les enjeux de l’utilisation de l’IA dans les musées concernent l’ensemble de la sphère d’activité muséale. Ces technologies s’insèrent au cœur des pratiques qu’il s’agisse du travail clérical quotidien, de la traduction, mais aussi des processus métiers. Et leur utilsation pose évidemment diverses questions professionnelles et éthiques.

Après avoir envisagé la question d’un point de vue général avec Emmanuelle Bermès lors d’une première séance, puis nous être arrêté plus spécifiquement sur la médiation avec les expériences du MNBAQ et du MetaLab d’Harvard, nous intéresserons plus particulièrement aujourd’hui au enjeux de la description, du catalogage ou de la redocumentation des collections.

Pour ce faire, nous avons le plaisir d’accueillir **Marion Charpier** qui travaille à l’École nationale des chartes et au MAD. 

Programme de la séance :

- Quelques mots d’introduction sur les enjeux (Emmanuel Chateau) notamment du côté des métadonnées
- Ensuite Camille Delattre présentera quelques exemples concernant l’utilisation de modèles vision computationnelle

Augmentation des processus métiers à travers l’ensemble des institutions GLAMs.

## Considérations

L’utilisation de l’IA dans les institutions patrimoniales offre de **nombreuses oportunité pour améliorer la découvrablité et l’utilisation des collections numérisées** à travers des mécanismes tels que la transcription audio ou textuelle, l’extraction de données structurées, la classification d’images, le géocodage des localisations ou la rectification géographique des plans. De plus, en mobilisant le public dans le cadre d’opérations de crowdsourcing, les institutions patrimoniales peuvent générer d’abondantes données structurées de grande qualité pour entraîner des algorithmes afin de pouvoir générer des données similaires à grande échelle.

Au delà du lissage des opérations d’inventaire, le cataloguage assistée par IA (AI-driven cataloging) prétend libérer les régisseurs de collections et le personnel de catalogage des tâches triviales et laborieuses du maintien des enregistrements, afin de leur permettre de s’engager plus directement avec les objets.

cf. exemple de discours publicitaire :

> Beyond streamlining inventory tasks, AI-driven cataloging liberates registrars and collection staff from the shackles of mundane record-keeping, granting them the freedom to explore and engage deeply with museum objects. (Berry 2023)
>
> Berry, Ana. 2023. « AI Cataloging ». *Museum Advocate* (blog). 23 août 2023. https://www.museumadvocate.org/data-review/.

Cette promesse est en partie contestable au sens où les catalogueurs fournissent habituellement des données d’autorités ce qui implique un important niveau de contrôle. Or les modèles actuellement utilisés reposent principalement sur des approches probabilistes, ne sont pas exempts de biais, et présentent des risques d’halucinations. Cela nécessite de bien circonscrire le périmètre d’intervention de la machine. D’autant que le succès de ces dispositifs repose également sur le fait de pouvoir disposer de données de références fiables.

Toutefois, il apparaît de plus en plus clairement que l’intelligence artificielle est amenée à occuper une place considérable dans les processus métiers au sein des musées soit comme instrument, soit comme infrastructure.

- incitations des vendeurs de produits logiciels
- conversion générique de la société

// avec Moteurs de recherche

Les discours sur l’IA tendent à prophétiser le remplacement de l’homme par la machine. On parle de **4e révolution industrielle** et certains n’hésitent pas à affirmer que près de 50% des tâches peuvent être automatisables.

Pour autant, **la machine n’élimine évidemment pas complètement le travail humain**. À un point ou un autre du processus, des interactions humaines sont requises. Qu’il s’agisse de fournir des données d’entraînement pour concevoir des modèles, ou bien de pouvoir les faire évoluer les ajuster à des tâches spécifiques (fine-tuning). Il faut également compter avec de nouvelles interactions homme-machine qui peuvent profondément transformer les chaînes de travail.

L’expression **Human-in-the-Loop machine learning** s’intéresse à la définition de nouveaux types d’interaction entre les humains et les algorithmes d’apprentissage machine (HITL-ML). Elle réfère à la nécessité d’une interaction humaine, d’une intervention, d’un contrôle ou d’un jugement pour contrôler ou changer la sortie d’un procesus. L’idée n’étant pas seulement de rendre l’apprentissage machine plus adapté ou obtenir le résultat précis plus rapidement mais également de rendre les humains plus effectifs et plus efficients (Mosqueira-Rey et al. 2023, p. 3006).

> A “human-in-the-loop” process in machine learning (ML) is one in which humans and algorithms work together to solve problems more efficiently and accurately than each could on their own. Algorithms attempt to solve problems at a much greater scale than humanly possible while humans offer feedback to algorithms in the form of model examples of successful answers or corrections of mistakes, iteratively improving the accuracy of the algorithms’ predictions. (Averkamp et al. 2021, p. 5)

Plusieurs étapes 

- **active learning**, dans lequel le système reste en contrôle du processus d’apprentissage et traite les humains comme des oracles pour annoter des données non-étiquettées
- **interactive machine learning** dans lquel il y a une interaction étroite entre les utilisateurs et les systèmes d’apprentissage, les utilisateurs fournissant interactivement des informations de manière plus spécifique et incrémentale
- **machine learning teaching**, où les experts du domaines ont le contrôle sur le processus d’apprentissage en délimitant le savoir qu’ils souhaitent transférer au modèle d’apprentissage machine

Certains systèmes attentifs à l’ordre d’apprentissage, ou encore à l’accessibilité. Débouche sur les termes de **Usable AI** ou **Useful AI**.

**Plateformisation ou externalisation**. Déplacement spatial du travail des données. On a de plus en plus recours à des services tiers au cours de ces processus, ce qui ne va pas sans poser des enjeux tant en terme de soutenabilité que de contrôle. Mais ces évolutions ont également des conséquences organisationnelles à l’égard des hiérarchies qui séparent le travail des données du travail sur les modèles. Sorte de **taylorisme digital** qui introduit une séparation entre la plannification et la mise en œuvre et qui valorise la chaîne verticale d’information et de contrôle et pourrait dévaluer les interactions horizontales qui permettent aux personnels d’apprendre directement de leurs pairs (Cole, Radice et Umney 2021, 91 à chercher).

Averkamp, Shawn, Kerri Willette, Amy Rudersdorf, et Meghan Ferriter. 2021. « Humans-in-the-Loop. Recommendations report ». Library of Congress, AVP.

LC Labs

## Travail métier et catalogage

Tâches

- Description
- Normalisation et harmonisation
- Alignements

Rapports professionnels (information et bib)

Cox, Andrew M. 2021. « Research Report: The Impact of AI, Machine Learning, Automation and Robotics on the Information Profession ». CILIP. https://www.cilip.org.uk/page/researchreport.

Pointe les enjeux de formation et liés aux référentiels de compétences

Rapport qui suggère un changement paradigmatique de la recherche en vue d’une lecture manuelle à l’extration de connaissance à partir de collections, de textes d’images ou d’autres données

Changements qui ont lieu à travers toute la chaine de valeur de l’information : depuis la production, l’organisation, à sa consommation.

ex. recherche web. Agents conversationnels 

enjeux pour les professionnels de l’information : défis organisationnels pour tirer parti de l’IA et des robots. Implique expertise dans le domaine des licences, le data stewardship, l’architetcure de données, éthique professionnelle. = compétences déjà existenates.

Rpositionnement nécessaire à l’égard de la pensée computationnelle.

## Human in the loop

Rapport de la LC Labs Bibliothèque du congrès 2021.

2020 rapport recommandant de rendre une grande partie de ses collections numérisées « online, ready for computation, and ready for users ». Nombreuses initiatives mobilisant les utilisateurs par le passé : FlickrCommons, Beyond Words, By the People program.

Lab engagé dans plusieurs expérimentations avec le ML depuis 2019.  Septembre 2019, Machine Learning + Libraires Summit où 75 institutions patrimoniales, praticiens et expers réunis. Programme d’innovateurs en résidence : Newspaper Navigator en 2020 (Ben Lee) ; collections musicales classification, extraction et assemblage pour hip hop (Brian For) ; état de l’art par (Ryan Cordell).

État de l’art produit par Ryan Cordell en 2020 qui pointait enjeux concernant les biais et la nécessité de réduction des risques. Pb de qualités des sorties issues du crowdsourcing, et la nécessité de communique aux utlisateurs les données produites automatiquement (vs autorités).

Hypotheses  

- Machine learning and crowdsourcing can be used together in engaging, ethical, and useful ways in data enrichment activities. 
- There are design approaches that can responsibly and clearly present human- and machine-generated metadata in digital collections discovery interfaces. 
- It is possible to create a repeatable approach/methodology for selecting collections, data pipelines, and tasks for ML and crowdsourcing workflows.
- It is possible to create a repeatable approach to identifying and engaging users.

Choix des collections

- important de consulter et d’inclure des experts des collections
- maintenir une liste de collections candidates
- réévaluer de manière continue les bénéfices, risques et biais pour chq collection candidate

Design

- Prototyper des taches pour mettre à jour les complexités assez tôt dans le processus de design
- investir outrils de prototypage
- planifier ground-truth testing
- faire des itw très tôt avec les volontaires
- designer community outreach plan

Implémentation

- Commit to continuous staffing of key machine-learning and community experts throughout the initiative.
- Conduct ground-truth testing to improve accuracy and monitor risk in machinelearning processes
- Iterate and improve upon crowdsourcing user experience through continued user testing

Presentation / sharing

- Build holistic approaches to safe and ethical user experiences
- Design interfaces that support data in varied states of accuracy and completeness
- Include UX Designers in the development of research and user experiences
- Test early prototypes and mockups with collection users and experts

## Axiell

Améliorer l’intégrité des données : L’IA identifie et corrige les erreurs, les incohérences et les doublons dans les enregistrements, garantissant ainsi la fiabilité des informations.
Accroître la capacité de recherche : L’IA génère des mots-clés pertinents et des balises sémantiques, facilitant la recherche d’objets spécifiques et la découverte de liens entre les œuvres.
Ajouter de la profondeur aux enregistrements : L’IA peut extraire des informations pertinentes à partir de sources externes, telles que des bases de données d’art, des biographies d’artistes et des articles de recherche, enrichissant ainsi les descriptions des objets.

En comparant Axiell à Transkribus, on constate qu’ils adressent des aspects différents de la gestion des collections. Transkribus se concentre sur la transcription de documents manuscrits, tandis qu’Axiell s’attaque à la structuration et à l’enrichissement des données existantes.

## NER ChatGPT

Opérations de normalisation de données

Tâche classique de reconnaissance d’entités-nommées NER

Utilisation de ChatGPT 

@todo exemples DH2024 Washington

## Lise Jaillant Aeolian Network

## Science Museum

## **John Stack** (Science Museum), Title:** *Machine Learning and Cultural Heritage: What Is It Good Enough For?*

V&A propose chose comparable. Propose connexion avec autres projets nationaux de connecter contenus. Question de recherche consiste à savoir dans quelle mesure le passage à l’échelle permet d’améliorer le catalogage des collections.

Lier les collections à Wikidata. Et à travers Wikidata à d’autres choses ou collections.

- Améliorer les interfaces de collections
- améliorer découvrabilité
- liens aux autres sources

AI, LOD, Knowledge Graph

Surtout utilisation de Machine learning

- Easy Wings : processing IDs and URLs (links)
- Disambiguation : adding new links to Wikidata chercher des personnes etx. et voir si peut faire une connexion. Fonctionne bien sur les personnes et les collections d’objets.
- NER Named Entity Recognition

Utilisation knowledge graph pour créer interfaces.

Widget.

**ML fonctionne pour**

- Intéressant pour suggérer des possibilités et mettre en lumière des connections.
- Identification de tendances et manques
- Visualisation étendue et diversité des collections.
- Identification contenus en rapport
- Travailler à l’échelle
- Apporter une nouvelle terminologie à côté du catalogue

**Mais**

- ML génère du contenu qui nécessite un encadrement ou des contextualisations.
- Faux positifs, pas toujours apparents et requiert savoirs de spécialistes.
- Notions de collections canonique mise en cause 
- comprendre ce que ne peut pas encore faire
- approches critique nécessaire.

GitHub.com/TheScienceMuseum/heritage-connector

 www.ai4lam.org

https://collection.sciencemuseumgroup.org.uk/api/objects/co159324

https://ai.harvardartmuseums.org/explore

On the Books corpus

https://github.com/UNC-Libraries-data/OnTheBooks/blob/master/workflow.md

Sur utilisation IIIF et Google

https://docs.google.com/document/d/19eVfnVoirwA462_GltwRLyscDQ6Jby4cW225tpCgdNw/edit#heading=h.ylsw36sxin6j

## Turing Institute et cartes 2020-2021

Creating a generalisable machine learning pipeline to process text on maps and catalysing humanities, scientific, and cultural heritage communities to use map text as data

https://www.turing.ac.uk/research/research-projects/machines-reading-maps

## Leveraging Large Language Models to Generate a Knowledge Graph for Italian Literary Texts

Cristian Santini

*This paper outlines a methodology for Knowledge Extraction from historical literary texts in Italian using a combination of Large Language Models and fine-tuned models for Relation Extraction. The research aims to offer a novel way to extract and represent entities and relations from literary manuscripts.*

Recherche sur Leopardi, nombreuses ressources numérisées.

Plusieurs approches dans le domaine de l’extraction des connaissances.

- sequence-to-sequence relation Extratcion Model
  - useful for end to end
  - based on Wikidata schema
  - souvent biais à l’égard relations simples (dates de naiss, lieu naiss)
- Zero or few-shor RE with LLM
  - mais pas de schéma fiable
  - prompt hallucination

Conrtibution évaluer instruction-tuned LLMs pour extratcion triplets sémantique de textes littéraire. Proposer un pipeline qui combine seq2seq models avec LLM. Encodage en TEI

Cas usage, semi-diplomatic edition 41 lettres autographes de Leopardi encodées en TEI. Facsimile disponibles.

Approchae conssite à traiter fichiers XML par script pour extraire métadonnées, auteur, titre et URI, représentation en CIDOC CRM puis pipeline extraction qui utilise différents outils extraction. Composant qui lie à entités Wikidata, pis troisième modèle sequence encoding.

Zero-shot RE avec ChatGPT --> requête.

Renvoie bien des triplets mais forme intermédiaire car doit exprimer en langage naturel. Pas possible utiliser efficacement.

Ce que fait récupérer triplet de GPT et renvoie à REBEL pour produire statement sous forme de phrase puis SPARQL pour importer action et propriétés logiques.

Mais pb. Filtering with SBERT car produisait des erreurs. Par exemple lieu de travail et lieu de mort. Utilisation sequence encodeur SBERT avec similarité possible de retirer statement inconsistants produits par ChatGPT.

Analyse erreurs. Baseline mREBEL qui est un moteur extraction... nb triplets extrait très faible 40, 4 corrects. 0.10, 18 unique reation. Avec ChatGPT trop de relations 662 triplets, 607 corrects, 0.92%, 400 unique relation.

Chat GPT + REBEL bien meilleur.

Avantages

Possible enrichir donnés synthétiques avec informations sémantiques issues de Wikidata. Haute fibabilité LLM même pour langue historique. Enhanced explainabiliy.

Limitation : vulnérable à des cascades d’erreur. Manque supervision humaine. Fiabilité limitée de LLM en raisons hallucinations.

Juste début. Fuet développer stratégie pour importer axiomes d’ontologies pour raisonner. Souhaite également améliorer le rafinage des triples. Inclure supervision humaine dans le processus. Utiliser KG pour supporter récupération augmented generation et autres tâhces. Q&R etc.

https://sntcristian.github.io/leopardi_kg/

## Bnf

## The MET

2019, COllaboration avec Microsoft et le MIT dans le cadre du programme OpenAccess

Preuve de concept Art Explorer : enrichir expérience utilisateur. Enrichissement des tags.

Choi, Jennie. 2019. « Exploring Art with Open Access and AI: What’s Next? » *The Metropolitan Museum of Art* (blog). 11 juin 2019. https://www.metmuseum.org/perspectives/met-microsoft-mit-exploring-art-open-access-ai-whats-next.

Enrichissement de données

Les musées maintiennent des métadonnées très descriptives de leurs collections. Mais souvent ces descriptions répondent avant tout à des modèles métiers qui s’alignent assez peu avec les besoins des utilisateurs. Ces métadonnés ne sont par ailleurs pas toujours standardisées.

--> utilisation IA possibilité d’enrichir l’indexation et la navigation dans les contenus.

Étiquetage, classification visuelle.

Projet subject-keywords dataset depuis 2018, hackaton avec MIT et Microsoft

Enjeux éthiques étiquetage --> importance de signaler les tags générés par ordinateur

## LUX

### Images and AI

Interagîr avec AI. Comment envisage interactions avec IA. Nombreuses images, mais aussi documents, données structurées et audio. Données générées. 

Tâche plus utile, transcription du contenu. Description des entités, résumés, classification, traduction et reconnaissance entité nommées.

En même temps souhiate que le système soit prédictible, reliable, performant, affordable, ethical, explainable, multilingue.

Impact environnemental dans le fait de faire tourner machine. Tâches que les humains peuvent mener.

Exemples de cas d’usage

- transcription écritures ms, dans plusieurs langages
- créer web accessibility text pour une image, ou pour une partie de l’image sélectionnée par un utilisateur
- catégorisation
- etc.
- créer linked data description, etc.
- répondre questions
- extraire données

Sans doute bientôt idem pour vidéos et modèles 3D.

AI requires accurate, relevant & big data. Pas d’institution qui possède ensemble du savoir vous. En utilisant les principes FAIR, et LOUD, peut combiner entre institutions approches qui produisent de la valeur internement plutôt que cout. Takeaway slide, celle là.

we must publish and use FAIR and LOUD data to fully leverage this technology to provide value to our community.

Exemple Béatrice Joyeux-Prunel, LUX layer sur GPT4o. Quel artiste Béatrice utilisa...

LUX CH Knowledge Graph, lieu de naissance, occupation, nationalité, etc. Titres etc. d’où viennent informations ? de diverses sources sur le web. Œuvres de la bibliothèque du congrès. Wikidata et national Library.  LOC. liens qui permettent de consulter plus info.

Graph Retrieval Augmented Generation pour overcome informations manquantes du graphe de connaissance. exemple catalogue exposition. demande même question mais en amenant information contextuelle du graph à l’agent...

Suggéré plusieurs artistes sur lesquels a publié. Pourquoi Kusama ? Un livre à paraître aujourd’hui.

Quid des images ? Connaît choses à propos des artistes. Montrer objets concernés. Très rapide avec IIIF et Linked Art. En mettant les données FAIR dans l’AI peut rendre choses très...

no single organization have all inforamtion about Picasso. But together, we do !

Putting the AI in FAIR

AI-powered knowledge enhancement. We can use modal AI to extract knowledge form images. But the What ?

Actuellement extraire provenance objets à Yale.

Handwritten and Printed Text. Exemple catalogue de vente en français. Écritures au 

Single operations, 100% correct

Autre exemple reçu de Matisse pour 4 peintures. Transcriptions. Très petits nombre d’erreurs. Surpris que pu lire ligne difficile.

Information extraction

Can FAIR-in-AI improve AI-in-FAIR ?

Human Readbel Provenance. Description dans le catalogue. Dans Lux les organisations mais pas liées au peintre encore.

Alors possibilité de marquer les contenus. Cercle vertueux qui permet de collecter contenus. Peut imaginer faire cela à l’échelle pour le projet sur les expositions de Béatrice. 

Près demi million de lieux. Place Description enrichment. Sujet du livre, histoire de Notre-Dame. Donner une description courte et formelle. Présentation dans les enregistrements. Bon travail à partir du contexte.

Expérimentation

Deux préocupations à discuter. Technocal model Collapse.

Dès lors que contenus AI augmente, entraînement sur ce contenu. 

Conclusion. OXford closed look. Stanford n’arrive pas. Data to AI to data peut devenir dangereux mais sans doute pas à cette échelle.

Question plus importante. Bias amplification. Grande majorité des coprus entraînement issu du web et terrible. S’assurer que communauté ait contribué.

Conclusions principes FAIR et LOUD et APIs, AIs comprenne le context des questions. EN particulier IIIF images and Linke Art semantics. AI can accurately extract knwoledge from imaegs. AI generated data peuvent enrich sparse data. The amplification of baisi in AI loops doivent être 

## Projet Ritter augmenté

Structuration automatique et extraction d’entités-nommées pour les fichiers biblio. Pour la BNU, utilisation IA à des fins patrimoniales un enjeu stratégique. Des envies et des idées dans les équipes. Des fonds exceptionnels sur lesquels peut travailler. Des compétences, même si important de pouvoir s’associer de nouvelles compétences dans ce domaine si l’on veut favoriser l’émergence de ces technologies. Master en technologie des langues de l’U de Strasbourg qui nous permet d’avoir des expertises fines sur le sujet. 

À l’occasion de différents projets que l’occasion de monter des partenariats et de travailler avec des chercheurs. En fonction des besoins des chercheurs. Mais aussi favoriser les partenariats.

Appel Equipex Biblissima+. Idée de Daniel Bornman responsable fonds patrimoniaux. Apporter ensemble de séquençage technique sur un outil savant. Répertoire bibliographique des livres imprimés en Alsace édité entre 1937 et 1960. Le but arriver à une dématérialisations structurée et enrichie.

- édition numérique sur la plateforme [Estrades](https://estrades.huma-num.fr) (Guillaume Porte)
- versement dans le portail Biblissima+

6650, 7000 entrées très structurées. Auteur titre, adresse bibliographique. Renvois vers les différents répertoires, cote et provenance. Très normé mais évolution en fonction des volumes. Pensait que proche ISBD.

Acquérir le texte OCR, lancement structuration semi-automatisée, puis reconnaissance entités-nommées avec leur alignement sur des référenciels et des répertoires bibliographiques. Outils reconnaissance entités-nommées : Spacy, et service Entity Fishing de HumaNum. Pensait pouvoir utiliser les informations de mise en page pour reconnaissance. Existence d’une table permettant de traiter les choses comme base de connaissance pour améliorer la reconnaissance. Idem noms de lieux. Abréviations. Dates.

Entités nommées très importantes pour pouvoir procéder à une étude intellectuelle. Analyse de réseau. Stage pour état de l’art et bibliothèques NLP. Tester en situation réelle les outils et les hypothèses de travail.

4 stratégies pour l’extraction, la reconnaissance et la classification des entités nommées

**Stratégie par règle** avec extraction sur texte brut avec expressions régulières : exploiter la base principale pour aller chercher les entités dans le texte. Sait ce que rentre mais peut de variabilité, pb océrisation, etc. qui rendent difficle

Table analytique des références

Expression régulière (expression syntaxique de chaîne)

**Comparer avec des modèles spécialisés dans la Reconnaissance entité nommées** en allant regarder ce qui était disponible sur Hugging Face entraîné sur grandes modèles de données et certaines tâches.

Gestion des mots inconnus

Avantage, gestion variants linguistiques. Mais pas de spécialisation sur nos données.

Très facile à utiliser, quelques lignes de codes seulement (5 lignes).

**Spécialisation sur un modèle de données.** Entraînement d’un modèle de type BERT sur nos données

- Adaptation à nos données
- peut avoir déjà bénéficié d’un pré-entraînement pour une tâche ou une langue
- mais demandeur de données

Préparation des données pour l’entrainement. Demande des connaissances en TAL. Etape préalable encodage XML. Puis prétraitement/tokenisation. Segmentation caractères et mots. Grands modèles de langues utilisent leur propre tokenizeur pour pouvoir gérer des mots jamais rencontrés. Donc nouvelle tokenization où mots inconnus divisés en token qui correspond à une sous-chaîne. Doit donc ensuite procéder à un alignement. Pas une tâche complexe mais nécessite connaissances.

**Modèles génératifs via interace web**

 Prompts pas de connaissance.

Varibilité des réponses, demande connaissance pour réintégration.

Exemple interaction avec Chat de Mistral pour la tâche NER. Fonctionne assez bien.

#### Evaluation

Annotation manuelle 50 pages, 214 notices annotées manuellement.

Moyenne F1 mesure capacité extraction et classification (zéro plus mauvaise, 1 meilleure)

Le modèle par règle le plus performant alors que ces stratégies qui étaient censées être dépassées. Ensuite Chat Mistral qui est le seul comparable. Modèle pré-entraîné sur nos données, une amélioration mais très faible. Surtout quand prend moyenne non-pondérée.

La classification automatique par ces modèles pas encore tout à fait généralisable. En tous les cas pas avec si peu de données annotées. Pourrait encoder plus de données mais risque de produire un modèle très spécifique à nos données. Questions sur les modèles génératifs pour rendre plus reproductible ces informations. Utilisation de la structure des notices pas encore exploitée. Pose donc la question d’intégration de ces traitements automatisés dans la chaîne numérique. Pose la question des volumes de données disponibles, comment les pré-traite, etc. Sans doute pas tout à fait au point même si du potentiel.

### Modèles CLIP





### *Kunstverkenner*/Art explorer (RijksMuseum), 2024

Faire des connexions à travers 800 000 artefacts

2012, un des premiers musées à rendre entièrement disponible en ligne sa colection numérisée

Faire des connexions entre collection de 800 000 œuvres d’art et les 500 000 ouvrages conservés dans sa bibliothèque.

>The Rijksmusum was the first museum to throw its collection open to the world. [...] We wanted to digitise the whole collection, including scanning the *Night Watch* in the greatest resolution ever, but there was so much more. The Rijksmuseum is a catalyst for scientific knowledge…but with 800,000 objects online, search was a challenge. We wanted to make them more accessible. (« Rijksmuseum Launches AI Tool to Help Make Connections in 800,000-Strong Collection » 2024)

### Harvard Art Museum

Harvard Art Museum, 53M tags et descriptions générées par ordinateur pour faciliter la recherche parmi les 380 000 images d’œuvres. Voir comment l’ordinateur voit l’art.

Smithonian Institute pour recherche interne 

Un outil qui fait des comparaisons.

Thorne H

https://www.chartes.psl.eu/recherche/centre-jean-mabillon/projets-de-recherche/torne-h-traitement-dobjets-par-reconnaissance-numerique-en-environnement-humain-henrot

## Museum + AI

Murphy, Oonagh, et Elena Villaespesa. 2020. « AI: A Museum Planning Toolkit ». The Museums + AI Network. Londres: Pratt, Goldsmiths University of London. https://themuseumsai.network/toolkit/.

## Réflexions

Catalogage, production des autorités et responsabilités du musée.

Processus de qualité

## Présentation de Marion Charpier

Cheffe de projet intelligence artificielle au MAD

Après une thèse de doctorat consacrée au Dragon à l’époque médiévale à l’EHESS soutenue en 2020, Marion Charpier a intégré le Master Technologies numériques appliquées à l’histoire de 2022 - 2023. Son travail de fin d’étude portait déjà sur l’utilisation de l’IA pour travailler sur l’important fonds de l’artiste décorateur Jean Royère conservé dans les collections du MAD.

Elle est aujourd’hui chercheuse principale du projet TORNE-H dirigé par Emmanuelle Bermès au Centre Jean-Mabillon, et porté par le Musée des Arts Déco. L’objectif de cette recherche est de démontrer la valeur ajoutée des méthodes de *computer vision* pour analyser des collections muséales non décrites et d’étudier **l’impact de l’intégration de l’IA dans les processus de travail du musée**.

## Divers

Responsible operation sur IA, Thomas Padilla

Padilla, Thomas G. 2018. « Collections as data: Implications for enclosure ». *College & Research Libraries News* 79 (6) : 296. https://doi.org/10.5860/crln.79.6.296.

Padilla, Thomas, Laurie Allen, Hannah Frost, Sarah Potvin, Elizabeth Russey Roke, et Stewart Varner. 2019. « Always Already Computational: Collections as Data ». Final report. Collections as Data. Consulté le 7 juillet 2021. https://doi.org/10.5281/zenodo.3152935.

———. 2019. « Responsible Operations: Data Science, Machine Learning, and AI in Libraries ». OCLC Research Position Paper. OCLC. Consulté le 7 juillet 2021. https://doi.org/10.25333/xk7z-9g97.

Nicole Coleman, https://library.stanford.edu/people/cnc
