project:
  name: Breast Cancer Prediction with MLflow
  description: >
    This project demonstrates how to train, evaluate, log, and test a machine learning model 
    using the breast cancer dataset from scikit-learn. It uses MLflow to track experiments,
    log metrics, and manage models.
  framework: scikit-learn
  experiment_tracking: MLflow

workflow:
  steps:
    - name: Load Dataset
      description: >
        Load breast cancer data using scikit-learn's built-in dataset loader. 
        Prepare the features (X) and labels (y).
    - name: Split Dataset
      description: >
        Split the data into training and testing sets (80/20 split).
    - name: Train Model
      description: >
        Train a RandomForestClassifier with 100 estimators and a fixed random seed.
    - name: Evaluate Model
      description: >
        Predict on the test set and calculate accuracy.
    - name: Log with MLflow
      description: >
        Log the model, parameters, and accuracy metric with MLflow.
        Include an input example to define model signature and remove MLflow warnings.
    - name: Test Saved Model
      description: >
        Load the saved model from MLflow using its run ID and test it on the test dataset.

dependencies:
  - pandas
  - numpy
  - scikit-learn
  - mlflow

outputs:
  - metrics:
      - name: accuracy
        type: float
        description: Accuracy of the model on the test set
  - artifacts:
      - name: model
        type: sklearn model
        description: Random forest classifier saved in MLflow with input example

notes:
  - Ensure the MLflow tracking server is properly set up if running in remote environments.
  - The warning about model signature is avoided by including an input_example during model logging.
  - You can extend this project by adding more models, hyperparameter tuning, or a user interface.

