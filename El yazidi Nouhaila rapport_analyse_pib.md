# Rapport d'Analyse Approfondie du PIB
## Comparaison Internationale et Évolution Temporelle

---

## 1. INTRODUCTION ET CONTEXTE

### 1.1 Objectif de l'analyse

L'objectif principal de cette analyse est d'examiner et de comparer les performances économiques de plusieurs pays à travers l'étude de leur Produit Intérieur Brut (PIB). Cette étude vise à :

- Identifier les tendances de croissance économique sur une période significative
- Comparer les niveaux de développement économique entre différentes régions du monde
- Analyser les dynamiques de croissance et leur évolution temporelle
- Fournir des insights sur les disparités économiques internationales

### 1.2 Méthodologie générale employée

Notre approche méthodologique s'articule autour de plusieurs axes :

1. **Collecte de données** : Extraction de données officielles provenant d'institutions internationales reconnues
2. **Analyse statistique descriptive** : Calcul d'indicateurs de tendance centrale et de dispersion
3. **Analyse comparative** : Comparaison transversale entre pays et longitudinale dans le temps
4. **Visualisation de données** : Création de graphiques professionnels pour faciliter l'interprétation
5. **Interprétation économique** : Contextualisation des résultats dans le cadre économique global

### 1.3 Pays sélectionnés et période d'analyse

**Pays sélectionnés** :
- **États-Unis** : Première économie mondiale, représentant les économies avancées occidentales
- **Chine** : Deuxième économie mondiale, exemple d'économie émergente à forte croissance
- **Allemagne** : Première économie européenne, représentant l'Union Européenne
- **Japon** : Troisième économie mondiale, économie développée asiatique
- **Inde** : Grande économie émergente à fort potentiel démographique
- **Brésil** : Principale économie d'Amérique latine
- **France** : Grande économie européenne développée
- **Maroc** : Économie émergente d'Afrique du Nord

**Période d'analyse** : 2000-2023 (23 années)

Cette période permet d'observer :
- Les effets de la crise financière de 2008
- La reprise économique post-crise
- L'impact de la pandémie COVID-19 (2020-2021)
- Les tendances de long terme

### 1.4 Questions de recherche principales

1. Quels pays ont connu la croissance économique la plus forte sur la période analysée ?
2. Comment les différentes crises mondiales ont-elles affecté les économies étudiées ?
3. Existe-t-il une convergence ou une divergence entre économies développées et émergentes ?
4. Quel est l'impact du PIB par habitant sur le niveau de développement ?
5. Quelles sont les tendances de croissance actuelles et futures prévisibles ?

---

## 2. PRÉSENTATION DES DONNÉES

### 2.1 Source des données

**Source principale** : Banque mondiale (World Bank Open Data)
- Base de données : World Development Indicators (WDI)
- URL : https://data.worldbank.org/
- Fiabilité : Haute - données officielles collectées auprès des instituts statistiques nationaux

**Sources complémentaires** :
- Fonds Monétaire International (FMI) - World Economic Outlook
- OCDE - Statistiques économiques
- Eurostat pour les pays européens

### 2.2 Variables analysées

| Variable | Description | Unité | Utilisation |
|----------|-------------|-------|-------------|
| **PIB nominal** | Valeur totale de la production | USD courants | Comparaison taille économique |
| **PIB par habitant** | PIB divisé par population | USD par personne | Niveau de vie |
| **Taux de croissance** | Variation annuelle du PIB | Pourcentage (%) | Dynamique économique |
| **PIB réel** | PIB ajusté de l'inflation | USD constants 2015 | Comparaisons temporelles |
| **Part du PIB mondial** | Contribution au PIB mondial | Pourcentage (%) | Importance relative |

### 2.3 Période couverte

- **Début** : Année 2000
- **Fin** : Année 2023
- **Fréquence** : Données annuelles
- **Nombre d'observations** : 24 points de données par pays (192 observations totales)

### 2.4 Qualité et limitations des données

**Points forts** :
- ✓ Données officielles vérifiées par des institutions internationales
- ✓ Méthodologie standardisée permettant les comparaisons internationales
- ✓ Couverture temporelle large permettant l'analyse de tendances
- ✓ Mise à jour régulière des données

**Limitations identifiées** :
- ⚠ Économie informelle non capturée dans les statistiques officielles (particulièrement important pour les pays émergents)
- ⚠ Variations méthodologiques entre pays dans le calcul du PIB
- ⚠ Ajustements de parité de pouvoir d'achat (PPA) sujets à débat
- ⚠ Données 2023 possiblement provisoires et sujettes à révision
- ⚠ Le PIB ne mesure pas le bien-être social ou la qualité de vie

### 2.5 Tableau récapitulatif des données (2023)

| Pays | PIB (Milliards USD) | PIB par habitant (USD) | Taux de croissance (%) | Population (Millions) |
|------|---------------------|------------------------|------------------------|----------------------|
| **États-Unis** | 27 360 | 81 695 | 2.5 | 335 |
| **Chine** | 17 963 | 12 720 | 5.2 | 1 412 |
| **Allemagne** | 4 456 | 53 571 | -0.3 | 83 |
| **Japon** | 4 231 | 33 950 | 1.9 | 125 |
| **Inde** | 3 737 | 2 612 | 7.2 | 1 430 |
| **France** | 3 030 | 45 319 | 0.9 | 67 |
| **Brésil** | 2 173 | 10 126 | 2.9 | 215 |
| **Maroc** | 138 | 3 685 | 3.4 | 37 |

*Note : Données approximatives basées sur les dernières estimations disponibles*

---

## 3. CODE D'ANALYSE

### 3.1 Introduction au code

Cette section présente l'ensemble du code Python nécessaire pour réaliser l'analyse complète du PIB. Le code est organisé de manière modulaire pour faciliter la compréhension et la réutilisation. Chaque bloc remplit une fonction spécifique et est accompagné d'explications détaillées.

**Prérequis techniques** :
- Python 3.8 ou supérieur
- Bibliothèques listées ci-dessous

---

### 3.2 Importation des bibliothèques

**Explication** : Cette première étape consiste à importer toutes les bibliothèques nécessaires pour l'analyse. Chaque bibliothèque a un rôle spécifique dans le processus d'analyse des données.

```python
# Bibliothèque pour la manipulation et l'analyse de données structurées
import pandas as pd

# Bibliothèque pour les calculs numériques et les opérations mathématiques
import numpy as np

# Bibliothèque de base pour la création de visualisations
import matplotlib.pyplot as plt

# Bibliothèque avancée pour des visualisations statistiques élégantes
import seaborn as sns

# Module pour gérer les avertissements (optionnel, pour un affichage plus propre)
import warnings
warnings.filterwarnings('ignore')

# Configuration du style visuel pour des graphiques professionnels
sns.set_style("whitegrid")
plt.rcParams['figure.figsize'] = (14, 8)  # Taille par défaut des graphiques
plt.rcParams['font.size'] = 11  # Taille de police
plt.rcParams['axes.labelsize'] = 12  # Taille des labels d'axes
plt.rcParams['axes.titlesize'] = 14  # Taille des titres
plt.rcParams['xtick.labelsize'] = 10  # Taille des graduations x
plt.rcParams['ytick.labelsize'] = 10  # Taille des graduations y
plt.rcParams['legend.fontsize'] = 10  # Taille de la légende
plt.rcParams['figure.titlesize'] = 16  # Taille du titre principal

print("✓ Toutes les bibliothèques ont été importées avec succès")
```

**Résultat attendu** : Message de confirmation indiquant que toutes les bibliothèques sont disponibles.

---

### 3.3 Création de données synthétiques

**Explication** : Dans un contexte réel, les données seraient chargées depuis un fichier CSV ou une API. Pour les besoins de cette démonstration, nous créons des données synthétiques réalistes basées sur les tendances économiques réelles observées entre 2000 et 2023.

```python
# Fonction pour générer des données de PIB réalistes
def generer_donnees_pib():
    """
    Génère un DataFrame contenant des données synthétiques de PIB
    pour 8 pays sur la période 2000-2023.
    
    Returns:
        pd.DataFrame: DataFrame avec colonnes Année, Pays, PIB, PIB_par_habitant
    """
    
    # Définition de la période d'analyse
    annees = list(range(2000, 2024))  # 24 années de données
    
    # Liste des pays à analyser
    pays = ['États-Unis', 'Chine', 'Allemagne', 'Japon', 
            'Inde', 'Brésil', 'France', 'Maroc']
    
    # Dictionnaire contenant les paramètres de croissance pour chaque pays
    # PIB_initial : PIB en 2000 (milliards USD)
    # taux_croissance : taux de croissance moyen annuel
    # volatilite : écart-type de la croissance (simule les fluctuations)
    parametres_pays = {
        'États-Unis': {'PIB_initial': 10252, 'taux_croissance': 0.035, 'volatilite': 0.02},
        'Chine': {'PIB_initial': 1211, 'taux_croissance': 0.095, 'volatilite': 0.015},
        'Allemagne': {'PIB_initial': 1955, 'taux_croissance': 0.025, 'volatilite': 0.025},
        'Japon': {'PIB_initial': 4888, 'taux_croissance': 0.01, 'volatilite': 0.02},
        'Inde': {'PIB_initial': 468, 'taux_croissance': 0.07, 'volatilite': 0.02},
        'Brésil': {'PIB_initial': 655, 'taux_croissance': 0.035, 'volatilite': 0.03},
        'France': {'PIB_initial': 1366, 'taux_croissance': 0.025, 'volatilite': 0.02},
        'Maroc': {'PIB_initial': 38, 'taux_croissance': 0.045, 'volatilite': 0.025}
    }
    
    # Liste pour stocker toutes les lignes de données
    donnees = []
    
    # Seed pour la reproductibilité des résultats
    np.random.seed(42)
    
    # Génération des données pour chaque pays
    for pays_nom in pays:
        # Récupération des paramètres du pays
        params = parametres_pays[pays_nom]
        pib_actuel = params['PIB_initial']
        
        # Génération du PIB pour chaque année
        for annee in annees:
            # Simulation d'événements économiques majeurs
            # Crise financière 2008-2009
            if annee in [2008, 2009]:
                choc = np.random.uniform(-0.05, -0.02)
            # Pandémie COVID-19 en 2020
            elif annee == 2020:
                choc = np.random.uniform(-0.08, -0.03)
            # Conditions normales
            else:
                choc = np.random.normal(0, params['volatilite'])
            
            # Calcul du taux de croissance pour l'année
            taux = params['taux_croissance'] + choc
            
            # Mise à jour du PIB avec la croissance
            pib_actuel = pib_actuel * (1 + taux)
            
            # Calcul du PIB par habitant (simplification basée sur le PIB)
            # Note : Dans un cas réel, on utiliserait les données de population réelles
            if pays_nom == 'États-Unis':
                pib_par_hab = pib_actuel / 0.33  # ~330M habitants
            elif pays_nom == 'Chine':
                pib_par_hab = pib_actuel / 1.41  # ~1.4B habitants
            elif pays_nom == 'Inde':
                pib_par_hab = pib_actuel / 1.43  # ~1.4B habitants
            elif pays_nom == 'Allemagne':
                pib_par_hab = pib_actuel / 0.083  # ~83M habitants
            elif pays_nom == 'Japon':
                pib_par_hab = pib_actuel / 0.125  # ~125M habitants
            elif pays_nom == 'France':
                pib_par_hab = pib_actuel / 0.067  # ~67M habitants
            elif pays_nom == 'Brésil':
                pib_par_hab = pib_actuel / 0.215  # ~215M habitants
            else:  # Maroc
                pib_par_hab = pib_actuel / 0.037  # ~37M habitants
            
            # Ajout de la ligne de données
            donnees.append({
                'Année': annee,
                'Pays': pays_nom,
                'PIB': round(pib_actuel, 2),
                'PIB_par_habitant': round(pib_par_hab, 2)
            })
    
    # Création du DataFrame
    df = pd.DataFrame(donnees)
    
    return df

# Génération des données
df_pib = generer_donnees_pib()

# Affichage des premières lignes pour vérification
print("✓ Données générées avec succès")
print(f"\nDimensions du dataset : {df_pib.shape[0]} lignes × {df_pib.shape[1]} colonnes")
print("\nAperçu des données :")
print(df_pib.head(10))
```

**Résultat** : Un DataFrame contenant 192 observations (8 pays × 24 années) avec les variables Année, Pays, PIB et PIB par habitant.

---

### 3.4 Nettoyage et préparation des données

**Explication** : Cette étape essentielle consiste à vérifier la qualité des données, identifier et traiter les valeurs manquantes, et préparer les données pour l'analyse.

```python
# Fonction de nettoyage et préparation des données
def nettoyer_donnees(df):
    """
    Nettoie et prépare les données pour l'analyse.
    
    Args:
        df (pd.DataFrame): DataFrame brut
    
    Returns:
        pd.DataFrame: DataFrame nettoyé
    """
    
    print("=== NETTOYAGE DES DONNÉES ===\n")
    
    # 1. Vérification des valeurs manquantes
    print("1. Vérification des valeurs manquantes :")
    valeurs_manquantes = df.isnull().sum()
    print(valeurs_manquantes)
    
    if valeurs_manquantes.sum() == 0:
        print("✓ Aucune valeur manquante détectée\n")
    else:
        print(f"⚠ {valeurs_manquantes.sum()} valeurs manquantes détectées\n")
        # Traitement des valeurs manquantes (interpolation ou suppression)
        df = df.fillna(method='ffill')  # Forward fill
    
    # 2. Vérification des doublons
    print("2. Vérification des doublons :")
    doublons = df.duplicated().sum()
    print(f"Nombre de doublons : {doublons}")
    
    if doublons > 0:
        df = df.drop_duplicates()
        print(f"✓ {doublons} doublons supprimés\n")
    else:
        print("✓ Aucun doublon détecté\n")
    
    # 3. Vérification des types de données
    print("3. Types de données :")
    print(df.dtypes)
    print()
    
    # 4. Vérification des valeurs aberrantes (PIB négatif serait une erreur)
    print("4. Vérification des valeurs aberrantes :")
    pib_negatif = (df['PIB'] < 0).sum()
    print(f"PIB négatifs : {pib_negatif}")
    
    if pib_negatif > 0:
        print("⚠ Attention : valeurs négatives détectées")
        df = df[df['PIB'] >= 0]
    else:
        print("✓ Aucune valeur aberrante détectée\n")
    
    # 5. Création de variables dérivées
    print("5. Création de variables calculées :")
    
    # Calcul du taux de croissance annuel
    df = df.sort_values(['Pays', 'Année'])
    df['Taux_croissance'] = df.groupby('Pays')['PIB'].pct_change() * 100
    print("✓ Taux de croissance annuel calculé")
    
    # Calcul du PIB en milliards (pour meilleure lisibilité)
    df['PIB_milliards'] = df['PIB']
    print("✓ PIB en milliards créé")
    
    # Ajout d'une colonne période (pour analyses par décennie)
    df['Période'] = pd.cut(df['Année'], 
                           bins=[1999, 2009, 2019, 2024],
                           labels=['2000-2009', '2010-2019', '2020-2023'])
    print("✓ Variable 'Période' créée\n")
    
    print("=== NETTOYAGE TERMINÉ ===\n")
    
    return df

# Application du nettoyage
df_pib_clean = nettoyer_donnees(df_pib)

# Affichage du résumé statistique
print("Résumé statistique des données nettoyées :")
print(df_pib_clean[['PIB', 'PIB_par_habitant', 'Taux_croissance']].describe())
```

**Résultat** : Un DataFrame nettoyé avec des variables supplémentaires calculées (taux de croissance, périodes).

---

### 3.5 Calcul des statistiques descriptives

**Explication** : Cette section calcule les principales statistiques descriptives qui permettront de comprendre la distribution et les caractéristiques des données.

```python
# Fonction de calcul des statistiques descriptives
def calculer_statistiques(df):
    """
    Calcule et affiche les statistiques descriptives complètes.
    
    Args:
        df (pd.DataFrame): DataFrame nettoyé
    
    Returns:
        dict: Dictionnaire contenant les différentes statistiques
    """
    
    print("="*60)
    print("STATISTIQUES DESCRIPTIVES DÉTAILLÉES")
    print("="*60)
    print()
    
    stats = {}
    
    # 1. Statistiques globales par pays
    print("1. STATISTIQUES PAR PAYS (2000-2023)")
    print("-" * 60)
    
    stats_pays = df.groupby('Pays').agg({
        'PIB': ['mean', 'std', 'min', 'max'],
        'PIB_par_habitant': ['mean', 'std', 'min', 'max'],
        'Taux_croissance': ['mean', 'std']
    }).round(2)
    
    print(stats_pays)
    print()
    stats['stats_pays'] = stats_pays
    
    # 2. PIB moyen par période
    print("2. PIB MOYEN PAR PÉRIODE")
    print("-" * 60)
    
    pib_periode = df.groupby(['Pays', 'Période'])['PIB'].mean().unstack()
    print(pib_periode.round(2))
    print()
    stats['pib_periode'] = pib_periode
    
    # 3. Taux de croissance moyen par pays
    print("3. TAUX DE CROISSANCE MOYEN PAR PAYS (%)")
    print("-" * 60)
    
    croissance_moyenne = df.groupby('Pays')['Taux_croissance'].mean().sort_values(ascending=False)
    print(croissance_moyenne.round(2))
    print()
    stats['croissance_moyenne'] = croissance_moyenne
    
    # 4. Volatilité de la croissance (écart-type)
    print("4. VOLATILITÉ DE LA CROISSANCE (ÉCART-TYPE)")
    print("-" * 60)
    
    volatilite = df.groupby('Pays')['Taux_croissance'].std().sort_values(ascending=False)
    print(volatilite.round(2))
    print()
    stats['volatilite'] = volatilite
    
    # 5. Classement des pays par PIB en 2023
    print("5. CLASSEMENT PAR PIB EN 2023")
    print("-" * 60)
    
    classement_2023 = df[df['Année'] == 2023].sort_values('PIB', ascending=False)[['Pays', 'PIB', 'PIB_par_habitant']]
    classement_2023.index = range(1, len(classement_2023) + 1)
    print(classement_2023.round(2))
    print()
    stats['classement_2023'] = classement_2023
    
    # 6. Croissance cumulée 2000-2023
    print("6. CROISSANCE CUMULÉE 2000-2023 (%)")
    print("-" * 60)
    
    pib_2000 = df[df['Année'] == 2000].set_index('Pays')['PIB']
    pib_2023 = df[df['Année'] == 2023].set_index('Pays')['PIB']
    croissance_cumulee = ((pib_2023 / pib_2000 - 1) * 100).sort_values(ascending=False)
    print(croissance_cumulee.round(2))
    print()
    stats['croissance_cumulee'] = croissance_cumulee
    
    print("="*60)
    
    return stats

# Calcul des statistiques
statistiques = calculer_statistiques(df_pib_clean)
```

**Résultat** : Un ensemble complet de statistiques descriptives organisées par thèmes.

---

### 3.6 Fonction de création des visualisations

**Explication** : Cette section contient toutes les fonctions nécessaires pour créer les visualisations professionnelles de l'analyse.

```python
# Palette de couleurs professionnelle
couleurs_pays = {
    'États-Unis': '#1f77b4',
    'Chine': '#ff7f0e',
    'Allemagne': '#2ca02c',
    'Japon': '#d62728',
    'Inde': '#9467bd',
    'Brésil': '#8c564b',
    'France': '#e377c2',
    'Maroc': '#7f7f7f'
}

def creer_visualisations(df, stats):
    """
    Crée l'ensemble des visualisations pour le rapport.
    
    Args:
        df (pd.DataFrame): DataFrame nettoyé
        stats (dict): Dictionnaire des statistiques
    """
    
    # Configuration générale
    plt.style.use('seaborn-v0_8-darkgrid')
    
    # 1. ÉVOLUTION DU PIB AU FIL DU TEMPS
    print("Création du graphique 1 : Évolution du PIB...")
    
    fig, ax = plt.subplots(figsize=(16, 9))
    
    for pays in df['Pays'].unique():
        donnees_pays = df[df['Pays'] == pays]
        ax.plot(donnees_pays['Année'], 
                donnees_pays['PIB'] / 1000,  # Conversion en billions
                label=pays,
                color=couleurs_pays[pays],
                linewidth=2.5,
                marker='o',
                markersize=4)
    
    # Marquage des événements majeurs
    ax.axvline(x=2008, color='red', linestyle='--', alpha=0.5, linewidth=1.5)
    ax.text(2008, ax.get_ylim()[1] * 0.95, 'Crise 2008', 
            rotation=90, verticalalignment='top', fontsize=10, color='red')
    
    ax.axvline(x=2020, color='red', linestyle='--', alpha=0.5, linewidth=1.5)
    ax.text(2020, ax.get_ylim()[1] * 0.95, 'COVID-19', 
            rotation=90, verticalalignment='top', fontsize=10, color='red')
    
    ax.set_xlabel('Année', fontsize=14, fontweight='bold')
    ax.set_ylabel('PIB (Billions USD)', fontsize=14, fontweight='bold')
    ax.set_title('Évolution du PIB par Pays (2000-2023)', 
                 fontsize=18, fontweight='bold', pad=20)
    ax.legend(loc='upper left', frameon=True, shadow=True, fontsize=11)
    ax.grid(True, alpha=0.3)
    
    plt.tight_layout()
    plt.savefig('evolution_pib.png', dpi=300, bbox_inches='tight')
    plt.show()
    print("✓ Graphique 1 créé\n")
    
    
    # 2. COMPARAISON DU PIB EN 2023
    print("Création du graphique 2 : Comparaison PIB 2023...")
    
    fig, ax = plt.subplots(figsize=(14, 8))
    
    donnees_2023 = df[df['Année'] == 2023].sort_values('PIB', ascending=True)
    couleurs = [couleurs_pays[p] for p in donnees_2023['Pays']]
    
    bars = ax.barh(donnees_2023['Pays'], 
                    donnees_2023['PIB'] / 1000,
                    color=couleurs,
                    edgecolor='black',
                    linewidth=1.2)
    
    # Ajout des valeurs sur les barres
    for i, bar in enumerate(bars):
        width = bar.get_width()
        ax.text(width, bar.get_y() + bar.get_height()/2,
                f'{width:.1f}T',
                ha='left', va='center', fontweight='bold', fontsize=10)
    
    ax.set_xlabel('PIB (Billions USD)', fontsize=14, fontweight='bold')
    ax.set_ylabel('Pays', fontsize=14, fontweight='bold')
    ax.set_title('Comparaison du PIB entre Pays (2023)', 
                 fontsize=18, fontweight='bold', pad=20)
    ax.grid(axis='x', alpha=0.3)
    
    plt.tight_layout()
    plt.savefig('comparaison_pib_2023.png', dpi=300, bbox_inches='tight')
    plt.show()
    print("✓ Graphique 2 créé\n")
    
    
    # 3. PIB PAR HABITANT EN 2023
    print("Création du graphique 3 : PIB par habitant...")
    
    fig, ax = plt.subplots(figsize=(14, 8))
    
    donnees_2023_hab = df[df['Année'] == 2023].sort_values('PIB_par_habitant', ascending=True)
    couleurs_hab = [couleurs_pays[p] for p in donnees_2023_hab['Pays']]
    
    bars = ax.barh(donnees_2023_hab['Pays'], 
                    donnees_2023_hab['PIB_par_habitant'] / 1000,
                    color=couleurs_hab,
                    edgecolor='black',
                    linewidth=1.2)
    
    # Ajout des valeurs
    for i, bar in enumerate(bars):
        width = bar.get_width()
        ax.text(width, bar.get_y() + bar.get_height()/2,
                f'${width:.1f}K',
                ha='left', va='center', fontweight='bold', fontsize=10)
    
    ax.set_xlabel('PIB par Habitant (Milliers USD)', fontsize=14, fontweight='bold')
    ax.set_ylabel('Pays', fontsize=14, fontweight='bold')
    ax.set_title('PIB par Habitant par Pays (2023)', 
                 fontsize=18, fontweight='bold', pad=20)
    ax.grid(axis='x', alpha=0.3)
    
    plt.tight_layout()
    plt.savefig('pib_par_habitant_2023.png', dpi=300, bbox_inches='tight')
    plt.show()
    print("✓ Graphique 3 créé\n")
    
    
    # 4. TAUX DE CROISSANCE MOYEN PAR PAYS
    print("Création du graphique 4 : Taux de croissance moyen...")
    