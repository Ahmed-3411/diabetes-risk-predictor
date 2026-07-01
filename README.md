#  Diabetes Risk Predictor

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?style=flat-square&logo=scikitlearn)
![Gradio](https://img.shields.io/badge/Gradio-UI-yellow?style=flat-square&logo=gradio)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Views](https://visitor-badge.laobi.icu/badge?page_id=Mordekai66.diabetes-risk-predictor)

Binary classification pipeline that predicts diabetes risk from patient health and lifestyle features. Trains and compares Logistic Regression and Decision Tree classifiers, tunes hyperparameters via GridSearchCV, and exposes a Gradio interface for real-time risk assessment.

---

## Features

- Preprocessing: `dropna` for missing value removal, `LabelEncoder` per categorical column, `StandardScaler` for numeric features
- Model comparison: Logistic Regression vs. Decision Tree (Accuracy, Precision, Recall, F1)
- Hyperparameter tuning via `GridSearchCV` on Decision Tree (`max_depth`, `min_samples_split`) with 3-fold cross-validation
- Confusion matrix visualization for Logistic Regression with Seaborn
- Interactive Gradio UI for live diabetes risk prediction

---

## Dataset

File: `diabetes_risk_dataset.csv`

| Feature | Type |
|---|---|
| Age | Numeric |
| BMI | Numeric |
| Blood Pressure | Numeric |
| Physical Activity (hours/week) | Numeric |
| Family History | Categorical — Yes / No |
| Smoking Status | Categorical — Yes / No |
| **Diabetes Risk** | **Target — 0 / 1** |

---

## Setup

```bash
pip install -r requirements.txt
```

Place `diabetes_risk_dataset.csv` in the same directory as the notebook, then run all cells.

---

## Gradio Interface

After running the final cell, a local web UI launches. Enter age, BMI, blood pressure, and activity hours, then provide family history and smoking status as binary values (1 = Yes, 0 = No). The tuned Decision Tree model returns whether the patient is at risk of diabetes.

---

## Project Structure

```
.
├── Predicting_Diabetes_Risk.ipynb
├── diabetes_risk_dataset.csv
├── LICENSE
|── requirements.txt
├── .gitignore
└── README.md
```
