

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

## Handling Imbalanced Dataset
### Method 1: Undersampling
- **Description**:
    - Undersampling involves reducing the number of instances in the majority class (churn = 0) to match the number of instances in the minority class (churn = 1).
- **Steps**:
    1. Identify the majority and minority classes in the dataset.
    2. Randomly sample instances from the majority class to match the size of the minority class.
    3. Train the model on the balanced dataset.
- **Results**:
    - Improved F1 score compared to the imbalanced dataset.
- ![CR_Undersampling](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/43fa6e58-d7bd-4504-8173-0cb7baebaf1b)

### Method 2: Oversampling
- **Description**:
    - Oversampling involves increasing the number of instances in the minority class (churn = 1) to match the number of instances in the majority class (churn = 0).
- **Steps**:
    1. Identify the majority and minority classes in the dataset.
    2. Duplicate instances from the minority class to match the size of the majority class.
    3. Train the model on the balanced dataset.
- **Results**:
    - F1 score increased compared to the imbalanced dataset.
- ![CR_Oversampling_Duplication](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/2b397eb3-bb6a-42ed-9cb4-4012c7961d86)

### Method 3: SMOTE (Synthetic Minority Over-sampling Technique)
- **Description**:
    - SMOTE generates synthetic samples for the minority class by interpolating between existing instances using the K-nearest neighbors algorithm.
- **Steps**:
    1. Identify the majority and minority classes in the dataset.
    2. Generate synthetic samples for the minority class by **KNN** to match the size of the majority class.
    3. Train the model on the balanced dataset.
- **Results**:
    - Achieved the best F1 score among all methods.
- ![CR_SMOTE](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/f3e56185-5e70-4622-9f72-03549a0642f7)

## Methods Comparison
- Compared the performance of different methods for handling imbalanced datasets.
- Found that SMOTE outperformed undersampling and simple oversampling.

## Conclusion
- Chose SMOTE as the method for handling the imbalanced dataset.
- Trained the final model using the balanced dataset and evaluated its performance.
- Achieved improved performance in terms of F1 score and overall model accuracy.
- ![Confusion Matrix with SMOTE](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/24c70990-1e00-413a-be19-f548360e3cda)

