Breast Cancer Diagnosis - Exploratory Data Analysis (TP1) 
Présentation du ProjetCe projet constitue la première phase (TP1) d'un cycle complet de MLOps. 
L'objectif est de réaliser une analyse exploratoire approfondie (EDA) et un prétraitement rigoureux du dataset Breast Cancer Wisconsin (Diagnostic) afin de préparer le terrain pour la modélisation prédictive.L'enjeu est de comprendre quelles caractéristiques morphologiques des noyaux cellulaires (extraites d'images de ponction à l'aiguille fine) sont les plus discriminantes pour identifier une tumeur Maligne (M) ou Bénigne (B).
 Le DatasetSource : UCI Machine Learning Repository.
 Taille : 569 échantillons, 32 variables.Variable Cible : Diagnosis (M = Malignant, B = Benign).Caractéristiques : 10 mesures de base (radius, texture, area, etc.) déclinées en moyenne, erreur standard et pire valeur (worst).
  Étapes Réalisées
  1. Analyse Exploratoire (EDA)Audit de qualité : Vérification de l'intégrité des données (absence de valeurs manquantes).
  Analyse de distribution : Étude du déséquilibre des classes (37% M / 63% B).Visualisation statistique : Utilisation de Seaborn et Matplotlib pour tracer des histogrammes de densité et des matrices de corrélation.
  Séparabilité : Identification des variables clés (ex: points concaves, périmètre) montrant une séparation nette entre les classes.
  2. Preprocessing & Data EngineeringNettoyage : Suppression des colonnes non informatives (id).Encodage : Transformation de la cible catégorielle en valeurs numériques ($M=1, B=0$).Feature Scaling : Préparation à la standardisation pour harmoniser les ordres de grandeur entre les variables (ex: area vs smoothness).

     Résultats Clés
Multicolinéarité : Détection de fortes corrélations entre le rayon, le périmètre et l'aire, suggérant une possible réduction de dimension future.

Variables discriminantes : Les caractéristiques de type "Worst" semblent plus prédictives que les "Mean".

Prêt pour le TP2 : Le dataset nettoyé est exporté et prêt pour l'entraînement des algorithmes de classification.

 Installation et Utilisation
Cloner le dépôt :

Bash

git clone https://github.com/votre-username/breast-cancer-mlops.git
Installer les dépendances :

Bash

pip install pandas matplotlib seaborn scikit-learn
Exécuter le notebook :

Bash

jupyter notebook TP1.ipynb
