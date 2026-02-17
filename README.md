📊 Customer Churn Prediction using Machine Learning & Deep Learning
📌 Project Overview

This project focuses on predicting customer churn using both traditional Machine Learning and Deep Learning models.

The objective is to identify customers likely to leave the company so that proactive retention strategies can be implemented.

The project demonstrates:

End-to-end ML pipeline

Proper data preprocessing (encoding + scaling)

Handling imbalanced datasets

Model comparison (Logistic Regression vs Neural Network)

Threshold tuning

ROC & Precision–Recall curve analysis

Business-driven model evaluation

🎯 Problem Statement

Customer churn leads to revenue loss.
The goal is to build a classification model that predicts whether a customer will churn.

This is a binary classification problem:

1 → Churn

0 → No Churn

Since churn represents ~26% of customers, the dataset is imbalanced.
Therefore, recall for the churn class is prioritized over raw accuracy.

🗂 Dataset

Telco Customer Churn Dataset

~7,000 customers

20 features including:

Demographics

Service usage

Contract details

Monthly and total charges

⚙️ Data Preprocessing

The following steps were performed:

Removed customerID

Converted TotalCharges to numeric

Dropped rows with missing values

Converted target variable (Churn) to 0/1

Train-test split using stratification

One-Hot Encoding for categorical variables

Standard Scaling for numeric features

To prevent data leakage:

Encoders and scalers were fitted only on training data.

🤖 Models Implemented
1️⃣ Logistic Regression (Baseline Model)

Strong baseline for tabular data

Simple and interpretable

Achieved ~80% accuracy

Recall for churn ≈ 0.57

2️⃣ Neural Network (Deep Learning)

Architecture:

Dense (ReLU)

Dropout (regularization)

Dense (ReLU)

Dropout

Output layer with Sigmoid

Training Setup:

Binary Crossentropy loss

Adam optimizer

Early stopping

Batch size = 32

Neural Network Results:

Accuracy ≈ 80%

Threshold tuning improved recall from 0.54 → 0.78

Trade-off observed between recall and precision

📈 Evaluation Metrics

The models were evaluated using:

Accuracy

Precision

Recall

F1-score

Confusion Matrix

ROC Curve

Precision–Recall Curve

Primary business metric:

Recall for churn class (to minimize missed churners)

📊 ROC & Precision–Recall Analysis

ROC Curve:

Measures model’s ability to separate churn vs non-churn

AUC used for overall comparison

Precision–Recall Curve:

More informative for imbalanced datasets

Helps determine optimal classification threshold

Threshold tuning was performed to balance recall and precision.

🧠 Key Insights

Logistic Regression performed competitively on tabular data.

Deep Learning did not significantly outperform the baseline.

Lowering classification threshold increased recall substantially.

Business priorities determine the optimal threshold.

Deep Learning is not always superior for structured tabular datasets.

💼 Business Recommendation

For this dataset, Logistic Regression is recommended because:

Comparable performance

Better interpretability

Lower computational cost

Easier deployment

Deep Learning adds complexity without significant improvement.

🛠 Tech Stack

Python

Pandas

NumPy

Scikit-learn

TensorFlow / Keras

Matplotlib
