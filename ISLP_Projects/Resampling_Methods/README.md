# 📘 Summary: Resampling Methods (Chapter 5)

Resampling methods are essential tools in statistical learning to assess model performance, estimate accuracy, and reduce overfitting. They help us make better use of data, especially when data is limited.

---

## 🔹 1. Why Resampling?

- Evaluate model accuracy.
- Estimate test error without a separate test set.
- Tune hyperparameters (like `k` in KNN or `lambda` in ridge regression).

---

## 🔹 2. Cross-Validation (CV)

### a. Validation Set Approach
- Split data into training and test sets.
- Fit model on training data, test on validation set.
- Simple but has high variance depending on the random split.

### b. Leave-One-Out Cross-Validation (LOOCV)
- Train model on all data **except one point**, repeat for all points.
- Nearly unbiased, but computationally expensive for large datasets.

### c. k-Fold Cross-Validation
- Split data into **k folds**, train on k−1 folds, test on the remaining.
- Repeat for each fold and average the results.
- Common choice: **k = 5 or 10**
- Balances bias and variance better than LOOCV.

### d. Cross-Validation for Classification
- Use **classification error**, **precision**, **recall**, or **AUC** as metrics.

---

## 🔹 3. The Bootstrap

- Resample dataset **with replacement**, typically **B = 1000** times.
- Useful to estimate:
  - Standard errors
  - Confidence intervals
  - Model stability
- Does **not require a train-test split**.

---

## 🔹 4. Lab: Cross-Validation and Bootstrap in Python

- Demonstrates:
  - Validation set approach with `train_test_split`
  - k-Fold CV with `cross_val_score` from `scikit-learn`
  - Custom bootstrap procedures using NumPy and Pandas
- Applied to real-world datasets like `Auto` and `Portfolio`

---

## ✅ Summary Points

- Use **CV** to estimate **test error** and select models.
- Use the **bootstrap** to estimate **standard errors** and assess model **stability**.
- Both techniques improve model selection and generalization performance.


