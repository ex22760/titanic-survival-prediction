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

## Techniques Used

- Exploratory Data Analysis (EDA)
- Random sample imputation for numerical and categorical features
- Categorical encoding (e.g., one-hot, label encoding)
- Logistic Regression and baseline modeling
- Submission generation and performance evaluation

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
