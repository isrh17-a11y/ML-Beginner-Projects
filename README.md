# Breast-Cancer-Prediction-
A binary classification project using Logistic Regression to predict whether a breast tumor is malignant or benign.

Uses scikit-learn's built-in load_breast_cancer dataset (30 numeric features per tumor: radius, texture, smoothness, etc.)
Splits data 80/20, scales features with StandardScaler, trains a LogisticRegression model
Reports test accuracy
Includes a single-sample prediction demo on one real tumor record, printing "Benign" or "Malignant"
