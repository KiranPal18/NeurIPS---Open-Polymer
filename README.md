## Polymer Property Prediction using Molecular Feature Engineering and Machine Learning

This repository contains machine learning pipelines for predicting polymer properties from molecular structure data.  
It was developed for the **NeurIPS 2025 Open Polymer Prediction Challenge**, focusing on building interpretable and high-performance models using molecular descriptors, graph features, and ensemble learning techniques.

---

## Project Overview

Polymer property prediction requires converting molecular data into numerical representations that capture both chemical structure and physical behavior.  
Traditional identifiers such as SMILES strings lack structural context, limiting predictive accuracy.  
This project addresses that by integrating **feature engineering**, **graph modeling**, and **ensemble regression** to predict polymer properties such as Tg, Tc, FFV, Rg, and density.

The repository includes two main implementations:

1. **`polymer-17.ipynb`**  
   - Complete feature-engineered ensemble pipeline for polymer property prediction.  
   - Combines RDKit descriptors, Morgan fingerprints, and graph features.  
   - Uses XGBoost, LightGBM, and CatBoost models with Optuna optimization.  

2. **`polymer_model_ensemble.py`**  
   - Ensemble model combining **XGBoost** and **LightGBM** regressors optimized via **Optuna**.  
   - Uses Mordred and RDKit features with automated preprocessing.  
   - Integrates descriptor filtering, graph topology computation, and feature scaling.  

---

## Dataset

The dataset used in this project is provided by the **AI-OF-GOD-4 Kaggle competition**.  
You can access it directly here:  
🔗 [NeurIPS - Open Polymer Prediction 2025](https://www.kaggle.com/competitions/neurips-open-polymer-prediction-2025/data))

---

## Core Components

### 1. Molecular Feature Engineering
- Extracted **physicochemical and structural descriptors** using RDKit.  
- Computed **Mordred descriptors** for advanced molecular representation.  
- Generated **Morgan fingerprints** for substructure encoding.  
- Derived **graph-based topology features** (diameter, path length, cycle count) via NetworkX.  

### 2. Ensemble Modeling
- Implemented **XGBoost**, **LightGBM**, and **CatBoost** models for regression.  
- Applied **Optuna** for hyperparameter optimization to minimize MAE.  
- Combined predictions through weighted ensembling to improve robustness.  
- Used **K-Fold Cross-Validation** for model validation.

### 3. Reproducibility and Modularity
- Structured scripts for reproducible pipelines.  
- Includes `requirements.txt` for consistent dependency setup.  
- Compatible with both **Kaggle** and **local Jupyter environments**.  

---

## Technology Stack

- **Language:** Python  
- **Libraries:** RDKit, Mordred, scikit-learn, XGBoost, LightGBM, CatBoost, Optuna, Pandas, NumPy, Matplotlib, Seaborn  
- **Platform:** Kaggle Notebook  

---

## Results

-`polymer-17.ipynb` (Feature-engineered ensemble model with full molecular descriptors) **0.84**      
-`polymer_model_ensemble.py` (XGBoost–LightGBM ensemble with Optuna tuning) **0.74**

---

## Learnings

- Advanced feature engineering significantly improves model accuracy.  
- Model ensembling enhances prediction stability across multiple polymer properties.  
- Feature importance analysis aids interpretability in chemistry–ML workflows.  
- Modular pipelines make reproduction and future extension straightforward.

---

## Outcome

The project demonstrates that integrating **domain-specific chemistry features** with **ensemble machine learning** leads to more accurate polymer property predictions.  
It serves as a baseline framework for future polymer informatics and molecular property prediction challenges.

---
