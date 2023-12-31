# Implémentez un modèle de scoring
## Présentation:
L'entreprise Prêt a dépenser, société financière, propose des crédits à la consommation pour des personnes ayant peu ou
pas du tout d'historique de prêt.
Cette entreprise souhaite mettre en oeuvre un outil de "scoring crédit" pour calculer la probabilité qu'un client
rembourse son crédit
puis classifie la demande en crédit accordé ou refusé.
Elle souhaite développer un algorithme de classification en s'appuyant sur des sources de données variées (donées
comportementales, données provenant d'autres institutions financières, etc)

De plus, les chargés de relation clients ont fait remonter le fait que les clients sont de plus en plus demandeurs de
transparence vis-à-vis des décisions d'octroi de crédit.
Cette demande de transparence des clients va tout à fait dans le sens des valeurs que l'entreprise veut incarner.

Prêt à dépenser décide donc de développer un dashboard interactif pour que les chargés de relation client puissent à
la fois expliquer de façon la plus transparente possible les décisions d'octroi de crédit, mais également permettre à
leurs clients de disposer de leurs informations personnelles et de les explorer facilement.
## Mission:

- Construire un modèle de scoring qui donnera une prédiction sur la probabilité de faillite d'un client de façon automatique.
- Construire un dashboard interactif à destination des gestionnaires de la relation client permettant d'interpréter les prédictions faites par le modèle, et d’améliorer la connaissance client des chargés de relation client.
- Mettre en production le modèle de scoring de prédiction à l’aide d’une API, ainsi que le dashboard interactif qui appelle l’API pour les prédictions.

## Construction:
Dans ce dépôt, vous trouverez plusieurs fichiers:

- "script.py" : code contenant la préparation des données, l'entraînement et la configuration du modèle de classification
  (LGBMClassifier).
- "app.py" : code permettant de déployer le modèle sous forme d'API.
- "dashboard.py" : code permettant de généer le dashboard.
- "data_drift.zip" : tableau HTML d'analyse de data drift réalisé à partir d'evidently.
- "datadrift.ipynb" : notebook permettant de générer le tableau d'analyse de data drift réalisé à parti d'evidently.
- "feature_importances.py" : code permettant de générer les shap values pour les feature importances.
- "test_id_to_index", "test_prediction", "test_valid_id" : code permettant de générer des tests unitaires. 
- "model.pkl", "model_knc" : modèles enregistrés au format pickle. 
- "shap_val.pickle" : shap values enregistrées au format pickle pour les feature importances.
## Données:
- Les données ont été téléchargés à cette adresse : https://www.kaggle.com/c/home-credit-default-risk/data

- Kernel Kaggle utilisé pour facilité l'analyse exploratoire, la préparation des données et le feature engineering
  nécessaire à l'élaboration du modèle de scoring : https://www.kaggle.com/code/jsaguiar/lightgbm-with-simple-features/script

## Packages:
Différents packages Python ont été utilisés:

- mlflow 2.1.1
- pandas 1.4.4
- numpy 1.23.5
- scikit-learn 1.0.2
- lightgbm 3.3.5
- imbalanced-learn 0.10.1
- scipy 1.9.1
- plotly 5.9.0
- shap 0.41.0
- requests 2.28.1
- streamlit 1.20.0
- matplotlib 3.5.2
- evidently 0.2.8
- pytest 7.4.0
- Flask 1.1.2

## Compétences:
- Définir et mettre en œuvre une stratégie de suivi de la performance d’un modèle
- Évaluer les performances des modèles d’apprentissage supervisé
- Utiliser un logiciel de version de code pour assurer l’intégration du modèle
- Définir la stratégie d’élaboration d’un modèle d’apprentissage supervisé
- Réaliser un dashboard pour présenter son travail de modélisation
- Rédiger une note méthodologique afin de communiquer sa démarche de modélisation
- Présenter son travail de modélisation à l'oral
- Déployer un modèle via une API dans le Web
- Définir et mettre en œuvre un pipeline d’entraînement des modèles