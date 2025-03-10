# Projet de Tarification - Prédiction de Risque de Sinistre

## Description

Ce projet vise à développer un modèle de tarification pour prédire le risque de sinistre en utilisant des techniques de machine learning. Plusieurs modèles de classification ont été utilisés pour estimer les probabilités associées aux sinistres. Le projet comprend également un travail approfondi de feature engineering et d'analyse de données.

## Modèles Utilisés

- **AdaBoost**
- **Gradient Boosting**
- **Random Forest**
- **XGBoost**
- **HistGradientBoosting**

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

# Rapport sur les Résultats des Modèles de Classification

Ce projet évalue plusieurs modèles de classification utilisés pour prédire la survenance de sinistres dans un contexte d'assurance automobile. Les modèles ont été évalués en utilisant différentes métriques de performance, notamment l'AUC-ROC, la précision, le rappel, et le F1-score, pour déterminer leur capacité à prédire les sinistres, en particulier dans un contexte de données déséquilibrées.

## Résumé des Performances des Modèles

Les modèles de classification testés sont les suivants : **Gradient Boosting**, **Logistic Regression**, **Random Forest**, **XGBoost**, **Adaboost**, et **HistGradient**. Tous les modèles ont montré des performances similaires, avec des AUC autour de **0.64**, mais une différence notable a été observée dans la capacité à prédire correctement la classe 1 (sinistre).

| **Modèle**           | **AUC** | **Accuracy** | **Précision (Classe 1)** | **Rappel (Classe 1)** | **F1-score (Classe 1)** |
|----------------------|---------|--------------|--------------------------|-----------------------|-------------------------|
| **Gradient Boosting** | 0.64    | 0.94         | 0.00                     | 0.00                  | 0.00                    |
| **Logistic Regression**| 0.59    | 0.94         | 0.00                     | 0.00                  | 0.00                    |
| **Random Forest**     | 0.64    | 0.57         | 0.09                     | 0.66                  | 0.16                    |
| **XGBoost**           | 0.63    | 0.94         | 0.00                     | 0.00                  | 0.00                    |
| **Adaboost**          | 0.62    | 0.94         | 0.00                     | 0.00                  | 0.00                    |
| **HistGradient**      | 0.64    | 0.94         | 0.00                     | 0.00                  | 0.00                    |

### Observation des Résultats

1. **Précision et Rappel** :
   - Les modèles comme **Gradient Boosting** et **Logistic Regression** présentent une précision élevée pour la classe majoritaire (classe 0), mais une performance extrêmement faible pour la classe 1 (sinistre).
   - Le modèle **Random Forest** a montré un meilleur rappel pour la classe 1 (66%), ce qui est important pour identifier les sinistres.

2. **Distribution des Probabilités Prédites** :
   - Les probabilités prédites pour chaque observation ont montré deux pics distincts dans la distribution des **probabilités d'accident** :
     - **Premier groupe** : Fréquences relativement faibles (entre **0.35 et 0.50**), représentant le groupe le plus large.
     - **Deuxième groupe** : Fréquences plus élevées (entre **0.50 et 0.60**), représentant un groupe plus petit mais à **risque plus élevé**.

### Analyse des Variables Importantes

Les **importances des caractéristiques** (feature importances) du modèle **Random Forest** montrent que certaines variables sont particulièrement significatives pour prédire la survenance de sinistres :

- **La taille de la souscription de la police d'assurance** : Plus le montant de la souscription est élevé, plus le risque d'un sinistre est important.
- **L'âge du véhicule** : Les véhicules plus anciens présentent un risque plus élevé.
- **L'âge de l'assuré** : Les assurés plus jeunes ou plus âgés peuvent présenter un risque plus élevé.

Ces résultats ouvrent la voie à des analyses plus approfondies, par exemple via des courbes de **Partial Dependence** (PD) pour mieux comprendre l'impact de chaque caractéristique.

### Recommandations Stratégiques

1. **Segmentation des Clients** :
   - Compte tenu des deux groupes distincts observés dans la distribution des probabilités, il serait judicieux de procéder à une **segmentation des clients** selon leur risque de sinistre. Cela permettrait de mieux ajuster les **primes d'assurance** et de rendre l'offre plus **compétitive**.

2. **Tarification Différenciée** :
   - Pour le groupe à **risque élevé** (probabilités entre 0.50 et 0.60), les primes pourraient être augmentées.
   - Pour le groupe à **faible risque** (probabilités entre 0.35 et 0.50), les primes pourraient être réduites pour les rendre plus **attractives**.

3. **Amélioration du Modèle** :
   - Bien que le modèle **Random Forest** soit performant, il existe des possibilités d'améliorer les résultats via l'**ajustement des hyperparamètres** ou l'utilisation de techniques comme l'**oversampling/undersampling** pour gérer le déséquilibre de classe.

4. **Exploration des Variables avec Partial Dependence** :
   - L'utilisation des courbes **Partial Dependence** pourrait être un excellent moyen d'explorer l'impact des variables clés sur la probabilité d'un sinistre et affiner davantage les recommandations.

### Conclusion

Bien que les modèles aient montré des performances inégales, le modèle **Random Forest** a permis d'identifier des segments de clients à risque élevé. Ces segments peuvent être utilisés pour ajuster la **tarification** et mieux gérer le **risque** dans le portefeuille d'assurance. Une segmentation précise et une approche de tarification différenciée peuvent améliorer la compétitivité des primes tout en minimisant les pertes dues à des sinistres mal classifiés.

L'utilisation des **Partial Dependence** pour analyser les relations entre les variables et le sinistre peut encore affiner ces résultats.

---

## Contributeurs

- Jules D'ALMEIDA
