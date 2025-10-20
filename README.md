# Delivery_time_prediction

## Project
Simple linear regression project to predict Delivery Time from Sorting Time using a small dataset. The analysis, model training, evaluation, and model persistence are implemented in the notebook.

## Files
- Dataset: [delivery_time.csv](delivery_time.csv)  
- Notebook: [delivery_time.ipynb](delivery_time.ipynb) — contains data processing, EDA, model training and evaluation. Referenced symbols in the notebook: [`df`](delivery_time.ipynb), [`x`](delivery_time.ipynb), [`y`](delivery_time.ipynb), [`x_train`](delivery_time.ipynb), [`x_test`](delivery_time.ipynb), [`y_train`](delivery_time.ipynb), [`y_test`](delivery_time.ipynb), [`lr_model_fit`](delivery_time.ipynb), [`loaded_model`](delivery_time.ipynb), [`delivery_sorting_lrmodel.sav`](delivery_time.ipynb).  
- This README: [README.md](README.md)

## Approach
- Exploratory Data Analysis and simple preprocessing performed in the notebook.
- Built a Simple Linear Regression model with scikit-learn: input = Sorting Time, target = Delivery Time.
- Train/test split: train_size=0.8, random_state=1234.

## Model
The fitted linear model follows:
$$\hat{y} = \beta_0 + \beta_1 x$$

Numeric fit (notebook outputs):
$$\hat{y} \approx 6.6638 + 1.6015\,x$$

Model persisted with joblib as `delivery_sorting_lrmodel.sav` (saved in the notebook).

## Evaluation (from notebook)
- R²: 0.5775 (approx)
- MAE: 1.9031
- MSE: 5.4622
- RMSE: 2.3371

These metrics are computed in the notebook; see the evaluation cells in [delivery_time.ipynb](delivery_time.ipynb).

## How to run
1. Open the notebook: [delivery_time.ipynb](delivery_time.ipynb) and run all cells.
2. Ensure the dataset [delivery_time.csv](delivery_time.csv) is in the same directory.
3. To reload the saved model in Python:
```python
# filepath: [README.md](http://_vscodecontentref_/0)
import joblib
model = joblib.load('delivery_sorting_lrmodel.sav')
```