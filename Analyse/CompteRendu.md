🧾 1. Présentation Générale

Le Employee Salary Dataset est un ensemble de données RH contenant les informations démographiques, professionnelles et salariales de 50 employés.
Il est conçu pour des analyses de :

prédiction de salaires,

étude des tendances RH,

segmentation du personnel,

EDA (analyse exploratoire des données).

Licence : CC0 (Domaine public)
Mise à jour : Jamais
Taille : 50 lignes, 9 colonnes

🗂️ 2. Structure du Dataset
Variable	Description
EmployeeID	Identifiant unique
Name	Nom de l’employé
Department	Département (IT, Marketing, Finance...)
Experience_Years	Années d’expérience
Education_Level	Niveau d’éducation
Age	Âge
Gender	Sexe
City	Localisation
Monthly_Salary	Salaire mensuel
📊 3. Analyse Descriptive des Variables
3.1. Département

Marketing : 26%

Operations : 20%

Autres (IT, HR, Finance) : 54%

→ Bonne variété de départements.

3.2. Niveau d’Éducation

Master : 38%

High School : 24%

Autres (Bachelor, PhD...) : 38%

→ Forte présence d’employés diplômés de Master.

3.3. Genre

Femmes : 54%

Hommes : 46%

→ Dataset légèrement dominé par les femmes.

3.4. Ville

Delhi : 30%

Hyderabad : 24%

Autres villes : 46%

→ Les employés sont répartis sur plusieurs hubs technologiques de l’Inde.

3.5. Expérience

Entre 1 et 50 ans, répartis par tranches de façon très régulière.
→ Indice que le dataset est synthétique.

3.6. Âge

Entre 22 et 57 ans, distribution uniforme.

3.7. Salaire mensuel

Min : 28 420

Max : 149 123

Concentration entre 64 000 et 76 000

→ Quelques salaires très élevés constituent des outliers intéressants.

🔍 4. Relations et Insights Potentiels
4.1. Salaire vs Expérience

Relation généralement positive : plus d'expérience → salaire plus élevé.
Quelques anomalies indiquent un dataset artificiel.

4.2. Salaire vs Département

Marketing et Finance montrent souvent des salaires élevés.

HR et Operations présentent plus de variabilité.

4.3. Salaire vs Niveau d’Éducation

Tendance attendue :
PhD / Master → salaires plus élevés
High School → salaires plus faibles (avec exceptions)

4.4. Salaire vs Ville

Delhi, Mumbai et Bangalore affichent les salaires les plus élevés.

🧪 5. Qualité du Dataset
✔️ Points forts

Aucune valeur manquante

Variables significatives

Parfait pour un projet Machine Learning ou EDA

Facile à visualiser et interpréter

❗ Limites

Seulement 50 lignes → modèles ML limités

Distributions trop parfaites → dataset probablement synthétique

Risque de surapprentissage

Certaines colonnes peu utiles (Name)

🚀 6. Applications possibles
Analyses exploratoires (EDA)

Heatmap de corrélation

Boxplots département vs salaire

Analyse hommes/femmes

Graphiques expérience vs salaire

Étude des outliers

Machine Learning

Objectif : Prédire Monthly_Salary

Modèles recommandés :

Régression Linéaire

Random Forest

XGBoost

Variables importantes :
Experience_Years, Department, Education_Level, City, Age
