# 🔢 Busy Ratio Prediction for Food Delivery using Machine Learning

This project aims to predict the **busy_ratio** of restaurants in a food delivery network using historical restaurant, dasher, and order data. Multiple regression models were evaluated, including Lasso Regression, Random Forest, XGBoost, and AdaBoost.

---

## 📌 Objective

Predict the **busy_ratio** — a metric representing how busy a restaurant is — using engineered features such as:
- EMA/SMA indicators
- Dasher activity logs
- Store and time-based encodings
- Price range and item count

---

## 📁 Dataset

The dataset contains over **138,000 training records**, with validation and test sets of ~29,600 records each. Extensive feature engineering and selection were performed before modeling.

---

## ⚙️ Techniques Used

- Feature Engineering (EMA, SMA, EMA_diff, SMA_diff, log transformations)
- Feature Selection (XGBoost importance, Lasso regularization)
- Cross-validation (5-fold and 10-fold)
- Regression Modeling (Lasso, Decision Tree, Random Forest, XGBoost, AdaBoost)
- Evaluation (RMSE, R²)
- Visualization (Feature importance, residuals)

---

## 🧠 Models and Performance

| Model                | Train RMSE | Validation RMSE | Train R² | Validation R² |
|---------------------|------------|------------------|----------|----------------|
| **Lasso Regression**| 0.0133     | 0.0145           | 0.9988   | 0.9989         |
| Decision Tree       | 0.0296     | 0.0521           | 0.9942   | 0.9851         |
| Random Forest       | 0.0175     | 0.0500           | 0.9980   | 0.9863         |
| XGBoost             | 0.0078     | 0.1884           | 0.9996   | 0.8055         |
| AdaBoost            | 0.2397     | 0.2525           | 0.6193   | 0.6507         |

✅ Best overall model: **Lasso Regression**

---

## 📊 Feature Selection Summary

Top features (consistently selected across methods):
- `EMA`, `EMA_diff`, `SMA`, `SMA_diff`
- `total_busy_dashers_log`, `total_onshift_dashers_log`
- `delivery_time_diff`
- `subtotal`, `min_item_price`, `max_item_price`

---

## 🔍 Cross-Validation

- **5-Fold CV Average**: MSE = 0.0028, R² = 0.9827  
- **10-Fold CV Average**: MSE = 0.0028, R² = 0.9827

---

## 🛠️ Tech Stack

- Python (Pandas, NumPy, Scikit-learn, XGBoost)
- Jupyter Notebooks
- Matplotlib / Seaborn
- An more
