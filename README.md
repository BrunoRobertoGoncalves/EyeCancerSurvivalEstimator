# Eye Cancer Survival Estimator

This project applies advanced **machine learning techniques** to real-world clinical data in order to **predict the survival time (in months)** for patients with ocular cancer. The focus is on both predictive performance and **interpretability** using SHAP.

## ⚠️ Disclaimer: Predictive ≠ Causal

This machine learning model is **predictive**, not causal. It identifies statistical patterns in the dataset based on historical outcomes. It does **not** infer cause-and-effect relationships between variables.

For example:

- Patients who received more chemotherapy might show higher survival time in the model.
- This **does not mean** that increasing chemotherapy sessions causes longer life.
- In fact, this could reflect **survivorship bias** — those who live longer are able to receive more treatment.

### ⚠️ This tool is not a medical device

- It should **not be used for clinical decision-making**.
- It was built purely for **educational and exploratory purposes**.
- Always consult a healthcare professional for medical evaluation or prognosis.


## Overview

- Regression model using **XGBoost**
- Features include age, treatment types, stage, genetic markers, and family history
- Model interpretability with **SHAP values**
- Interactive UI to simulate patients and view predictions in real time
- Designed for portfolio use — clean, educational, and reproducible

---

## Dataset

The dataset contains anonymized records of patients diagnosed with eye cancer, including:

- `Age`
- `Cancer_Type`
- `Stage_at_Diagnosis`
- `Treatment_Type`
- `Chemotherapy` (number of cycles)
- `Surgery_Status`
- `Radiation_Therapy`
- `Genetic_Markers`
- `Family_History`
- `Survival_Time_Months` (**target variable**)

> ⚠️ *This dataset is fictitious and used for educational purposes only.*

---

## Techniques Used

- `XGBoostRegressor` for survival prediction
- Feature engineering (`Years_Since_Diagnosis`)
- Encoding categorical variables (`get_dummies`, `.cat.codes`)
- Evaluation metrics: **MAE**, **RMSE**, **R²**
- Model explainability using **SHAP**:
  - Global: `bar` and `beeswarm` plots
  - Local: `waterfall` plots per patient
- Interactive UI using `ipywidgets`

---

## How to Use the Estimator

Inside the notebook, scroll to the section:

```python
## 🧠 Eye Cancer Survival Estimator
