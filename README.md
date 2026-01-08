# Linear Models Project – New York Housing Prices

## Description
This project predicts house prices in New York using a real dataset from Kaggle: [New York Housing Market](https://www.kaggle.com/nelgiriyewithana/new-york-housing-market).  
It demonstrates a complete machine learning workflow: **EDA, preprocessing, modeling, evaluation, and visualization**.

---

## Dataset
- **Source:** Kaggle
- **Target variable:** `PRICE`
- **Features:**  
  - **Numerical:** `BEDS`, `BATH`, `LATITUDE`, `LONGITUDE`  
  - **Categorical:** `TYPE`, `ADDRESS`, `STATE`, `MAIN_ADDRESS`, `ADMINISTRATIVE_AREA_LEVEL_2`, `LOCALITY`, `SUBLOCALITY`, `STREET_NAME`, `LONG_NAME`, `FORMATTED_ADDRESS`

---

## Preprocessing
- **Numerical pipeline:**  
  - Missing value imputation (mean)  
  - Standard scaling
- **Categorical pipeline:**  
  - Missing value imputation (most frequent)  
  - One-hot encoding (`handle_unknown='ignore'`)  

All preprocessing steps are combined using a **ColumnTransformer** and included in a **Pipeline**.

---

## Model
- **Linear models used:**  
  - Ridge Regression (with hyperparameter tuning for `alpha`)  
  - Optionally, LinearRegression or Lasso can be tested
- **Pipeline:** preprocessing + model
- **Hyperparameter tuning:** `GridSearchCV` with cross-validation (5 folds)

---

## Evaluation
- **Metrics used:**  
  - Mean Squared Error (MSE)  
  - Root Mean Squared Error (RMSE)  
  - R² score
- **Visualizations:**  
  - Scatter plot: predicted vs actual prices  
  - Histogram of prediction errors

---

## Results
- Ridge regression with optimal alpha gave the best R² score.  
- Predictions closely follow real prices, with most errors centered around zero.

---

## How to Run
1. Clone the repository:  
```bash
git clone <repo-url>
