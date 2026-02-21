# 🏪 Superstore Sales Analysis — Analyse Bivariée des Performances Commerciales

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-teal)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Contexte du Projet

Ce projet constitue une **analyse exploratoire bivariée** (EDA) du célèbre **Superstore Dataset**, réalisée dans le cadre du Projet 3. L'objectif est d'identifier professionnellement les facteurs influençant les performances commerciales afin de formuler des **recommandations stratégiques concrètes et chiffrées**.

---

## 🎯 Objectifs

- Identifier les **drivers de profitabilité** à travers des analyses bivariées rigoureuses
- Quantifier l'impact de variables clés : `Discount`, `Region`, `Category`, `Sub-Category`, `Ship Mode`, `Segment`
- Détecter les **sous-catégories déficitaires** et les combinaisons Région × Catégorie problématiques
- Produire des **insights business actionnables** avec simulation ROI

---

## 📁 Structure du Projet

```
superstore-analysis/
│
├── superstore_analysis.ipynb     # Notebook principal (analyses + visualisations)
├── Sample-Superstore.csv       # Dataset source
└── README.md                     # Documentation du projet
```

---

## 🔬 Plan d'Analyse

Le notebook est structuré en 9 sections progressives :

| # | Section | Contenu |
|---|---------|---------|
| 0 | **Setup** | Imports, configuration style, palettes |
| 1 | **Chargement & Aperçu** | Types, valeurs manquantes, stats descriptives |
| 2 | **Feature Engineering** | `Profit Margin`, `Is_Loss`, `Delivery Days` |
| 3 | **Bivariée Quanti–Quanti** | Corrélations Pearson/Spearman, scatter plots |
| 4 | **Bivariée Quanti–Quali** | Boxplots, ANOVA, T-test, impact du Discount |
| 5 | **Tableaux Croisés Quali–Quali** | Heatmaps Category × Region, Top/Flop Sub-Categories |
| 6 | **Ship Mode & Segment** | Profitabilité par mode de livraison et segment client |
| 7 | **Détection Facteurs Clés** | Corrélations avec Profit, tableau de synthèse |
| 8 | **Simulation ROI** | +10% Quantity dans les top régions |
| 9 | **Insights & Recommandations** | Conclusions stratégiques chiffrées |

---

## 📊 Principaux Résultats

### 🌍 Performance par Région
| Région | Profit Total | Marge Globale |
|--------|-------------|---------------|
| West   | $108 418    | 14.9% ✅      |
| East   | $91 523     | 13.5% ✅      |
| South  | $46 749     | 11.9% ⚠️      |
| Central| $39 706     | 7.9%  🔴      |

### 📦 Performance par Catégorie
| Catégorie       | Profit Total | Marge Globale |
|----------------|-------------|---------------|
| Technology      | $145 455    | 17.4% ✅      |
| Office Supplies | $122 491    | 17.0% ✅      |
| Furniture       | $18 451     | 2.5%  🔴      |

### 📚 Sous-catégories déficitaires
| Sub-Category | Ventes    | Profit     | Marge   |
|-------------|-----------|------------|---------|
| Tables      | $206 966  | -$17 725   | -8.6%   |
| Bookcases   | $114 880  | -$3 473    | -3.0%   |
| Supplies    | $46 674   | -$1 189    | -2.6%   |

---

## 💡 Recommandations Stratégiques

1. **Plafonner les discounts à 20% max** - au-delà, chaque vente devient une perte sèche (-114% de marge à >50%)
2. **Simuler +10% Quantity sur West/East** - gain estimé +$19 994, soit **+7% du profit global**
3. **Concentrer le budget marketing sur West & East** - écart de +7 points de marge sur Central
4. **Revoir le pricing de Tables et Bookcases** - 207k$ de ventes pour -17k$ de profit
5. **Développer Technology & Office Supplies** (~17% de marge) au détriment de Furniture (2.5%)
6. **Cibler Home Office et Corporate** - profit moyen respectivement 33.8$ et 30.5$ vs 25.8$ pour Consumer
7. **Privilégier First Class** pour les commandes haute valeur (profit moyen +$4.3 vs Standard Class)

---

## 🛠️ Technologies Utilisées

- **Python 3.10+**
- **Pandas** - manipulation et agrégation des données
- **Seaborn / Matplotlib** - visualisations avancées
- **SciPy** - tests statistiques (ANOVA, T-test)
- **Jupyter Notebook** - environnement d'analyse

---

## ▶️ Installation & Exécution

```bash
# 1. Cloner le repository
git clone https://github.com/votre-username/superstore-analysis.git
cd superstore-analysis

# 2. Installer les dépendances
pip install pandas numpy matplotlib seaborn scipy jupyter

# 3. Lancer le notebook
jupyter notebook superstore_analysis.ipynb
```

> ⚠️ Assurez-vous que `Sample-Superstore.csv` se trouve dans le même dossier que le notebook.

---

## 📄 Dataset

Le **Superstore Dataset** est un dataset public de ventes au détail aux États-Unis, largement utilisé pour des exercices d'analyse de données. Il contient **9 994 transactions** sur 4 régions, 3 catégories de produits et plusieurs années.

---

## 👤 Pascal Adechinan

Projet réalisé dans le cadre d'un cours de **Data Analysis avec Python**.
