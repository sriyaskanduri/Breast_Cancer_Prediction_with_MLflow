# 🧠 Breast Cancer Prediction with MLflow

This project demonstrates how to build, evaluate, and track a machine learning model using the Breast Cancer dataset from scikit-learn. It uses **MLflow** for experiment tracking and model management.

## 📌 Project Overview

- **Dataset**: Breast Cancer Wisconsin Diagnostic dataset (`sklearn.datasets`)
- **Model**: Random Forest Classifier
- **Experiment Tracking**: MLflow
- **Purpose**: Train a classifier, log parameters and metrics, save the model, and test the saved model.

---

## 🚀 Features

- Load and explore the Breast Cancer dataset
- Train/test split for evaluation
- Train a RandomForestClassifier
- Log model, parameters, and accuracy using MLflow
- Load and test the saved model
- Example input provided to suppress MLflow signature warnings

---

## 🧰 Requirements

Install dependencies using pip:

```bash
pip install pandas numpy scikit-learn mlflow


Model trained and saved! Run ID: 123abc456xyz

🔍 Testing the saved model on the test data...

✅ Accuracy of the loaded model on test data: 0.9737

🔮 Sample Predictions:
Features: [17.99 10.38 ...]
True Label: 0 - Predicted: 0
...
