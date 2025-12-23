# Personalized Nutrition Predictor

An end-to-end machine learning prototype that predicts an individual’s daily caloric requirement using structured health, lifestyle, and dietary data.  
This project focuses on **model experimentation, evaluation, and system integration**, rather than clinical accuracy or production deployment.

---

## Project Motivation

Generalized nutrition guidelines do not account for individual differences in age, body composition, activity level, sleep, and stress.  
This project explores how classical machine learning and neural networks can be used to **estimate personalized caloric requirements** from tabular health data and expose the workflow through a simple desktop interface.

---

## Problem Statement

**Objective:**  
Predict **Caloric Requirement (kcal/day)** as a continuous value based on user health and lifestyle features.

**Problem Type:**  
Supervised regression on structured tabular data.

---

## Dataset Overview

The dataset consists of demographic, lifestyle, body composition, and dietary intake features:

**Input Features**
- Demographics: `Age`, `Gender`, `Height (cm)`, `Weight (kg)`
- Lifestyle: `Activity Level`, `Sleep Duration (hours)`, `Stress Level`, `Daily Water Intake (liters)`
- Health & Body Composition: `BMI`, `Body Fat Percentage`, `Health Conditions`
- Dietary Intake (used cautiously):  
  `Daily Calorie Intake`, `Protein Intake`, `Carbohydrate Intake`, `Fat Intake`

**Target Variable**
- `Caloric Requirement (kcal/day)`

> ⚠️ Note: Some dietary intake features may be correlated with the target and can introduce information leakage. They are included for experimentation, not as a guaranteed production-safe feature set.

---

## Modeling Approach

This project intentionally starts simple and increases complexity step by step.

### 1. Ridge Regression (Baseline)
- Used as a baseline linear model
- Handles multicollinearity through L2 regularization
- Provides interpretability and a performance benchmark

### 2. Feedforward Neural Network (FFNN)
- Captures non-linear relationships between health and lifestyle features
- Uses standardized input features
- Trained with mean squared error loss

### 3. FFNN + Random Forest Regressor (Stacked Experiment)
- FFNN is used to learn non-linear representations
- Random Forest Regressor is trained on FFNN outputs
- Explores bias–variance trade-offs and robustness

> This stacking approach is **experimental** and intended for learning purposes rather than claiming state-of-the-art performance.

---

## Model Evaluation

Models are evaluated using standard regression metrics:
- **MAE** – Mean Absolute Error (primary metric for interpretability)
- **MSE / RMSE** – Penalizes larger prediction errors
- **R² Score** – Measures explained variance

Prediction vs actual value plots are also generated for visual inspection.

---

## Application Interface

A simple **Tkinter-based GUI** is provided to:
- Upload datasets
- Run preprocessing and exploratory analysis
- Train models
- Evaluate performance
- Run predictions on unseen test data

The GUI is intended as a **prototype interface**, not a production-ready application.

---

## What This Project Is About

- Learning and applying regression models on real-world tabular data  
- Understanding bias–variance trade-offs  
- Comparing linear models with non-linear models  
- Building an end-to-end ML workflow (data → model → evaluation → inference)  
- Integrating ML models into a usable application  

---

## What This Project Is NOT About

- ❌ Medical or clinical nutrition advice  
- ❌ Personalized diet planning or meal recommendation systems  
- ❌ Production-grade ML pipelines  
- ❌ Large-scale deployment or real-time inference  
- ❌ Claims of optimal or validated nutritional accuracy  

---

## Limitations

- Dataset size and quality may limit generalization  
- Some features may introduce information leakage  
- Feature encoding is simplified and can be improved  
- Explainability is limited for deep learning components  
- No cross-validation or automated hyperparameter tuning is applied  

These limitations are acknowledged intentionally and would be addressed in a production setting.

---

## Future Improvements

- Refactor preprocessing using sklearn Pipelines  
- Add cross-validation and hyperparameter tuning  
- Improve feature selection and leakage handling  
- Introduce model explainability (e.g., SHAP)  
- Replace the GUI with a REST API (FastAPI)  

---

## Technologies Used

- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, tensorflow, matplotlib, seaborn  
- **GUI:** Tkinter  
- **Model Persistence:** joblib, Keras `.h5` models  

---

## Disclaimer

This project is for **educational and experimental purposes only** and should not be used for medical or dietary decision-making.
