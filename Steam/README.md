<h1 align="center">Jedha's ML Engineer Certificate</h1>
<h2 align="center">Bloc 2: Exploratory Data Analysis</h2>

<p align="center"><strong>One Case Study:</strong></p>
<p align="center">Big Data Analysis – <em>The Steam Video Games Platform 👾</em></p>
<br>
<p>Link to the Databrickx Project: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/282120262354643/2548154020458300/2219708563440839/latest.html</p>
---

### Contexte de l'entreprise

Steam est une plateforme de distribution numérique de jeux vidéo développée par **Valve**, lancée en 2003. Elle permet :

- la gestion des mises à jour et licences (DRM)  
- le jeu en ligne, le cloud gaming, et le stockage de sauvegardes  
- l’accès à une communauté (chat, messagerie, marketplace)

Elle héberge des milliers de titres d’éditeurs tiers et indépendants.

---

### Objectif du projet

Vous travaillez chez **Ubisoft**, qui prépare la sortie d’un nouveau jeu vidéo révolutionnaire.  
Votre mission est de **réaliser une EDA approfondie de la marketplace Steam** afin de mieux comprendre :

- les éditeurs dominants  
- les genres de jeux les plus populaires  
- l’évolution du marché mondial  
- les préférences par plateforme (Windows, Mac, Linux)

---

### Données utilisées
=> s3://full-stack-bigdata-datasets/Big_Data/Project_Steam/steam_game_output.json
---

### Questions d’analyse proposées

#### Analyse « macro »

- Quels éditeurs publient le plus ?  
- Quelles années ont vu un pic de sorties ? (Covid, etc.)  
- Quelles langues sont les plus fréquentes ?  
- Quelle est la répartition des prix ?  
- Quelle part de jeux est interdite aux mineurs ?

#### Analyse des genres

- Quels genres sont les plus fréquents ?  
- Quels genres sont les mieux notés ?  
- Quels genres sont les plus rentables ?  
- Certains éditeurs ont-ils un genre préféré ?

#### Analyse des plateformes

- Répartition des jeux par OS (Windows/Mac/Linux)  
- Existe-t-il des affinités plateforme-genre ?

---

### Données et technologies utilisées

| Outil / Tech       | Rôle                                       |
|--------------------|--------------------------------------------|
| **PySpark**        | Traitement des données en cluster          |
| **Databricks**     | Notebooks + visualisation interactive      |
| **S3 Bucket**      | Stockage des données (JSON semi-structuré) |
| `explode()`, `getField()` | Manipulation de champs imbriqués     |
| `groupBy()`, agrégats | Analyses segmentées par genre/année      |

---

### Livrables

- Un ou plusieurs **notebooks Databricks** contenant :
  - le traitement PySpark  
  - les visualisations intégrées

---
