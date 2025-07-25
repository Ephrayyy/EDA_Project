
# 💳 Détection de Fraude sur des Transactions Bancaires

## 🧠 Problématique

Comment analyser les transactions bancaires pour identifier des schémas de fraude ?

---

## 📁 Contenu du projet

Ce projet repose sur l’analyse d’un dataset de transactions bancaires (fichier `creditcard.csv`) pour détecter les cas de fraude, très rares mais critiques. Le jeu de données présente une forte déséquilibre entre classes (0 pour "non frauduleux", 1 pour "frauduleux").

---

## 📥 Téléchargement du jeu de données

Le jeu de données n'est pas inclus dans ce dépôt car il dépasse la limite de 100 Mo de GitHub.

👉 **Lien vers Kaggle** : [Credit Card Fraud Detection – Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

### Instructions :

1. Créez un compte sur [Kaggle](https://www.kaggle.com/) si ce n'est pas déjà fait.
2. Acceptez les conditions d'utilisation du dataset.
3. Téléchargez le fichier `creditcard.csv` et placez-le à la racine du projet.

---

## 🔧 Technologies utilisées

- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- LightGBM
- Scipy

---

## 🔍 Étapes du projet

### 1. **Chargement et exploration des données**
- Lecture du fichier `creditcard.csv`
- Visualisation de la distribution de la variable cible (`Class`)
- Analyse des corrélations avec `pearsonr`, `spearmanr`, `normaltest`

### 2. **Préparation des données**
- Séparation des données en features et cible
- Split en jeu d’entraînement et de test

### 3. **Modélisation**
- Utilisation d’un **StackingClassifier** combinant :
  - XGBoost
  - LightGBM
  - Logistic Regression en tant que méta-modèle
- Optimisation avec `GridSearchCV`

### 4. **Évaluation**
- Évaluation via `classification_report`
- Calcul de l'AUC avec `roc_auc_score`

---

## 📊 Résultats attendus

- Une meilleure détection des fraudes malgré l’extrême déséquilibre des classes.
- Des scores d’AUC supérieurs à ceux d’un simple modèle linéaire.
- Une approche interprétable grâce à l'utilisation de modèles de boosting.

---

## 📂 Arborescence du projet

```
.
├── New_Project.ipynb        # Notebook principal
├── creditcard.csv           # Jeu de données (à placer ici après téléchargement)
└── README.md                # Ce fichier
```

---

## ✅ À faire / Pistes d’amélioration

- Implémenter des techniques de rééquilibrage (SMOTE, undersampling…)
- Ajouter des métriques adaptées aux classes déséquilibrées (f1-score, confusion matrix)
- Intégrer SHAP pour l’interprétabilité des modèles

---

## 👤 Auteur

Ephraïm Kossonou  
Étudiant en Data Science à Aivancity
