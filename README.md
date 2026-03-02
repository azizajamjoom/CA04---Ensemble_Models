# CA04 — Ensemble Models

## Overview
This project evaluates multiple ensemble machine learning models using the Census Income dataset. The goal is to compare model performance by analyzing Accuracy and AUC while tuning the number of estimators for each algorithm.

Models implemented:
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost

---

## Dataset
The dataset comes from the U.S. Census Bureau and is used to predict whether an individual earns more than $50K annually.

Source:
https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true

- Target Classes: >50K and <=50K
- Total Records: 48,842
- Features: 7 demographic variables

Data preprocessing and encoding steps were reused from CA03.

---

## Methodology

### Data Preparation
- Loaded dataset from GitHub
- Encoded categorical variables using OrdinalEncoder
- Applied same transformations from CA03
- Split data into training and testing sets using the `flag` column

### Model Training
Each model was trained using:
n_estimators = [50,100,150,200,250,300,350,400,450,500]

For each value:
- Model trained on training data
- Predictions generated on test data
- Accuracy and AUC calculated
- Performance visualized using line plots

---

## Results

| Metric | Random Forest | AdaBoost | Gradient Boost | XGBoost |
|-------|---------------|----------|----------------|---------|
| Accuracy | 0.8385 | 0.8450 | **0.8471** | 0.8464 |
| AUC | 0.8815 | 0.8814 | **0.8994** | 0.8971 |

Gradient Boost achieved the best overall performance, followed closely by XGBoost.

---

## Key Insights
- Boosting models outperformed Random Forest.
- Performance improved initially with more estimators but plateaued afterward.
- Gradient Boost provided the best balance between accuracy and stability.

---

## Files Included
- `CA04_Ensemble_Models.ipynb` — Fully executed notebook
- `README.md` — Project documentation

---

## Requirements
Python libraries used:
- pandas
- numpy
- matplotlib
- scikit-learn
- xgboost

---

## Author
Aziza Jamjoom 
Mary Tekele
MSBA — Loyola Marymount University
