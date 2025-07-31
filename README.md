# Analyse et Modélisation de la Popularité des Jeux Vidéo sur Steam

![Steam Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Steam_icon_logo.svg/512px-Steam_icon_logo.svg.png)

---

## Présentation

Ce projet vise à analyser un large dataset de jeux vidéo disponibles sur la plateforme Steam afin de comprendre les facteurs qui influencent leur popularité. Par la suite, plusieurs modèles de machine learning sont testés pour prédire la popularité d’un jeu à partir de ses caractéristiques (tags, genres, prix, années de sortie, modes de jeu, etc.).

L’objectif final est de fournir un modèle performant et interprétable, capable d’aider à la recommandation ou à l’analyse des tendances du marché des jeux vidéo.

---

## Données

- **Source** : Dataset public Steam (version de 2019)
- **Taille** : 27 334 jeux, ~400 colonnes (tags, prix, dates, etc.)
- **Volume** : environ 84 MB en mémoire

### Données importantes

- `release_year` : année de sortie
- `price` : prix du jeu
- `tags` : genre et style (action, indie, rpg, simulation, etc.)
- `developer` : Développeurs du jeu.

---

## Outils et Technologies

- **Python** (pandas, numpy, scikit-learn, matplotlib, seaborn)
- **Jupyter Notebook** pour l’exploration, la modélisation et la visualisation
- **Git & GitHub** pour le versioning et partage du code

---

## Analyse Exploratoire

- Nettoyage et traitement des données manquantes et aberrantes
- Analyse des distributions, corrélations et tendances clés
- Visualisation des relations entre les tags, genres, popularité, ...
- Feature engineering sur les dates et les catégories

---

## Modélisation

- Modèles benchmarké :
  - Régression Logistique
  - Random Forest Classifier
  - Gradient Boosting
  - Perceptron Multi-Couches (MLP)
- Optimisation des hyperparamètres pour la random forest 
- Évaluation avec F1 score, précision, rappel

### Résultats clés

| Modèle              | F1 Score |
|---------------------|----------|
| Random Forest       | 0.762     |
| MLP Classifier      | 0.646    |
| Régression Logistique | 0.640  |
| Gradient Boosting    | 0.523    |

---

## Interprétation du modèle final (Random Forest)

- Les features les plus importantes sont :  
  `release_year`, `price`, certains tags.
- Le modèle confirme que les caractéristiques liées aux genres, modes de jeu et date de sortie jouent un rôle majeur dans la popularité.

---

