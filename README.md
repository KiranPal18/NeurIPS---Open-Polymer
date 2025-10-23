## Polymer Property Prediction using Molecular Feature Engineering and Machine Learning

This repository presents a solution for predicting polymer properties using a combination of **molecular feature engineering** and **machine learning**.  
The work was developed for the **NeurIPS 2025 Open Polymer Prediction Challenge**, aiming to improve predictive accuracy through chemical feature extraction and ensemble modeling.

---

## Project Overview

Polymer property prediction requires transforming raw molecular data into meaningful numerical representations.  
Traditional models often fail because raw identifiers, such as SMILES, do not reflect molecular structure or chemical behavior.  
This project introduces a structured workflow that converts molecular representations into feature-rich vectors and applies advanced machine learning algorithms for regression-based property prediction.

All implementation details are provided in the notebook `polymer-17.ipynb`, which includes preprocessing, feature computation, model training, and evaluation.

---

## Core Components

### 1. Feature Engineering
- Extracted molecular descriptors and physicochemical features using **RDKit**.  
- Generated **Morgan fingerprints** to represent substructural similarities.  
- Modeled molecular graphs with **NetworkX** to capture topological relationships.  
- Merged descriptor, fingerprint, and graph features into a comprehensive feature set.

### 2. Model Development
- Evaluated multiple ensemble algorithms: **XGBoost**, **LightGBM**, **CatBoost**, **Random Forest**, and **Extra Trees**.  
- Applied **Optuna** for hyperparameter optimization targeting **Mean Absolute Error (MAE)**.  
- Used **K-Fold Cross-Validation** for model validation and reliability testing.  
- Final predictions were generated from the best-performing configuration.

### 3. Reproducibility and Structure
- Modular design separating data preparation, feature generation, and model training.  
- Includes `requirements.txt` for reproducible setup in both local and Kaggle environments.

---

## Technology Stack

- **Language:** Python  
- **Libraries:** RDKit, scikit-learn, XGBoost, LightGBM, CatBoost, Optuna, NetworkX, Pandas, NumPy, Matplotlib, Seaborn  
- **Platform:** Kaggle / Jupyter Notebook  

---

## Learnings

- Understood the impact of feature representation on model accuracy.  
- Learned systematic model selection and hyperparameter optimization.  
- Built modular and reproducible ML pipelines for scientific datasets.  
- Improved skills in interpreting and visualizing chemical–ML relationships.

## Outcome

The project demonstrates that domain-aware feature engineering significantly improves predictive accuracy in polymer informatics.  
The resulting pipeline serves as a reliable baseline for further research in molecular and materials property prediction.

---
