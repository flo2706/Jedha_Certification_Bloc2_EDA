<h1 align="center">Jedha's ML Engineer Certificate</h1>
<h2 align="center">Bloc 2: Exploratory Data Analysis</h2>

<p align="center"><strong>One Case Study:</strong></p>
<p align="center">Big Data Analysis – <em>The Steam Video Games Platform 👾</em></p>
<br>

---

### Contexte de l'entreprise

**Steam** est une plateforme de distribution numérique de jeux vidéo développée par **Valve**, lancée en 2003.  
Elle permet notamment :

- la gestion des mises à jour et des licences (DRM)  
- le jeu en ligne, le cloud gaming, et le stockage de sauvegardes  
- l’accès à une communauté : chat, messagerie, marketplace

Elle héberge des milliers de titres d’éditeurs tiers et indépendants.

---

### Objectif du projet

Vous travaillez chez **Ubisoft**, qui prépare la sortie d’un nouveau jeu vidéo.  
Votre mission : **réaliser une analyse exploratoire des jeux Steam** afin de mieux comprendre le marché du jeu vidéo et ses tendances.

> **Quels éditeurs, genres ou plateformes dominent ? Quels sont les facteurs de popularité ou de succès d’un jeu ?**

---

### 🖼️ Portée de l’analyse

- Analyse de données issues de la **marketplace Steam**
- Données semi-structurées stockées au format JSON
- Utilisation de **PySpark** sur **Databricks** pour :
  - nettoyer, transformer et agréger les données
  - créer des visualisations interactives
- Le dataset contient des informations sur :
  - les jeux (nom, note, date, genres, éditeur, plateforme…)
  - leur tarification, les réductions, et les langues
  - les retours utilisateurs (notes, commentaires)

---

### Questions d’analyse proposées

#### Analyse macro

- Quels éditeurs publient le plus de jeux ?
- Quelles années ont connu le plus de sorties ? (effet Covid ?)
- Quelle est la distribution des prix ? des remises ?
- Quelles langues sont les plus représentées ?
- Quelle part des jeux sont classés 16+/18+ ?

#### Analyse des genres

- Quels sont les genres les plus populaires ?
- Les genres les mieux notés ?
- Les genres les plus rentables ?
- Certains éditeurs ont-ils des genres favoris ?

#### Analyse des plateformes

- Les jeux sont-ils disponibles sur Windows / Mac / Linux ?
- Certains genres privilégient-ils une plateforme ?

---

### Données et technologies utilisées

| Outil / Tech       | Rôle                                       |
|--------------------|--------------------------------------------|
| **PySpark**        | Traitement des données volumineuses        |
| **Databricks**     | Environnement de notebook + visualisation  |
| **S3 Bucket**      | Stockage des données  |
| `explode()`, `getField()` | Manipulation de schéma imbriqué     |
| `groupBy()`, agrégats | Analyses par segment (genre/plateforme)  |

---

### Livrables

- Un **notebook Databricks** publié :
  - incluant le code PySpark
  - les graphiques intégrés
  - les interprétations

📎 Lien vers le notebook Databricks :  
➡️ [Voir le projet](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/282120262354643/2548154020458300/2219708563440839/latest.html)

---

### 📚 Source des données

Données disponibles sur S3 (données internes Jedha) :  
`s3://full-stack-bigdata-datasets/Big_Data/Project_Steam/steam_game_output.json`

---

