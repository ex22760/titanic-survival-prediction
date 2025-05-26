# Titanic - Machine Learning from Disaster 

This repository showcases my solution to Kaggle’s iconic Titanic: Machine Learning from Disaster competition — where the challenge is to predict passenger survival using real-world data and classification models. Featuring robust feature engineering, advanced imputation techniques, and a tuned Random Forest pipeline, this project achieved a top 10% accuracy score on the leaderboard.

---

## Project Highlights

- **Kaggle Accuracy**: `0.78947`
- **Leaderboard Rank**: `1446 / 16022` (Top ~9%)
- **Model**: Logistic Regression with custom random imputation and feature engineering
- **Notebook**: Fully self-contained Kaggle-style notebook with EDA, preprocessing, modeling, and submission

---

## Workflow

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
  
  ![image](https://github.com/user-attachments/assets/11f1ea5d-2d57-4a9a-a288-183a49678dbf)

  
  ![image](https://github.com/user-attachments/assets/660a508b-0502-4d61-9a5f-6e6981d346a9)


- Stratified random sampling
- Advanced methods: **MICE**, **MissForest**, **KNN**

### 4. Feature Engineering & Preprocessing
- Capped outliers
- Log, Box-Cox, and Yeo-Johnson transformations

  
  ![image](https://github.com/user-attachments/assets/1137d0a4-28b9-47ad-97e9-282f57584fe5)

- Encoded rare labels in categorical columns
- Calculated permutation-based feature importances:

  
![image](https://github.com/user-attachments/assets/a30ccf30-86cf-476d-955b-74f5e1c56279)



### 5. Modelling and Grid Search

| Pipeline                         | Train Accuracy | Test Accuracy |
|---------------------------------|----------------|---------------|
| Random Forest Classification     | 0.995          | 0.802         |
| Gradient Boosting Classification | 0.915          | 0.802         |
| Logistic Regression              | 0.839          | 0.821         |
| **Random Forest with Grid Search** | **0.851**    | **0.825**     |
| Gradient Boosting with Grid Search | 0.909        | 0.795         |
| Logistic Regression with Grid Search | 0.833       | 0.810         |

  - Random Forest with Grid search performed best with best parameters: `max_depth=5`, `min_samples_split=10`, `n_estimators=30`


---

## Final Classification Report

| Class   | Precision | Recall | F1-Score | Support |
|---------|-----------|--------|----------|---------|
| 0       | 0.81      | 0.91   | 0.86     | 157     |
| 1       | 0.85      | 0.70   | 0.77     | 111     |
| **Accuracy** |           |        | **0.82**   | 268     |
| **Macro Avg** | 0.83      | 0.81   | 0.81     | 268     |
| **Weighted Avg** | 0.83  | 0.82   | 0.82     | 268     |


---

## How to Run 

1. Clone the repository:

```bash
git clone https://github.com/ex22760/titanic-survival-prediction.git
cd titanic-survival-prediction
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Launch the notebook:

```bash
jupyter notebook titanic_survival_analysis.ipynb
```

---

## Folder Structure

```bash

├── data/                   # Raw datasets used for the competition
├── titanic_notebook.ipynb  # Main notebook with code and analysis
├── submission_titanic.csv  # Final prediction file submitted to Kaggle
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
```

---

## Acknowledgements

Developed as part of the Titanic: Machine Learning from Disaster competition.

![image](https://github.com/user-attachments/assets/609478e2-b15a-4588-8f61-cdd6716bdf9e)

---

## Contact

**Sujin Subanthran**

[LinkedIn Profile](https://www.linkedin.com/in/sujin-subanthran-b44512226/)
