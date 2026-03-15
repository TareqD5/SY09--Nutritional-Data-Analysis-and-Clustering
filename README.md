# Nutritional Data Analysis & Clustering — SY09 Project

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-yellowgreen?logo=scikit-learn)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

> Unsupervised machine learning project applying dimensionality reduction (PCA, MDS) and hierarchical clustering (HAC) to a nutritional dataset, as part of the **SY09 – Data Science** course at UTC.

---

## Table of Contents

- [Overview](#overview)
- [Methodology](#methodology)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Key Results](#key-results)
- [Authors](#authors)

---

## Overview

This project was carried out as part of the **SY09 (Data Science)** course unit at the **Université de Technologie de Compiègne (UTC)**. The goal is to explore, visualize, and segment a nutritional dataset in order to identify coherent food groups and analyze their structural similarities.

The study is based on `cleaned_nutrition_dataset.csv`, a dataset containing a wide range of nutritional features for hundreds of food items. Through a rigorous data science pipeline, we apply unsupervised learning techniques to extract meaningful knowledge from this high-dimensional data.

---

## Methodology

The analysis follows a structured four-step pipeline:

1. **Data Cleaning & Preprocessing**  
   Standardization and normalization of all nutritional variables to ensure comparability across features with different scales.

2. **Dimensionality Reduction**  
   - **PCA (Principal Component Analysis):** Projects the data onto a lower-dimensional space while maximizing variance retention, enabling 2D/3D visualization.  
   - **MDS / AFTD (Multidimensional Scaling):** Preserves pairwise distances between food items in the projected space.

3. **Clustering (Segmentation)**  
   - **HAC (Hierarchical Agglomerative Clustering):** Groups food items bottom-up using linkage criteria. Dendrogram analysis is used to determine the optimal number of clusters.

4. **Advanced Visualization**  
   - **Shepard Diagrams:** Assess the quality of MDS projections by comparing original distances to projected distances.  
   - **Factorial Planes & Dendrograms:** Provide interpretable visual summaries of the clustering structure.

---

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3 |
| Data Analysis | Pandas, NumPy |
| Machine Learning | Scikit-learn (PCA, MDS, AgglomerativeClustering) |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |

---

## Project Structure
```
SY09--Nutritional-Data-Analysis-and-Clustering/
│
├── SY09_Jupyter.ipynb              # Main notebook: full analysis, code & visualizations
├── SY09_Projet_Rapport_Final.pdf   # Detailed report: methodology & result interpretation
├── cleaned_nutrition_dataset.csv   # Input dataset
└── utils.py                        # Utility functions (plot_dendrogram, plot_Shepard, etc.)
```

---

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/TareqD5/SY09--Nutritional-Data-Analysis-and-Clustering.git
cd SY09--Nutritional-Data-Analysis-and-Clustering
```

### 2. Install dependencies

It is recommended to use a virtual environment:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Launch the notebook
```bash
jupyter notebook SY09_Jupyter.ipynb
```

---

## Key Results

- **Nutrient correlations:** Strong relationships identified between fat content and caloric density, as well as between protein and mineral content.
- **PCA:** The first two principal components retain over **70% of total inertia**, confirming the adequacy of 2D projection for this dataset.
- **HAC Clustering:** The dendrogram analysis revealed **7 distinct food clusters**, including:
  - Dairy products
  - Meat & fish
  - Cereal & grain products
  - Fruits & vegetables
  - Processed/high-fat foods

---

## Authors

| Name | Institution |
|---|---|
| Tareq Derdaki | UTC — Université de Technologie de Compiègne |
| Ruoyang Wang | UTC — Université de Technologie de Compiègne |
| Tidiane Bengriche | UTC — Université de Technologie de Compiègne |

**Course:** SY09 – Data Science  
**Institution:** [Université de Technologie de Compiègne (UTC)](https://www.utc.fr)
