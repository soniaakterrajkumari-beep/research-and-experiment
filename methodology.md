# Methodology

## 1. Research Question
* **Refined Question:** Can ensemble tree-based models (Random Forest) outperform linear baseline models (Ridge Regression) in accurately predicting house sale prices?

## 2. Dataset Description
* **Source:** Ames Housing Dataset.
* **Features:** 79 explanatory variables (square footage, year built, quality ratings, etc.).
* **Target Variable:** `SalePrice` (Continuous monetary value).
* **Size:** 1,460 rows and 81 columns.
* **Limitations:** Missing values in sparse categories and skewness in target distribution.

## 3. Data Cleaning Plan
* Impute numerical missing values using **median** and categorical using **mode**.
* Log-transform skewed numerical features and target variable `SalePrice`.

## 4. Feature Engineering Plan
* Create `TotalSF` = `TotalBsmtSF` + `1stFlrSF` + `2ndFlrSF`.
* Create `HouseAge` = `YrSold` - `YearBuilt`.
* Apply One-Hot Encoding and Standard Scaling.

## 5. Model Selection
* **Model 1 (Baseline):** **Ridge Regression**
* **Model 2 (Advanced):** **Random Forest Regressor**

## 6. Evaluation Metrics
* **Metrics:** Root Mean Squared Error (RMSE) on log scale and R2 Score.
