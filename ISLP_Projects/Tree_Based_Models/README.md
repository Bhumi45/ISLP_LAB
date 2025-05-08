
## 🌲 Tree-Based Models

Tree-based methods are a class of non-linear models that split the feature space into rectangular regions. They’re intuitive, interpretable, and applicable to both regression and classification.

---

## 🧠 Core Concepts

### 🌿 1. Decision Trees

- **Regression Trees**: Predict a continuous outcome.
- **Classification Trees**: Predict a categorical outcome.

They partition data recursively and assign a constant prediction in each final (leaf) node.

### 🪓 2. Tree Construction

- Trees are built via **recursive binary splitting**.
- Splits are chosen by minimizing a **cost function**:
  - **Regression**: Residual Sum of Squares (RSS)
  - **Classification**: Gini, Entropy, or Misclassification Rate

---

## ✂️ Pruning

- Prevents **overfitting** by trimming back the full tree.
- **Cost complexity pruning** controls model complexity using a parameter \( \alpha \).

---

## 🧪 Ensemble Methods

### 🌳 Bagging

- Trains many trees on **bootstrapped** data samples.
- Final prediction is the **average** (regression) or **majority vote** (classification).
- **Reduces variance**.

### 🌲 Random Forests

- Like bagging, but each split only considers a **subset of predictors**.
- Improves accuracy by de-correlating trees.

### 🔥 Boosting

- Builds trees **sequentially**, each one correcting the errors of the previous.
- Controlled via:
  - **Learning rate**
  - **Number of trees**
  - **Tree depth**

### 📦 BART (Bayesian Additive Regression Trees)

- Bayesian model averaging over ensembles of trees.
- Captures uncertainty and performs regularization automatically.

---

## 📘 References

- *An Introduction to Statistical Learning*, Chapter 8
- [statlearning.com](https://www.statlearning.com)
