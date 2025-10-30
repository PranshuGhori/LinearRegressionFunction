# 📊 MultiLinearRegression — From Scratch

A pure NumPy and Pandas implementation to learn the math behind multiple linear regression and Ordinary Least Squares (OLS).

---

## 🚀 What This Project Does

- Fits multiple linear regression using matrix algebra (no sklearn)
- Calculates R² and Adjusted R²
- Summarizes model and coefficients in DataFrames

---

## 🧠 Math Used

**OLS Estimate:**  
`beta_hat = (X.T @ X)^(-1) @ X.T @ y`

**Goodness of Fit:**  
`R^2 = 1 - (SSE / SST)`  
`Adjusted R^2 = 1 - (1 - R^2) * ((n - 1) / (n - p - 1))`

- **SST** (Total Sum of Squares): `sum((y_i - mean(y))^2)`
- **SSR** (Explained Sum of Squares): `sum((y_hat_i - mean(y))^2)`
- **SSE** (Residual Sum of Squares): `sum((y_i - y_hat_i)^2)`
- **n**: Number of observations
- **p**: Number of predictors

**Standard Error of Coefficients:**  
`SE_beta = sqrt( diag(MSE * (X.T @ X)^(-1)) )`  
where `MSE = SSE / (n - p - 1)`

---

## 📦 Requirements

- Python
- NumPy
- Pandas
