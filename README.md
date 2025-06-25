# H1N1 and Seasonal Vaccine Prediction

# 🧬 H1N1 & Seasonal Vaccine Prediction (Multi-Output Classification)

A complete machine learning pipeline to predict vaccine uptake for H1N1 and seasonal flu based on behavioral, demographic, and health-related features. This project was submitted as part of a real-world ML challenge, and ranked **177 out of 7,450 participants**.

---

## 📌 Problem Statement

Given survey data from the 2009 H1N1 pandemic, the goal is to predict:
1. Whether a person received the **H1N1 vaccine**
2. Whether a person received the **seasonal flu vaccine**

This is a **multi-label classification** problem with two binary outputs per individual.

---

## 🛠 Tools & Techniques Used

### 🧠 Model Architecture
- **XGBoost Classifier** wrapped in **MultiOutputClassifier**
- Hyperparameter tuning with **Optuna**
- Final prediction using a **scikit-learn Pipeline**

### 🧼 Preprocessing
- **ColumnTransformer** to handle categorical vs. numeric features
- **SimpleImputer** to fill missing values
- **OneHotEncoder** and **StandardScaler** used as appropriate

### 🔁 Validation
- **StratifiedKFold** cross-validation to preserve label distribution
- **cross_val_predict** for out-of-fold predictions
- **ROC AUC** used for evaluation (separately for each target)

---

## 📈 Model Performance

| Label | AUC Score |
|-------|-----------|
| H1N1 Vaccine | 0.8758|
| Seasonal Vaccine | 0.8643|

- Final submission score: **Top 2.5% globally**
- Validation was robust due to out-of-fold prediction strategy

## 🏅 Challenge Info

- Dataset: Provided as part of the [DrivenData Vaccine Prediction Challenge](https://www.drivendata.org/competitions/)
- Rank: **177 / 7450** participants
- Platform: DrivenData.org

