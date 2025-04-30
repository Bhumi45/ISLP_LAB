# 📘 Summary: Classification (Chapter 4)

Classification is a statistical learning task where the goal is to predict a **categorical** outcome (label or class) based on input variables.

## 🔹 1. Overview of Classification
- Predicts **class labels** (e.g., spam vs. not spam).
- Output variable is **qualitative** (not numeric).
- Performance is measured using **classification error rate**, accuracy, confusion matrix, etc.

## 🔹 2. Why Not Use Linear Regression?
- Linear regression isn't ideal for classification:
  - Can predict values outside the [0, 1] range.
  - Assumes linearity, which may not fit categorical outcomes well.

## 🔹 3. Logistic Regression
- Models the **probability** of class membership using a logistic function:
  $$
  P(Y = 1 \mid X) = \frac{e^{\beta_0 + \beta_1 X}}{1 + e^{\beta_0 + \beta_1 X}}
  $$
- Outputs values between 0 and 1.
- Classification is done by thresholding the probability (e.g., 0.5).

### Extensions:
- **Multiple logistic regression**: More predictors.
- **Multinomial logistic regression**: More than 2 classes.

## 🔹 4. Generative Models for Classification
### Linear Discriminant Analysis (LDA)
- Assumes predictors are normally distributed within each class.
- Estimates **class-conditional distributions** and uses Bayes’ Theorem.

### Quadratic Discriminant Analysis (QDA)
- Like LDA, but allows each class to have its **own covariance matrix**.
- More flexible than LDA, but requires more data.

### Naive Bayes
- Assumes predictors are **independent** given the class.
- Simple and effective, especially for high-dimensional data (e.g., text).

## 🔹 5. K-Nearest Neighbors (KNN)
- A non-parametric method.
- Classifies a new observation based on the **majority class** of its $k$ nearest neighbors.
- Flexible but can overfit with small $k$.

## 🔹 6. Model Comparison
- Performance varies by method and data.
- Trade-offs between **bias and variance**, **interpretability vs. flexibility**.

## 🔹 7. Generalized Linear Models (GLMs)
- Logistic regression is a special case of GLMs.
- Poisson regression can be used for **count data**.

## 🔹 8. Python Lab
- Demonstrates:
  - Logistic regression with `statsmodels` and `scikit-learn`
  - LDA, QDA, and Naive Bayes
  - KNN classification
  - Evaluation using **confusion matrices**, **ROC curves**, and **accuracy**

