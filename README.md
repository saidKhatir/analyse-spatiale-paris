# Analyse géospatiale – Ville de Paris (M2, cours Boris Merisckay)

Ce dépôt regroupe **3 scripts/notebooks** réalisés dans le cadre d’un cours de Master 2 (Boris Merisckay).  
Objectif : explorer des jeux de données Open Data de la **Ville de Paris** dans leurs dimensions **attributaire** et **spatiale** (nettoyage, statistiques descriptives, jointures spatiales, cartographie, carroyage, maillage H3).

---

## Contenu du dépôt

### Séance 1 — Espaces verts & Arbres
- Téléchargement et exploration des **espaces verts** (CSV)
- Nettoyage / typage (pandas)
- Agrégations (par catégorie, arrondissement) + graphiques
- Téléchargement et exploration des **arbres** (CSV)
- Nettoyage (filtrage valeurs aberrantes) + graphiques
- Export d’un tableau d’agrégation en Excel

### Séance 2 — Vélib & IRIS
- Import des couches **IRIS** et **Vélib** (GeoJSON)
- Préparation des données (centroïdes, reprojections)
- Statistiques descriptives sur les stations Vélib
- Création d’indicateurs (taux de dispo / occupation, typologie émettrice/réceptrice)
- Cartographie thématique (matplotlib + contextily) + carte interactive (folium)
- Jointure attributaire avec données population/logement (CSV) et cartographie

### Séance 3 — Jointures spatiales, agrégations & maillages
- Import IRIS, Vélib, réseau cyclable (GeoJSON)
- Calculs métriques (surfaces, longueurs)
- Jointures spatiales (stations ↔ IRIS, pistes ↔ IRIS, arbres ↔ IRIS)
- Agrégations et cartographies (points proportionnels, choroplèthes)
- Carroyage régulier (grille) + agrégation
- Maillage hexagonal **H3** (Uber) + cartographie

---

## Données utilisées (sources)
- Ville de Paris Open Data : espaces verts, arbres, Vélib, réseau cyclable
- IRIS (Île-de-France / INSEE via plateforme)
- Données population/logement (via export ArcGIS)

> Les données sont téléchargées automatiquement dans les scripts via `wget` (ou à adapter en `requests` si besoin).

---

## Prérequis
- Python 3.9+ recommandé
- GDAL / dépendances géospatiales (selon OS)
- Bibliothèques principales : `pandas`, `geopandas`, `shapely`, `contextily`, `mapclassify`, `folium`, `matplotlib`, `seaborn`, `h3`, `openpyxl`

---

## Installation (pip)

### 1) Créer et activer un environnement virtuel
```bash
python -m venv .venv
source .venv/bin/activate        # macOS/Linux
# .venv\Scripts\activate         # Windows
