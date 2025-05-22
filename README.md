<h1 align="center">Jedha's ML Engineer Certificate</h1>
<h2 align="center">Bloc 2: Exploratory Data Analysis</h2>

<p align="center"><strong>Two Case Studies:</strong></p>

<p align="center">EDA: <em>Speed Dating</em><br>
Big Data: <em>Steam's Video Games Platform</em></p>



---

### Objectif du projet

L'équipe marketing de **Kayak** souhaite créer une application qui recommandera les **meilleurs destinations et hôtels français** en fonction :

- de la météo prévue dans les 7 prochains jours
- des meilleurs hôtels disponibles de la région 

---

### Données utilisées

- **35 villes françaises** issues de _OneWeekIn.com_
- Données météo via **OpenWeatherMap API**
- Coordonnées via **Nominatim API**
- Hôtels scrappés depuis **Booking.com** avec **Scrapy** :
  - Nom, coordonnées, note, description, URL

---

### Pipeline ETL

1. **Extraction**
   - API météo (OpenWeather)
   - Booking.com via un spider **Scrapy**
2. **Nettoyage & enrichissement**
3. **Stockage**
   - `.csv` enrichi stocké sur **AWS S3**
4. **Chargement**
   - Données chargées dans une **base PostgreSQL (AWS RDS)**

---

### Visualisation des résultats

#### Carte 1 : Top 5 des villes météo

- Créée avec **Plotly Express**
- Affiche les villes les plus "ensoleillées"
- Utilise un **score météo personnalisé** basé sur température, humidité, pluie, etc.

#### Carte 2 : Top hôtels par ville (Streamlit)

- Interface **Streamlit** avec **Folium**
- Sélection d'une ville → affichage des meilleurs hôtels (avec note disponible)
- Chaque hôtel contient :
  - Nom
  - Note
  - Description
  - 🔗 Lien vers Booking.com

---

### Technologies utilisées

| Outil / Tech       | Rôle                              |
| ------------------ | --------------------------------- |
| Python             | Langage principal                 |
| Pandas             | Traitement de données             |
| Requests           | Appels API météo et géocodage     |
| Scrapy             | Scraping structuré Booking.com    |
| Plotly             | Carte des meilleures destinations |
| Folium             | Carte hôtelière dynamique         |
| Streamlit          | Application web interactive       |
| AWS S3             | Stockage des données brutes       |
| AWS RDS (Postgres) | Entrepôt de données SQL           |

---

### Livrables

- Un fichier .csv dans un bucket S3 contenant des info enrichies sur la météo et les hôtels pour chaque ville française (code + captures d'écran (livrable - bucketS3))
- Une DB SQL Où l'on obtient les mêmes data nettoyées à partir de S3 (code + captures d'écran (livrable - DB))
- 2 cartes contenant un top 5 des destinations (du 24/04/2025 au 30/04/2025) et un top 20 des hôtels des 35 villes (livrable - maps))

---
