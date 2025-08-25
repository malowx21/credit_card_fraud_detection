# Credit Card Fraud Detection

## Objectif
Ce projet a pour but de développer un modèle de **détection de fraude bancaire** à partir de données de transactions.  
Les fraudes sont rares par rapport aux transactions normales, ce qui crée un **problème de classification déséquilibrée**.  
L’objectif est de créer un modèle capable de **repérer les transactions frauduleuses avec un maximum de précision**, tout en limitant les faux positifs.

## Dataset
- Source : [Kaggle - Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- 284 807 transactions dont seulement 492 frauduleuses (~0.17%).  
- Les données sont **anonymisées** et les variables principales sont issues d’une **analyse en composantes principales (PCA)**.  
- Format : CSV, stocké dans le répertoire `data/` (géré avec Git LFS).

## Méthodologie
1. **Prétraitement**
   - Standardisation des variables
   - Gestion du déséquilibre des classes :
     - `undersampling` des transactions majoritaires
     - `oversampling` des transactions minoritaires (SMOTE)
   - Vérification de la qualité des données (valeurs manquantes, outliers)

2. **Entraînement du modèle**
   - **Régression logistique** pour la classification binaire (fraude / non-fraude)

3. **Évaluation**
   - Matrice de confusion
   - F1-score, précision, rappel
   

## Ce que j’ai appris
- Gestion d’un **jeu de données fortement déséquilibré**
- Techniques de **prétraitement** avancées
- Mise en œuvre d’un **modèle supervisé** pour la classification
- Importance de l’**évaluation adaptée** pour les problèmes déséquilibrés
- Utilisation de **Git LFS** pour gérer de gros fichiers de données

## Extensions possibles
- Tester d’autres modèles : arbres de décision, Random Forest, Gradient Boosting
- Implémenter un pipeline complet avec `scikit-learn`
- Comparer différentes techniques de gestion du déséquilibre (SMOTE, ADASYN, etc.)
- Ajouter une **interface interactive** pour prédire la fraude sur de nouvelles transactions
- Déployer le modèle en tant que **API REST** pour tests en temps réel

## Structure du projet

```Bash
CreditCardFraudDetection/
├─ data/ 
|└─ creditcard.csv
├─ notebooks/ 
|└─ credi_card_fraud_detection.ipynb
├─ .gitattributes
├─ README.md
└─ requirements.txt 
```
