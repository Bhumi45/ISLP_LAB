
# 📘 Summary: Linear Regression (Chapter 3)

Linear regression is one of the most fundamental and widely used methods in statistical learning. It models the relationship between a dependent variable and one or more independent variables.

## 🔹 1. Simple Linear Regression
- **Goal**: Predict a response variable \( Y \) using one predictor \( X \).
- **Model**:  
  \( Y = \beta_0 + \beta_1 X + \varepsilon \)
- \( \beta_0 \): intercept, \( \beta_1 \): slope.
- Fitted using **least squares**, minimizing the residual sum of squares (RSS).

## 🔹 2. Multiple Linear Regression
- Uses **multiple predictors** \( X_1, X_2, ..., X_p \).
- **Model**:  
  \( Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \cdots + \beta_p X_p + \varepsilon \)
- Allows capturing more complex relationships.

## 🔹 3. Model Assessment
- **Coefficient accuracy**: Estimated using **standard errors** and **confidence intervals**.
- **Model accuracy**:
  - **R-squared**: Proportion of variance in \( Y \) explained by the model.
  - **F-statistic**: Tests if at least one predictor is useful.

## 🔹 4. Important Considerations
- **Qualitative predictors**: Can be included using dummy variables.
- **Interactions**: Model combined effects of predictors (e.g., \( X_1 \times X_2 \)).
- **Non-linear transformations**: Add \( X^2, \log(X) \), etc., to model curvature.
- **Diagnostics**: Check assumptions (linearity, constant variance, etc.) using residual plots.

## 🔹 5. Python Lab
- Covers:
  - Fitting models with `statsmodels` and `scikit-learn`
  - Making predictions
  - Interpreting coefficients
  - Visualizing regression lines
  - Handling qualitative variables and interactions
