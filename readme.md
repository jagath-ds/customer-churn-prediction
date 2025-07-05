# 🧠 Customer Churn Prediction using Machine Learning

This project aims to predict customer churn using various supervised ML algorithms. We analyze customer demographics and behavior to predict if a customer is likely to leave the bank — enabling proactive retention strategies.

---

## 📌 Objective

Customer churn costs banks significant revenue. By identifying potential churners early, we can take data-driven actions to retain them. This project builds a classifier to flag customers at risk based on real-world features.

---

## 🗃️ Dataset

- ✅ 10,000+ bank customers
- 🎯 Target column: `Exited` (1 = churned, 0 = retained)
- 📊 Features include: Age, Geography, Balance, NumOfProducts, IsActiveMember, etc.

**Preprocessing steps:**
- Dropped irrelevant columns (`Surname`, `CustomerId`, `RowNumber`)
- Label encoded `Gender` and one-hot encoded `Geography`
- Balanced dataset using **SMOTE**
- Scaled features using **StandardScaler**

---

## 🤖 Models Used

| Model               | Precision | Recall (Churn) | F1-Score | ROC AUC |
|---------------------|-----------|----------------|----------|---------|
| Logistic Regression | 0.36      | 0.65           | 0.46     | 0.73    |
| Random Forest       | 0.73      | 0.49           | 0.58     | 0.85    |
| XGBoost             | 0.67      | 0.50           | 0.58     | 0.84    |
| LightGBM            | 0.69      | 0.50           | 0.58     | 0.86    |
| CatBoost            | 0.75      | 0.52           | 0.61     | 0.87 ✅ |

📌 **CatBoost** performed best with highest AUC and F1-Score.

---

## 📊 Visual Insights

The notebook includes clear visualizations for understanding key churn drivers:

- Churn rate by number of products
- Churn by geography, age group, and activity status
- Stacked bar plots comparing churned vs retained customers

These visuals help bridge technical findings with business actions.
