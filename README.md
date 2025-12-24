# Building Regression models

This project demonstrates end-to-end implementation of traditional machine learning models
with a focus on **interpretability, diagnostics, and generalization**.

## 📌 Project Highlights
- Built an interpretable Linear Regression model for house price prediction
- Performed detailed EDA and feature analysis
- Evaluated model using RMSE and R²
- Conducted residual diagnostics to validate assumptions
- Applied Ridge and Lasso regularization
- Used cross-validation to confirm generalization

## 🧠 Key Learnings
- Simple models can outperform complex ones on clean data
- Residual analysis is critical for validating regression assumptions
- Regularization introduces bias–variance trade-offs
- Cross-validation prevents overconfidence from a single data split

## 📊 Observations & Results

- A baseline **Linear Regression** model using only *house size* and *number of rooms* achieved an **RMSE of ~₹2.01 lakh** on the test set, with an **R² of ~0.95**, indicating that the model explains approximately **95% of the variance** in house prices.

- **Model coefficients were intuitive and interpretable**:
  - Each additional **square foot** of area is associated with an increase of approximately **₹4,425** in house price, holding other variables constant.
  - Each additional **room** is associated with an increase of approximately **₹6.5 lakh**, capturing layout and space-driven value effects.

- **Residual diagnostics validated model assumptions**:
  - Residuals were centered around zero with no clear patterns in the residuals vs predictions plot, suggesting the model captured the primary linear structure of the data.
  - Most residuals fell within **±₹2–3 lakh**, consistent with the observed RMSE.

- Applying **Ridge Regression (L2 regularization)** resulted in a higher **RMSE of ~₹2.38 lakh** and a lower **R² of ~0.93**, indicating that regularization introduced unnecessary bias for this low-dimensional and stable dataset.

- **5-fold cross-validation** produced a **mean RMSE of ~₹1.76 lakh**, with fold-wise errors ranging from approximately **₹1.28 lakh to ₹2.50 lakh**, confirming that the model’s performance is **stable across different data splits**.

- Overall, results show that a **simple, interpretable linear regression model** provides a strong and reliable baseline, and that additional complexity does not improve performance for this dataset.


## 🛠 Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn


