# Compte Rendu – Employee Salary Dataset

## 1. Présentation Générale
Le Employee Salary Dataset contient les informations démographiques, professionnelles et salariales de 50 employés. Il est conçu pour des analyses telles que la prédiction des salaires, les études des tendances RH, la segmentation du personnel, et l’analyse exploratoire des données (EDA). Ce dataset est sous licence CC0 (domaine public), n'a jamais été mis à jour, et comprend 50 lignes et 9 colonnes.

## 2. Structure du Dataset
| Variable          | Description                            |
|-------------------|------------------------------------|
| EmployeeID        | Identifiant unique                  |
| Name              | Nom de l’employé                   |
| Department        | Département (IT, Marketing, Finance...) |
| Experience_Years  | Années d’expérience                |
| Education_Level   | Niveau d’éducation                 |
| Age               | Âge                               |
| Gender            | Sexe                              |
| City              | Localisation                      |
| Monthly_Salary    | Salaire mensuel                   |

## 3. Analyse Descriptive des Variables
- **Département** : Marketing (26%), Operations (20%), Autres (IT, HR, Finance) (54%) – bonne variété de départements.
- **Niveau d’Éducation** : Master (38%), High School (24%), Autres (Bachelor, PhD...) (38%) – forte présence d'employés diplômés de Master.
- **Genre** : Femmes (54%), Hommes (46%) – dataset légèrement dominé par les femmes.
- **Ville** : Delhi (30%), Hyderabad (24%), Autres villes (46%) – répartition sur plusieurs hubs technologiques en Inde.
- **Expérience** : Entre 1 et 50 ans, répartis de manière très régulière, suggérant un dataset synthétique.
- **Âge** : Uniforme entre 22 et 57 ans.
- **Salaire mensuel** : Min 28 420, Max 149 123, concentration entre 64 000 et 76 000 avec quelques outliers très élevés.

## 4. Relations et Insights Potentiels
- Salaire et expérience montrent une relation positive : plus d'expérience, salaire plus élevé, avec quelques anomalies.
- Marketing et Finance tendent à avoir des salaires élevés, alors que HR et Operations présentent plus de variabilité.
- Niveau d’Éducation et salaire montrent la tendance attendue : PhD/Master avec salaires plus élevés, High School avec salaires plus bas, exceptions possibles.
- Les villes comme Delhi, Mumbai et Bangalore affichent les salaires les plus élevés.

## 5. Qualité du Dataset
- **Points forts** : aucune valeur manquante, variables significatives, parfait pour projets ML ou EDA, facile à visualiser.
- **Limites** : seulement 50 lignes, distributions très parfaites suggérant un dataset synthétique, risque de surapprentissage, certaines colonnes moins utiles (ex. Name).

## 6. Applications possibles
- Analyses exploratoires (EDA) : heatmap de corrélation, boxplots département vs salaire, analyse homme/femme, graphiques expérience vs salaire, étude des outliers.
- Machine Learning pour prédiction du salaire mensuel. Modèles recommandés : Régression Linéaire, Random Forest, XGBoost.
- Variables importantes pour ML : Experience_Years, Department, Education_Level, City, Age.
