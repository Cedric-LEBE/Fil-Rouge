# 🛒 Projet Fil Rouge - Prévision des Ventes E-commerce

## 📋 Description

Application interactive de prévision des ventes e-commerce basée sur l'apprentissage automatique et l'analyse de séries temporelles. Ce projet permet d'anticiper les ventes futures en exploitant des données transactionnelles historiques complexes pour optimiser la gestion des stocks, la planification logistique et les stratégies marketing.

## 🎯 Objectifs

L'objectif principal est de concevoir une application interactive permettant de :

1. **Prédire les ventes futures** sur différentes granularités temporelles (journalière, mensuelle)
2. **Fournir des indicateurs clairs** et interprétables pour la prise de décision
3. **Rendre les résultats accessibles** via une application interactive Streamlit

### Objectifs détaillés

#### 1️⃣ Compréhension et préparation des données
- Explorer et comprendre les différentes tables du dataset e-commerce
- Analyser la qualité des données (valeurs manquantes, incohérences, distributions)
- Fusionner les tables pertinentes pour construire des datasets analytiques cohérents

#### 2️⃣ Analyse Exploratoire des Données (EDA)
- Étudier l'évolution des ventes dans le temps
- Identifier les tendances, saisonnalités et cycles récurrents
- Analyser les ventes par type de produit, région géographique, mode de paiement
- Mettre en évidence les corrélations entre variables

#### 3️⃣ Feature Engineering orienté séries temporelles
- Créer des variables temporelles pertinentes (jour, mois, trimestre, année)
- Générer des features de séries temporelles (lag features, moyennes glissantes)
- Construire des variables métier utiles à la prévision

#### 4️⃣ Modélisation et prévision des ventes
- Modèles statistiques : ARIMA, SARIMA, Holt-Winters
- Modèles de Machine Learning : Régression, Random Forest, XGBoost
- Modèles spécialisés : Prophet
- Évaluation avec métriques adaptées (MAE, RMSE, MAPE)

#### 5️⃣ Restitution et déploiement
- Concevoir des visualisations interactives
- Déployer via une application Streamlit avec filtres dynamiques
- Préparer le projet pour une intégration MLOps

## 📊 Dataset

Le projet utilise des données e-commerce multi-tables incluant :

- **df_Orders.csv** - Commandes avec statuts et dates
- **df_OrderItems.csv** - Détails des articles commandés
- **df_Customers.csv** - Informations clients
- **df_Payments.csv** - Modes et montants de paiement
- **df_Products.csv** - Catalogue de produits

Les données sont organisées en deux ensembles :
- `data/train/` - Données d'entraînement
- `data/test/` - Données de test

## 🚀 Installation

### Prérequis

- Python 3.10 à 3.12
- pip ou uv pour la gestion des dépendances

### Installation des dépendances

```bash
# Cloner le repository
git clone https://github.com/Cedric-LEBE/Fil-Rouge.git
cd Fil-Rouge

# Créer un environnement virtuel
python -m venv .venv

# Activer l'environnement virtuel
# Sur Linux/Mac:
source .venv/bin/activate
# Sur Windows:
.venv\Scripts\activate

# Installer les dépendances
pip install -e .
```

## 📁 Structure du Projet

```
Fil-Rouge/
├── data/
│   ├── train/          # Données d'entraînement
│   │   ├── df_Customers.csv
│   │   ├── df_OrderItems.csv
│   │   ├── df_Orders.csv
│   │   ├── df_Payments.csv
│   │   └── df_Products.csv
│   └── test/           # Données de test
├── notebooks/
│   ├── Business Understanding.ipynb
│   ├── models_trainning.ipynb
│   └── Untitled-2.ipynb
├── src/
│   └── projet_fil_rouge/
│       └── __init__.py
├── pyproject.toml
├── Readme.md
└── .gitignore
```

## 💻 Usage

### Exploration des données

Les notebooks Jupyter permettent d'explorer et comprendre les données :

```bash
# Lancer Jupyter
jupyter notebook

# Ouvrir les notebooks dans notebooks/
# - Business Understanding.ipynb : Compréhension métier et EDA
# - models_trainning.ipynb : Entraînement des modèles
```

### Application Streamlit (à venir)

```bash
# Lancer l'application Streamlit (une fois développée)
streamlit run app.py
```

## 🛠️ Technologies Utilisées

### Analyse et Traitement de Données
- **pandas** - Manipulation de données
- **numpy** - Calculs numériques

### Visualisation
- **matplotlib** - Graphiques statiques
- **seaborn** - Visualisations statistiques
- **plotly** - Graphiques interactifs

### Machine Learning
- **scikit-learn** (v1.5.0) - Modèles ML classiques
- **xgboost** - Gradient boosting
- **statsmodels** - Modèles statistiques (ARIMA, SARIMA)
- **prophet** - Prévisions de séries temporelles

### Déploiement
- **streamlit** - Application web interactive
- **python-dotenv** - Gestion de configuration

### Utilitaires
- **joblib** - Sérialisation de modèles

## 🎯 Fonctionnalités

### Actuelles
- ✅ Exploration et analyse des données e-commerce
- ✅ Notebooks d'analyse métier
- ✅ Infrastructure de données multi-tables

### En développement
- 🚧 Pipeline de feature engineering
- 🚧 Entraînement et comparaison de modèles
- 🚧 Application Streamlit interactive
- 🚧 Système de prévision en production

### Roadmap
- 📋 Intégration MLOps
- 📋 Monitoring des modèles
- 📋 API REST pour les prévisions
- 📋 Déploiement containerisé (Docker)

## 📈 Métriques d'Évaluation

Les modèles sont évalués selon :
- **MAE** (Mean Absolute Error) - Erreur absolue moyenne
- **RMSE** (Root Mean Square Error) - Erreur quadratique moyenne
- **MAPE** (Mean Absolute Percentage Error) - Erreur en pourcentage

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :
1. Fork le projet
2. Créer une branche pour votre fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. Commiter vos changements (`git commit -m 'Add some AmazingFeature'`)
4. Push vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrir une Pull Request

## 📝 Contexte Métier

Dans un contexte e-commerce, la capacité à anticiper les ventes futures est un levier stratégique majeur pour :
1. Optimiser la gestion des stocks
2. Améliorer la planification logistique
3. Ajuster les stratégies marketing et promotionnelles
4. Maximiser le chiffre d'affaires tout en réduisant les coûts opérationnels

Les ventes e-commerce sont influencées par de nombreux facteurs : saisonnalité, comportements clients, types de produits, modes de paiement, localisation géographique, et conditions de livraison.

## 📄 Licence

Ce projet est un projet académique dans le cadre d'une formation en Data Science et Machine Learning.

## 👥 Auteur

Développé dans le cadre du projet Fil Rouge de formation en Data Science.

---

**Note** : Ce projet est en cours de développement. Certaines fonctionnalités sont encore en phase d'implémentation.
