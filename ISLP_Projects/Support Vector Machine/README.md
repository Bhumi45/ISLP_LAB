# 🤖 Support Vector Machines – ISLR Chapter 9 Summary

Support Vector Machines (SVMs) are powerful classification methods that find the optimal hyperplane separating classes with the **maximum margin**. They are effective in high-dimensional spaces and are particularly useful for non-linear decision boundaries when combined with kernels.

---

## 📘 Core Concepts

### 1. Hyperplanes

A **hyperplane** is a decision boundary that separates different classes.

- In 2D: a line
- In 3D: a plane
- In general: a (p−1)-dimensional space in p-dimensional data

---

### 2. Maximal Margin Classifier (MMC)

- Finds the hyperplane that **maximizes the margin** (distance from the closest data points).
- Works only when data is **perfectly linearly separable**.
- The **support vectors** are the closest points that lie on the margin — they determine the hyperplane.

---

### 3. Support Vector Classifier (Soft Margin)

- **Generalization of MMC** for non-separable data.
- Introduces **slack variables** to allow misclassification.
- Optimizes a trade-off between **maximizing margin** and **minimizing classification error**.
- Controlled by tuning parameter **C**:
  - Large C: less tolerant of misclassification (low bias, high variance)
  - Small C: more tolerant (high bias, low variance)

---

### 4. Support Vector Machines

- Allows **non-linear classification** using the **kernel trick**.
- Instead of transforming the data manually, SVM uses a **kernel function** to compute inner products in a high-dimensional space without explicit transformation.

---

## 🧮 Kernel Functions

| Kernel Type        | Description                                  |
|--------------------|----------------------------------------------|
| **Linear**         | \( K(x, x') = x^T x' \)                      |
| **Polynomial**     | \( K(x, x') = (1 + x^T x')^d \)              |
| **Radial (RBF)**   | \( K(x, x') = \exp(-\gamma \|x - x'\|^2) \) |
| **Sigmoid**        | \( K(x, x') = \tanh(\alpha x^T x' + c) \)   |

The **Radial Basis Function (RBF)** is the most commonly used for complex, non-linear boundaries.

---

## 🔄 Multiclass Classification

SVM is inherently binary, but can be extended to multiple classes using:

- **One-vs-One**: Build SVM for each pair of classes.
- **One-vs-Rest**: Build one SVM per class vs. all others.

---

## 📊 Evaluation Metrics

- **Confusion Matrix**
- **Precision, Recall, F1 Score**
- **ROC Curve and AUC**
- **Cross-validation** is essential for tuning `C`, kernel parameters (e.g., `gamma` for RBF).

---

## 💡 Practical Considerations

- Effective in **high-dimensional spaces**
- Memory-efficient: depends only on **support vectors**
- Sensitive to choice of kernel and hyperparameters
- Scaling of features is important!

---

## 🔧 Tools in Python

- `scikit-learn`: `SVC`, `LinearSVC`
- Grid search: `GridSearchCV` to tune `C`, `gamma`, and `kernel`
- Plotting decision boundaries helps visualize performance on 2D datasets

---

## 📘 References

- Chapter 9 – *An Introduction to Statistical Learning*
- [https://www.statlearning.com](https://www.statlearning.com)
- [scikit-learn SVM documentation](https://scikit-learn.org/stable/modules/svm.html)

