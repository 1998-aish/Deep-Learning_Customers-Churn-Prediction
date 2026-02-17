# 📊 Customer Churn Prediction – ML & Deep Learning

## 📌 Project Overview

This project predicts customer churn using Machine Learning and Deep Learning models.

The objective is to identify customers likely to leave so that proactive retention strategies can be applied.

This project demonstrates:

- End-to-end ML pipeline
- Data preprocessing (encoding + scaling)
- Handling imbalanced data
- Model comparison
- Threshold tuning
- ROC & Precision–Recall analysis

---

## 🎯 Problem Statement

Customer churn leads to revenue loss.  
The goal is to predict whether a customer will churn.

This is a **binary classification problem**:

- `1` → Churn  
- `0` → No Churn  

Since churn represents ~26% of customers, recall is prioritized over raw accuracy.

---

## 🗂 Dataset

- Telco Customer Churn Dataset
- ~7,000 customers
- 20 features including:
  - Demographics
  - Contract details
  - Service usage
  - Monthly and total charges

---

## ⚙️ Data Preprocessing

- Removed `customerID`
- Converted `TotalCharges` to numeric
- Dropped missing values
- Encoded target variable (`Churn`) as 0/1
- Stratified train-test split
- One-Hot Encoding for categorical variables
- Standard Scaling for numerical features

To prevent data leakage:
- Encoders and scalers were fitted only on training data.

---

## 🤖 Models Implemented

### 1️⃣ Logistic Regression (Baseline)

- Strong tabular baseline
- Interpretable and efficient
- ~80% accuracy
- Recall (Churn) ≈ 0.57

---

### 2️⃣ Neural Network (Deep Learning)

Architecture:

- Dense (ReLU)
- Dropout
- Dense (ReLU)
- Dropout
- Output (Sigmoid)

Training Setup:

- Loss: Binary Crossentropy
- Optimizer: Adam
- Early stopping
- Batch size = 32

Results:

- Accuracy ≈ 80%
- Lowering threshold improved recall to ~0.78
- Trade-off between precision and recall observed

---

## 📊 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve
- Precision–Recall Curve

Primary Business Metric:

> Recall for churn class (to reduce missed churners)

---

## 📈 ROC & Precision–Recall Analysis

- ROC Curve measures class separation ability.
- AUC close to 1 indicates better performance.
- Precision–Recall Curve is more informative for imbalanced data.
- Threshold tuning improves business-focused performance.

---

## 🧠 Key Insights

- Logistic Regression performed competitively.
- Deep Learning did not significantly outperform baseline.
- Threshold tuning improved churn recall.
- Business metrics are more important than raw accuracy.
- Deep Learning is not always superior for structured tabular data.

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib

---

## 📁 Project Structure

```
churn-prediction-ml/
│
├── data/
├── notebook/
├── images/
├── README.md
```

---

## 👨‍💻 Author

Aish  
Data Science & Machine Learning Enthusiast
