# Churn Prediction Using Artificial Neural Networks (ANN)

## Introduction
This project aims to predict customer churn using Artificial Neural Networks (ANN). We utilize a dataset from Kaggle for this purpose.

## Dataset Cleaning
1. **Handling Missing Values**: 
    - Dropped columns with NaN values, as they were in type "object" and had a negligible number of missing entries compared to the total dataset.

2. **Data Transformation**:
    - Converted categorical columns into numerical format using **one-hot encoding**.

## Data Visualization
Visualized key aspects of the dataset to gain insights:
- ![Churn vs Tenure](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/08856bd9-284a-4b68-9bde-0f29d2e6c5fe)
- ![Customer vs Churn](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/fefab892-55fb-437b-b9bd-31fc499e16d6)

## Model Architecture
- **ANN Configuration**:
    - Three hidden layers with 40, 40, and 20 units, each utilizing **ReLU** activation.
    - Output layer with 1 unit using **sigmoid** activation for binary classification.

## Model Performance
- **Training and Validation Metrics**:
    - Accuracy: 81.68%
    - Loss: 0.3932
    - Validation Accuracy: 80.98%
    - Validation Loss: 0.4289

- **Test Metrics**:
    - Accuracy: 79.25%
    - Loss: 0.4468

## Classification Report
![Classification Report](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/89dbf241-5fe7-4c54-a0c6-196a41424f6d)

## Confusion Matrix
![Confusion Matrix](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/6ca5d873-e809-494a-9e4b-b0e7c4f4bc52)

