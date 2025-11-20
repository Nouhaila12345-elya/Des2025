I. Introduction : Présentation du Projet Vinho Verde

Le présent projet s’appuie sur le jeu de données issu des travaux de Cortez et al. (2009), portant sur l’analyse physicochimique et sensorielle de deux variantes du vin portugais Vinho Verde : le vin rouge et le vin blanc.
Ces données regroupent un ensemble de mesures objectives réalisées en laboratoire, couplées à une évaluation subjective effectuée par un panel d’experts, qui attribue une note de qualité comprise entre 0 et 10.

L’objectif principal consiste à développer des modèles d’apprentissage automatique capables de prédire la qualité perçue d’un vin à partir de ses caractéristiques physicochimiques.
Ce cas d’étude constitue un excellent laboratoire méthodologique pour aborder des problématiques de régression, de classification, d’analyse exploratoire et de sélection de variables, à la croisée de l’œnologie, de la chimie analytique et de la science des données.

II. Justification du Choix de la Base de Données
1. Pertinence Métier

Le dataset constitue un outil d’aide à la décision pour les producteurs et œnologues. La prédiction automatique de la qualité peut :

réduire la dépendance aux évaluations sensorielles coûteuses ;

garantir une meilleure constance dans la classification des vins ;

améliorer la maîtrise des processus de production (contrôle qualité).

2. Analyse Bivariée : Vin Rouge vs Vin Blanc

L'existence de deux fichiers indépendants permet :

d’examiner les différences structurelles entre profils chimiques ;

d’évaluer l’influence des variables sur la qualité selon le type de vin.

Cela favorise une analyse comparative riche.

3. Défis de Modélisation

La base présente plusieurs défis intéressants :

Déséquilibre de la variable cible (notes extrêmes rares) ;

Nature ordinale du score de qualité ;

Présence potentielle d’outliers ;

Grande diversité de variables → nécessité d’une sélection ou réduction dimensionnelle.

4. Intérêt Académique

Ce dataset est souvent utilisé pour :

comparer des modèles (régression vs classification) ;

tester des pipelines complets ;

produire des analyses interprétables (SHAP, importance des variables).

III. Structure des Données et Variables

Le jeu de données est multivarié, numérique et sans valeurs manquantes.
Il contient :

1599 observations pour le vin rouge,

4898 observations pour le vin blanc.

A. Variables d’Entrée (Features)

Les 11 variables explicatives sont des mesures physicochimiques continues :

Catégorie	Variables	Rôle sensoriel / chimique
Acidité	fixed_acidity, volatile_acidity, citric_acid, pH	Définissent l’équilibre gustatif. L’acidité volatile est un indicateur de défauts.
Composition	residual_sugar, alcohol	Le sucre résiduel influence la douceur ; l’alcool est un prédicteur clé de qualité.
Protection	free_sulfur_dioxide, total_sulfur_dioxide, sulphates	Conservateurs pouvant affecter l’arôme s’ils sont trop élevés.
Autres	chlorides, density	Indicateurs du sel et corrélation avec alcool/sucre.
B. Variable de Sortie (Target)
Variable	Type	Description
quality	Score ordinal (0–10)	Note attribuée par des experts en dégustation.
IV. Stratégie de Modélisation Recommandée
1. Analyse Exploratoire des Données (EDA)

Objectifs :

Étudier les distributions et corrélations ;

Identifier les différences entre vins rouges et blancs (acidité, pH, soufre, alcool, densité…) ;

Repérer les valeurs extrêmes.

La corrélation alcool → qualité constitue un point d’analyse classique.

2. Prétraitement

Normalisation / standardisation des variables.

Détection des outliers (méthodes robustes : IQR, isolation forest).

Traitement du déséquilibre suivant la tâche (SMOTE, pondération).

3. Modélisation
A. Régression

Objectif : prédire la note exacte.
Modèles recommandés :

Random Forest Regressor

Gradient Boosting / XGBoost / LightGBM

Ridge / Lasso

B. Classification

Objectif : regrouper les notes en classes ordonnées, par exemple :

Basse qualité : ≤ 5

Qualité moyenne : = 6

Bonne qualité : ≥ 7

Modèles utilisés :

Random Forest Classifier

SVM

XGBoost

Logistic Regression

Stratégies contre le déséquilibre :

SMOTE

Pondération

Ajustement des seuils de décision

4. Interprétabilité

Outils recommandés :

Importance des variables

SHAP values

Partial Dependence Plots

Ces méthodes permettent de comprendre quelles caractéristiques rendent un vin "bon".

Conclusion

Le jeu de données Vinho Verde constitue un excellent support pour un projet de machine learning complet. Sa richesse et ses défis méthodologiques permettent :

d’explorer les différences entre vins rouges et blancs,

de comparer plusieurs approches de modélisation,

de produire des analyses interprétables et utiles pour les professionnels du secteur.

Il offre ainsi un cadre idéal pour un compte rendu structuré, académique et orienté machine learning, tout en s’intégrant dans une logique métier réelle (qualité du vin, contrôle, optimisation).
<img width="643" height="535" alt="image" src="https://github.com/user-attachments/assets/b1294806-c058-4b84-8303-b478b6ed72bb" />
<img width="552" height="529" alt="image" src="https://github.com/user-attachments/assets/206d09a1-3ba1-46b2-9fb0-12ea3a0f6ebe" />


