# Linear Regression – Quick Model Evaluation

Trains a Linear Regression model on real-world data (California Housing or fallback: Diabetes).
It covers data prep → training → evaluation → simple visualization → saving model info.

### Workflow

1. Load dataset (fetch_california_housing → fallback: load_diabetes)

2. Split data (80/20)

3. Standardize features (StandardScaler)

4. Train model (LinearRegression)

5. Evaluate via RMSE & MAE

6. Save:

- true_vs_pred.png (scatter plot)

- model_card.json (metrics summary)

### Example O/p

Dataset: California Housing, samples=20640, features=8
RMSE=0.72, MAE=0.53
Saved: true_vs_pred.png, model_card.json

Outputs: true_vs_pred.png → True vs Predicted plot

 
