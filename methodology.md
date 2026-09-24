# Methodology

## 1. Refined Research Question
* **Question:** Can an ensemble model (Random Forest Regressor) outperform a linear baseline model (Ridge Regression) in accurately predicting house sale prices using structural and spatial features?

## 2. Dataset Description
* **Source:** Ames Housing Dataset (via OpenIntro).
* **Target Variable:** `SalePrice` (Continuous monetary valuation of homes).
* **Features:** Structural and neighborhood characteristics including ground area, room counts, construction years, and quality ratings.
* **Limitations:** Contains sparse missing entries across structural columns and exhibits right-skewness in the raw price target distribution.

## 3. Data Cleaning Plan
* Impute continuous numerical missing values using the **median**.
* Impute missing categorical entries using the most frequent **mode**.
* Apply log-transformation (`np.log1p`) to normalise the target variable `SalePrice`.

## 4. Feature Engineering Plan
* Generate composite metric `TotalSF` from total area dimensions.
* Generate age metric `HouseAge` = `Year.Sold` - `Year.Built`.
* Encode categorical features using One-Hot Encoding (`pd.get_dummies`).
* Scale numerical inputs using `StandardScaler`.

## 5. Model Selection & Rationale
* **Baseline Model:** **Ridge Regression** — Selected as a linear benchmark to model underlying linear relationships while preventing overfitting through L2 regularization.
* **Advanced Model:** **Random Forest Regressor** — Selected as an ensemble tree model capable of capturing complex non-linear interactions and feature dependencies.

## 6. Evaluation Metrics & Rationale
* **Root Mean Squared Error (RMSE):** Selected to quantify prediction error magnitude on the log-scale, penalising larger errors appropriately.
* **R-squared Score ($R^2$):** Selected to evaluate the proportion of variance explained by the models relative to total variance.
