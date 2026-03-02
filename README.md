# 📊 ANOVA à mesures répétées — Projet de TP (ENSAE)

## 📌 Présentation générale

Ce dépôt GitHub regroupe l’ensemble du **travail réalisé dans le cadre du TP sanctionnant la fin du cours d’Analyse de la Variance (ANOVA)** à l’École nationale de la Statistique et de l’Analyse économique.
Le projet porte sur l’**analyse de données issues d’une expérimentation agronomique**, en mobilisant une **ANOVA à mesures répétées à trois facteurs** et, en complément, des **modèles linéaires mixtes**.

L’objectif est double :

* appliquer rigoureusement les notions théoriques vues en cours ;
* proposer une analyse statistique complète, reproductible et interprétable sur des données réelles.

Le dépôt contient :

* 📄 le **rapport scientifique rédigé en LaTeX** ;
* 🧪 les **scripts R complets et commentés** ;
* 📊 les **données sources (Excel)** ;
* 📈 les **figures et sorties graphiques** produites.

---

## 🎯 Objectifs de l’étude

Cette étude vise à analyser l’effet de plusieurs facteurs sur la **hauteur des plants** :

* 🌱 **Type de terreau** (Ma, Ca, An)
* 🌾 **Variété de plant** (Var1, Var2)
* ⏱️ **répétitions** (Rep1, Rep2, Rep3, Rep4)

Les objectifs statistiques sont :

* tester l’effet propre de chaque facteur ;
* analyser les **interactions** (terreau × variété, facteurs × temps) ;
* tenir compte de la **corrélation intra-sujet** induite par les mesures répétées ;
* comparer l’ANOVA à mesures répétées avec une approche plus flexible par **modèles linéaires mixtes**.

---

## 🧠 Importance pédagogique du cours d’ANOVA

Le cours d’ANOVA occupe une place centrale dans la formation de l’ingénieur statisticien. Il permet de passer :

> 🔹 d’une simple **analyse descriptive**
> ➜ à une **analyse explicative et inférentielle** rigoureuse.

À travers ce projet, l’étudiant apprend à :

* structurer une base de données expérimentale ;
* formuler des **hypothèses statistiques** et biologiques ;
* vérifier les **conditions d’application** des modèles ;
* interpréter correctement des **p-values, tailles d’effet et interactions** ;
* produire un travail **scientifique reproductible** (scripts + rapport).

---

## 🗂️ Structure du dépôt

```text
📁 data/
   └── dataset_initial.xlsx
   └── dataset.xlsx
   └── 1.BASE TP ANOVA ISE2 2025-2026.xlsx

📁 scripts/
   ├── analyse_anova_mesures_repetees_vf.Rmd

📁 figures/
   └── boxplots_interactions.png

📁 report/
   ├── main.tex
   └── page_de_garde.tex
```

---

## 🛠️ Logiciels et outils utilisés

* **R (≥ 4.2)**
  Packages principaux : `tidyverse`, `janitor`, `readxl`, `ggplot2`, `rstatix`, `lme4`, `lmerTest`, `emmeans`, `FactoMineR`, `factoextra`
* **Microsoft Excel** (préparation et inspection initiale des données)
* **LaTeX** (rédaction du rapport scientifique)
* **R Markdown** (reproductibilité de l’analyse)

---

## 🔬 Méthodologie (résumé)

1. **Structuration de la base de données**

   * Transformationde la base initiale au format large puis passage du format large → format long
   *  Renommage des noms des variables (terreau, variete, repetition) à l'aide du package janitor

2. **Analyse descriptive**

   * Statistiques univariées
   * Comparaisons bivariées : Visualisations (boxplots, profils de croissance)
   *Analyse exploratoire multivariée : ACP (analyse en composantes principales)

3. **Analyse inférentielle**

   * Vérification des hypothèses (normalité, homogénéité, sphéricité)
   * Corrections si nécessaire (Greenhouse–Geisser, Huynh–Feldt)
   * ANOVA à mesures répétées
   * Approche complémentaire : Modèles linéaires mixtes (effets aléatoires sujets)

---

## 📚 Références méthodologiques clés

* *Agronomy* (2025). Repeated measures design in agronomy experiments.
* DataNoVIA. (2024). *ANOVA mixte dans R : hypothèses et mise en œuvre*.
* Heliyon (2024). Application des modèles à mesures répétées dans l’analyse de données expérimentales.
* NumiQO. (2023). *ANOVA avec mesures répétées : tutoriel méthodologique*.
* Park, E., Cho, M., & Ki, C.-S. (2009). Correct use of repeated measures analysis of variance. *Korean Journal of Laboratory Medicine, 29*(1), 1–9.

---

## Auteurs

* [Awa Diaw](https://github.com/awa-d) et [Mamady I Bérété](https://github.com/kefimba)**
  Étudiants en 2e année – Filière ISE
  École nationale de la Statistique et de l’Analyse économique

Encadrement pédagogique :
* **M. Carlos Akakpovi** — Chargé du cours d’Analyse de la Variance (ANOVA)
