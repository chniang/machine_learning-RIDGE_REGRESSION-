# 📡 Prédiction de la consommation d'énergie 5G avec Régression Ridge

## 🎯 Objectif du projet

Ce projet s'inscrit dans le cadre d’un défi mondial organisé par l’Union Internationale des Télécommunications (UIT) en 2023. L’objectif est de **modéliser la consommation d’énergie des stations de base 5G** à l’aide de techniques d’apprentissage automatique, en particulier la **régression Ridge**.

Les stations de base consomment plus de 70% de l’énergie totale du réseau, et les dépenses opérationnelles (OPEX) atteignent près de 25% des coûts totaux d’un opérateur. Ce projet vise donc à aider à **prédire cette consommation** en fonction de plusieurs variables techniques, afin d’optimiser les performances énergétiques.

---

## 🧠 Problématique

Comment prédire avec précision l'énergie consommée par des stations de base 5G, en tenant compte :
- des configurations techniques,
- du trafic réseau,
- et des stratégies d’économie d’énergie ?

---

## 🧾 Données utilisées

Le jeu de données fourni est une version simplifiée d’un dataset collecté par l’UIT. Il contient :
- des mesures de trafic cellulaire (4G/5G),
- des configurations techniques,
- des caractéristiques temporelles,
- et la variable cible : **l’énergie consommée**.

📷 *Aperçu du dataset* :  
![aperçu du dataset](https://i.imgur.com/Agu9zeP.jpg)

---

## ⚙️ Étapes réalisées

1. **Chargement et exploration des données**
   - Analyse de structure, types de variables, valeurs manquantes.
   - Création d’un rapport automatique avec `ydata_profiling`.

2. **Prétraitement**
   - Gestion des valeurs manquantes.
   - Suppression des doublons.
   - Suppression des valeurs aberrantes via Z-score.
   - Encodage des variables catégorielles.
   - Standardisation avec `StandardScaler`.

3. **Modélisation**
   - Séparation des données (`train_test_split`).
   - Entraînement d’un modèle de **régression Ridge**.
   - Évaluation des performances du modèle.

4. **Évaluation**
   - `Mean Absolute Error (MAE)`
   - `Mean Squared Error (MSE)`
   - `R² Score`

---

## 📊 Bibliothèques utilisées

```python
pandas, numpy, matplotlib, seaborn, ydata_profiling,
scikit-learn (Ridge, train_test_split, StandardScaler, metrics),
scipy (zscore)
