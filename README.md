# Prédiction de la Consommation Énergétique, électricity (Time Series Forecasting)

Ce projet vise à modéliser et prédire la consommation énergétique à partir de données temporelles. Plusieurs approches sont comparées, allant des modèles statistiques (ARIMA) aux réseaux de neurones profonds (CNN, LSTM, GRU, Conv1D).

## 📁 Structure du projet

```
time-series-forecasting/
│
├── data/
│   └── pic-journalier-consommation-brute.csv
│
├── tuner_lstm/
├── tuner_conv/
│
├── best_lstm.h5
├── best_conv1d.h5
├── arima_model.joblib
│
├── Time Series Pipeline.py
├── README.md
└── requirements.txt
```

## 🚀 Modèles Utilisés

- **ARIMA / Auto-ARIMA** : pour modéliser des dépendances linéaires dans le temps.
- **LSTM** : un RNN conçu pour capter des dépendances temporelles complexes.
- **Conv1D** : réseau convolutif 1D adapté à la détection de motifs locaux dans les séries temporelles.

## 📊 Données

Le dataset `pic-journalier-consommation-brute.csv` contient des valeurs de consommation d'électricité (et potentiellement d'autres variables explicatives) à fréquence journalière. La première colonne représente la variable cible.

## 🔧 Fonctionnalités

- Analyse exploratoire (EDA)
- Prétraitement : traitement des valeurs manquantes et des outliers
- Feature engineering (extraction de caractéristiques temporelles)
- Mise à l’échelle des données (standardisation)
- Découpage temporel en ensembles d'entraînement, validation et test
- Création de séquences pour les réseaux profonds
- Entraînement avec Keras Tuner pour le réglage d’hyperparamètres
- Sauvegarde des meilleurs modèles
- Évaluation des modèles via MSE et visualisation des prédictions

## ✅ Exécution

```bash
python "Time Series Pipeline.py"
```

## 📌 Résultats

- Les performances des modèles sont comparées avec la MSE (Mean Squared Error).
- Visualisations des prévisions vs. données réelles disponibles pour :
  - ARIMA
  - CNN
  - LSTM
  - GRU
  - Conv1D

## 📦 Dépendances

Liste partielle des packages requis (voir `requirements.txt`) :
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- statsmodels, pmdarima
- tensorflow, keras-tuner

Installation recommandée :

```bash
pip install -r requirements.txt
```

## 💡 Améliorations possibles

- Intégration d’autres variables corrélées comme inputs (features multivariées)
- Tests avec d’autres architectures (Transformer)
- Déploiement avec Streamlit ou Dash pour créer un dashboard interactif

---

🧠 _Réalisé par : Marc Thierry NANKOULI,
                  Abdoulaye Chaibou,
                  El Filali Halima
                - Élèves ingénieurs en IA et Data Technologies._
