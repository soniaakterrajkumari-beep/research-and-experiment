# Experimental Methodology

## Data Pipeline
- Missing values handled via median imputation.
- Continuous numerical values scaled using `MinMaxScaler`.
- Categorical features encoded with One-Hot Encoding.

## Model Benchmarks
- **Decision Tree:** Criterion = Gini, Max Depth = 10.
- **Random Forest:** n_estimators = 100, Random State = 42.
- **Gradient Boosting:** Learning Rate = 0.1, n_estimators = 100.

## Evaluation Metrics
- Top-1 Accuracy Score
- Model Training Time (Seconds)
- 5-Fold Cross-Validation Score
