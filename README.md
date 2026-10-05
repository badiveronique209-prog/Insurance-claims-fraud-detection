# Insurance Claims Analysis & Fraud Detection

Ce projet analyse des déclarations de sinistres automobiles pour comprendre
quelles caractéristiques distinguent les déclarations frauduleuses des déclarations normales.
Je construis et compare trois modèles de Machine Learning pour prédire le risque de fraude.

## Ce que j'ai fait
Je suis partie d'un dataset brut de déclarations de sinistres avec des variables
sur le client, le véhicule, la police d'assurance et les circonstances de l'incident.
J'ai nettoyé les données, analysé les profils associés à la fraude,
puis modélisé la variable cible avec trois approches différentes.

Le pipeline de prétraitement garantit qu'aucune information du jeu de test
ne contamine l'entraînement : imputation, standardisation et encodage
sont appris sur le train uniquement.

## Résultats

Les résultats complets apparaissent dans le notebook après exécution sur le dataset réel.
Certaines variables liées aux montants déclarés, au type d'incident
et aux caractéristiques de la police présentent des distributions
notablement différentes entre fraudes et non-fraudes.

Le Recall est la métrique prioritaire dans ce contexte :
une fraude non détectée représente un coût direct pour la compagnie,
plus important qu'une fausse alerte sur une déclaration normale.

## Étapes du notebook

Chargement et exploration,structure du dataset, valeurs manquantes,
types de variables, premières observations.

Nettoyage ,traitement des valeurs spéciales, suppression des colonnes
identifiantes, vérification des doublons.

Analyse de la variable cible ,distribution fraude vs non-fraude,
déséquilibre des classes, conversion en 0/1.

Analyse exploratoire ,distributions numériques, variables catégorielles,
taux de fraude par catégorie, matrice de corrélation.

Préparation ,séparation train/test stratifiée avant tout prétraitement,
pipeline sklearn avec imputation, standardisation et One-Hot Encoding.

Modélisation ,Logistic Regression (modèle de référence), Random Forest
et Gradient Boosting, tous dans un pipeline complet.

Évaluation ,Accuracy, Precision, Recall, F1-score, ROC-AUC,
courbes ROC, matrice de confusion, importance des variables.

Interprétation métier,recommandations pour la compagnie d'assurance,
limites du modèle, conclusion.

## Stack

Python, pandas, scikit-learn, matplotlib, seaborn

## Dataset

Le fichier source est un dataset public de déclarations de sinistres automobiles
disponible sur Kaggle :
https://www.kaggle.com/datasets/buntyshah/auto-insurance-claims-data

