# Titanic - Machine Learning from Disaster (Kaggle)

This repository contains my submission for the classic Kaggle competition:  
**Titanic - Machine Learning from Disaster**

The goal is to predict which passengers survived the Titanic shipwreck using classification models.

---

## Project Highlights

- **Kaggle Accuracy**: `0.78947`
- **Leaderboard Rank**: `1446 / 16022` (Top ~9%)
- **Model**: Logistic Regression with custom random imputation and feature engineering
- **Notebook**: Fully self-contained Kaggle-style notebook with EDA, preprocessing, modeling, and submission

---

## Contents

- `titanic_notebook.ipynb`: Main notebook with code and analysis
- `submission_titanic.csv`: Final prediction file submitted to Kaggle
- `requirements.txt`: Python dependencies

---

## Data

You can download the original dataset from the Kaggle competition page:  
🔗 https://www.kaggle.com/competitions/titanic/data

Place `train.csv` and `test.csv` in a local `data/` folder if running offline.

---

## How to Run 

If you'd like to reproduce this locally:

```bash
git clone https://github.com/yourusername/titanic-survival-prediction.git
cd titanic-survival-prediction
pip install -r requirements.txt
'''

---

## 📊 Overview

This notebook walks through the following key steps:

### 1. Exploratory Data Analysis (EDA)
- Survival rate by gender and age
- Distribution analysis of age and fares

### 2. Feature Engineering
- Extracted **honorifics** from passenger names
- Grouped **cabins** by deck
- Calculated **family size** and identified **single mothers**
- Removed redundant/collinear features (e.g. high correlation between `SibSp` and `FamilySize`)

### 3. Imputation Techniques Explored
- Mean/Median/Mode imputation (with group-based logic)
- Random imputation (performed best)
- Stratified random sampling
- Advanced methods: **MICE**, **MissForest**, **KNN**

### 4. Feature Engineering & Preprocessing
- Capped outliers
- Log, Box-Cox, and Yeo-Johnson transformations
- Encoded rare labels in categorical columns
- Calculated permutation-based feature importances:
  - `Fare`: 0.103
  - `Pclass`: 0.099
  - `Age`: 0.083
  - `Sex_male`: 0.082
  - `Honorific_Mr`: 0.048

### 5. Modeling and Grid Search
- Built pipelines with:
  - Random Forest
  - Gradient Boosting
  - Logistic Regression
- **Final model**: `RandomForestClassifier` + `GridSearchCV`
  - Best Params: `max_depth=5`, `min_samples_split=10`, `n_estimators=30`
  - Train Accuracy: **0.851**
  - Test Accuracy: **0.825**

---

## 📈 Final Classification Report

'''bash 
 precision    recall  f1-score   support

       0       0.81      0.91      0.86       157
       1       0.85      0.70      0.77       111

accuracy                           0.82       268
macro avg      0.83      0.81      0.81       268
weighted avg   0.83      0.82      0.82       268
'''


