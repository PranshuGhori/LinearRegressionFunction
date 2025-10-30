# 📊 MultiLinearRegression — From Scratch (No sklearn)

A from-scratch implementation of **Multiple Linear Regression** using pure **NumPy** and **Pandas** — built to understand the math behind OLS, generate Excel-style summaries, and compute key statistics like **R²**, **Adjusted R²**, and **Standard Errors** for each coefficient.

---

## 🚀 Features
- Supports multiple predictors (`*X` arguments)
- Adds intercept automatically
- Computes R², Adjusted R², SST, SSR, SSE
- Returns clean DataFrames (Model Summary + Coefficients)
- Accepts custom feature names

---

## 🧪 Example Usage

```python
TV = np.array([230.1, 44.5, 17.2, 151.5, 180.8])
Radio = np.array([37.8, 39.3, 45.9, 41.3, 10.8])
Newspaper = np.array([69.2, 45.1, 69.3, 58.5, 58.4])
Sales = np.array([22.1, 10.4, 9.3, 18.5, 12.9])

model_table, coef_table = MultiLinearRegression(
    TV, Radio, Newspaper,
    y=Sales,
    feature_names=["TV", "Radio", "Newspaper"]
)

print(model_table.round(4))
print(coef_table.round(4))
