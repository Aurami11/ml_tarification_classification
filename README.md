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
Tous les modèles utilisés avaient des performances similaires mais Gradient Boosting et Random Forest se demarquaient avec AUC = 0.6 et Accurancy = 0.94.
Tous les modèles classifiaient assez mal, la survenance d'un sinistre pour le modèle donnant les résultats les plus optimistre, Random Forest, l'on avait 
Precision : 0.08 et Recall : 0.52.

Ainsi dans une optique de tarification, il serait peut etre meilleur de faire de la mutualisation de risque pour revenir à un modèle deterministe si l'on est averse au risque (risque de modèle élevé) sinon on peut faire de la segmentation en deux groupes d'individu.
## Contributeurs

- Jules D'ALMEIDA
