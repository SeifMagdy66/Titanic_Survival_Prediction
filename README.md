# Titanic Survival Prediction (Machine Learning Project)

## Overview
This project applies fundamental machine learning techniques to the famous **Titanic: Machine Learning from Disaster** dataset hosted on Kaggle. The objective is to build a classification model capable of predicting the survival status of passengers (`Survived` = 1) or non-survival (`Survived` = 0) based on various features such as age, gender, passenger class, and family size.

### Key Components:
* **Model Used:** Tuned Random Forest Classifier.
* **Final Kaggle Public Score:** **0.77751** (77.75% Accuracy).

---

## 🧪 Methodology

### 1. Data Cleaning and Preprocessing
* **Missing Data:** Handled missing values in `Age`, `Fare`, and `Embarked` columns using imputation (median or mode).
* **Dropping Features:** Columns with low predictive power or high missingness (`Cabin`, `Name`, `Ticket`) were removed or used for engineering and then dropped.

### 2. Feature Engineering
A crucial step involved creating a predictive feature:
* **Family Category:** Derived from `SibSp` and `Parch` columns to categorize passengers into **Solo**, **Small Family (2-4)**, or **Large Family (5+)**.

### 3. Model Optimization
* **Algorithm:** The **Random Forest Classifier** was chosen due to its robustness.
* **Tuning:** The model was significantly optimized using **GridSearchCV** to find the best hyperparameters (`n_estimators=300`, `max_depth=8`, `min_samples_split=5`), leading to the final high-performing model.

---

## 📂 Project Files

| File Name | Description |
| :--- | :--- |
| **`titanic_train.ipynb`** | **The main code file (Jupyter Notebook)** containing the full workflow: EDA, cleaning, feature engineering, model training, tuning (Grid Search), and final prediction. |
| `train.csv` & `test.csv` | The original dataset files used for training and testing. |
| `titanic_submission_final_tuned.csv` | The final prediction file submitted to Kaggle to achieve the score of 0.77751. |
| `LICENSE` | The MIT License file, defining usage rights. |
