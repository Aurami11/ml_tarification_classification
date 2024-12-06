# Projet de Tarification - Prédiction de Risque de Sinistre

## Description

Ce projet vise à développer un modèle de tarification pour prédire le risque de sinistre en utilisant des techniques de machine learning. Plusieurs modèles de classification ont été utilisés pour estimer les probabilités associées aux sinistres. Le projet comprend également un travail approfondi de feature engineering et d'analyse de données.

## Modèles Utilisés

- **AdaBoost**
- **Gradient Boosting**
- **Random Forest**
- **XGBoost**

Chaque modèle a été évalué pour sa capacité à prédire avec précision les risques de sinistre associés à chaque client.

## Installation

1. Clonez ce dépôt :

   ```bash
   git clone https://github.com/votre-utilisateur/projet-tarification.git
   cd projet-tarification
   ```

2. Créez un environnement virtuel et installez les dépendances :

   ```bash
   python -m venv env
   source env/bin/activate  # Sur Windows, utilisez `env\Scripts\activate`
   pip install -r requirements.txt
   ```

## Résultats

Les modèles ont été évalués à l'aide de plusieurs métriques, y compris l'AUC, la précision, le rappel et le F1-score.
Tous les modèles utilisés avaient des performances similaires mais Gradient Boosting et Random Forest se demarquaient avec AUC = 0.6 et Accurancy = 0.94 à la prémière analyse avec toutes les features, à la deuxième avec un data set plus propre après reduction de dimension des variables catégorielles encodées, tous les modèles maximisaient les metrics de test utilisés

## Contributeurs

- Jules D'ALMEIDA
