# Spotify Analysis — Analyse et Segmentation de Chansons

Projet d'analyse exploratoire et de segmentation de chansons Spotify à partir d'un jeu de données public de 32 828 titres.

## Table des matières

- [Présentation](#présentation)
- [Jeu de données](#jeu-de-données)
- [Techniques utilisées](#techniques-utilisées)
- [Stack technique](#stack-technique)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Structure du projet](#structure-du-projet)

---

## Présentation

Ce projet applique des méthodes d'analyse de données et d'apprentissage automatique non supervisé sur des chansons Spotify afin de découvrir des groupes de titres partageant des caractéristiques audio similaires.

L'objectif est de comprendre comment les chansons se regroupent naturellement selon leurs attributs musicaux (énergie, dansabilité, acoustique, etc.) et de visualiser ces structures en basse dimension.

---

## Jeu de données

Source : [TidyTuesday Spotify Songs](https://github.com/rfordatascience/tidytuesday) (données publiques, aucune clé API requise)

| Caractéristique | Valeur |
|-----------------|--------|
| Nombre de chansons | 32 828 |
| Nombre de colonnes | 23 |
| Nettoyage appliqué | Suppression des valeurs nulles (nom de titre, artiste, album) |

Variables audio analysées :

| Variable | Description |
|----------|-------------|
| danceability | Aptitude au mouvement et à la danse |
| energy | Intensité et activité perçue |
| acousticness | Probabilité que le titre soit acoustique |
| instrumentalness | Absence de voix dans le titre |
| speechiness | Présence de paroles parlées |
| liveness | Présence d'un public en direct |
| valence | Positivité émotionnelle transmise |
| loudness | Volume sonore moyen (en dB) |
| tempo | Rythme en battements par minute (BPM) |
| duration_ms | Durée du titre en millisecondes |

---

## Techniques utilisées

- **Clustering hiérarchique** : regroupement des chansons par similarité audio sans supervision
- **ACP (Analyse en Composantes Principales / PCA)** : réduction de la dimensionnalité pour simplifier la représentation des données
- **t-SNE** : visualisation en 2D de données de haute dimension pour explorer la structure des clusters
- **Arbre de décision** : classification supervisée pour interpréter et valider les groupes identifiés

---

## Stack technique

| Composant | Outil |
|-----------|-------|
| Langage | Python 3 |
| Environnement | Jupyter Notebook |
| Manipulation des données | pandas, numpy |
| Machine Learning | scikit-learn |
| Visualisation | matplotlib, seaborn, plotly |

---

## Installation

1. Cloner le dépôt :

```bash
git clone https://github.com/Aminata11052000/Spotify-Analysis.git
cd Spotify-Analysis
```

2. Créer et activer un environnement virtuel :

```bash
python -m venv venv
source venv/bin/activate      # Linux / macOS
venv\Scripts\activate         # Windows
```

3. Installer les dépendances :

```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly jupyter
```

4. Lancer Jupyter Notebook :

```bash
jupyter notebook
```

---

## Utilisation

Ouvrir le fichier `Projet_Data_Viz.ipynb` dans Jupyter Notebook et exécuter les cellules dans l'ordre.

Le notebook suit la progression suivante :

1. Chargement et exploration du jeu de données
2. Nettoyage des données
3. Analyse des distributions des variables audio
4. Réduction de dimensionnalité (PCA, t-SNE)
5. Clustering hiérarchique et visualisation des dendrogrammes
6. Classification par arbre de décision
7. Interprétation des clusters et conclusions

---

## Structure du projet

```
Spotify-Analysis/
├── Projet_Data_Viz.ipynb    # Notebook principal d'analyse
└── README.md
```
