# Customer Churn Prediction using ANN

This project uses an Artificial Neural Network (ANN) built with Keras to predict customer churn based on a bank's customer data. The goal is to classify whether a customer will exit the bank or not based on features like credit score, age, tenure, balance, and more.

## Dataset

The dataset used is **Churn_Modelling.csv**, which includes the following features:

- Credit Score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Has Credit Card
- Is Active Member
- Estimated Salary
- Exited (Target Variable)

## Project Workflow

1. **Data Exploration and Cleaning**
   - Checked for missing values
   - Basic statistics and type inspection

2. **Data Visualization**
   - Bar plots, pie charts, and box plots to visualize churn distributions
   - Correlation heatmap for numerical features

3. **Feature Engineering**
   - One-hot encoding for categorical variables
   - Feature scaling using `StandardScaler`

4. **Model Building**
   - ANN with two hidden layers using ReLU and dropout for regularization
   - Compiled with Adam optimizer and binary crossentropy loss

5. **Model Training**
   - Used early stopping to prevent overfitting
   - Evaluated using accuracy, confusion matrix, and classification report

## Model Architecture

- Input Layer: 11 features
- Hidden Layer 1: 7 units, ReLU activation + Dropout(0.2)
- Hidden Layer 2: 6 units, ReLU activation + Dropout(0.3)
- Output Layer: 1 unit, Sigmoid activation

## Performance

## Model Performance

| Metric        | Class 0 (Not Exited) | Class 1 (Exited) |
|---------------|----------------------|------------------|
| Precision     | 0.85                 | 0.90             |
| Recall        | 0.99                 | 0.31             |
| F1-Score      | 0.92                 | 0.47             |
| Support       | 1595                 | 405              |

**Overall Metrics:**

- **Accuracy:** 85%
- **Macro Avg F1-Score:** 69%
- **Weighted Avg F1-Score:** 82%

## Technologies Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- TensorFlow / Keras
- Scikit-learn
