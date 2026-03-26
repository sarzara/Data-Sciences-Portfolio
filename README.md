# Data-Sciences-Portfolio

This is my portfolio to share my ongoing and completed projects.
The table shows the languages, machine learning algorithms and
tools used for each project.

---

# Technical Skills

**Languages:** Python, Microsoft SQL Server

**Machine Learning:** Classification, Logistic Regression,
Random Forest, Decision Tree, SVM, XGBoost, Gradient Boosting,
KNN, Voting Ensemble, Regression, Clustering, Neural Networks,
Time Series Analysis

**Tools:** NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn,
Plotly, Jupyter Notebook

---

# Projects

| # | Title | Description | Skills & Tools | Status |
|---|-------|-------------|----------------|--------|
| 1 | **Heart Disease Prediction** | End-to-end ML pipeline to predict heart disease from 13 clinical features. Includes EDA, preprocessing, hyperparameter tuning (GridSearchCV), and evaluation of 8 models. Final model: Logistic Regression (AUC=0.93, Recall=0.92) | Python, Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn, Logistic Regression, Random Forest, SVM, XGBoost, Gradient Boosting, KNN, Decision Tree, Voting Ensemble, Pipeline, GridSearchCV | ✅ Completed |

---

# Project Details

## Heart Disease Prediction

**Dataset:** UCI Heart Disease (Cleveland) —
1,025 patients, 13 clinical features
[Kaggle Link](https://www.kaggle.com/datasets/ronitf/heart-disease-uci)

**Problem:** Binary classification — predict whether a patient
has heart disease based on routine clinical measurements.

**Pipeline Steps:**
- Exploratory Data Analysis (distributions, correlation
  heatmap, class balance)
- Data preprocessing (StandardScaler inside Pipeline,
  one-hot encoding of nominal features)
- Stratified 80/20 train-test split
- Hyperparameter tuning via GridSearchCV (5-Fold CV)
- Comparison of 8 models ranked by Recall (primary)
  and AUC-ROC (secondary)

**Results Summary:**

| Model | CV AUC | Test AUC | Accuracy | Recall |
|-------|--------|----------|----------|--------|
| Logistic Regression ★ | 0.85 | 0.93 | 89.7% | 0.92 |
| SVM | 0.86 | 0.94 | 85.9% | 0.88 |
| Voting Ensemble | 0.86 | 0.94 | 88.0% | 0.89 |
| XGBoost | 0.86 | 0.93 | 87.0% | 0.90 |
| Gradient Boosting | 0.85 | 0.92 | 87.0% | 0.91 |
| KNN | 0.85 | 0.93 | 86.4% | 0.88 |
| Random Forest | 0.86 | 0.92 | 86.4% | 0.86 |
| Decision Tree | 0.82 | 0.84 | 78.3% | 0.80 |

**Selected Model:** Logistic Regression
- Highest accuracy (89.7%) and Recall (0.92)
- Only missed 8 out of 102 heart disease patients
- Fully interpretable via coefficients and odds ratios
- Most suitable for clinical deployment

**Key Findings:**
- No overfitting detected — test AUC exceeded CV AUC
  across all models
- Most informative features: cp (chest pain type),
  max heart rate, oldpeak (ST depression),
  exang (exercise angina), slope (ST slope)
- No significant multicollinearity between features
- Logistic Regression selected over higher-AUC models
  due to superior Recall and full interpretability

