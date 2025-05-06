# Employee Turnover Analytics

This project involves predicting employee turnover within a company using machine learning techniques. The goal is to identify the key factors contributing to employee turnover and suggest targeted retention strategies for employees at risk of leaving.

## Problem Statement

The HR Department at Portobello Tech has provided data regarding employees' work details, such as job satisfaction, number of projects, average monthly working hours, time spent in the company, promotions, salary, and evaluation ratings. The task is to analyze this data to predict employee turnover, determine the factors contributing to turnover, and suggest retention strategies.

### Key objectives include:

- Performing data quality checks
- Identifying significant factors affecting employee turnover
- Handling class imbalance in the dataset
- Training machine learning models and evaluating their performance using cross-validation
- Using the best model to predict employee turnover and suggest retention strategies

## Dataset

The data is modified from the Kaggle dataset: [HR Data](https://www.kaggle.com/liujiaqi/hr-comma-sepcsv).

### Column Description:

- **satisfaction_level**: Satisfaction level at the job of an employee
- **last_evaluation**: Rating between 0 and 1, received by an employee at their last evaluation
- **number_project**: The number of projects an employee is involved in
- **average_montly_hours**: Average number of hours an employee spends at the office each month
- **time_spend_company**: Number of years spent in the company
- **work_accident**: 0 - no accident, 1 - accident during employment
- **left**: 0 - employee stays, 1 - employee leaves the company
- **promotion_last_5years**: Number of promotions received by the employee in the last five years
- **department**: Department to which the employee belongs
- **salary**: Salary in USD

## Steps Taken

### 1. Data Quality Check:
   - Check for missing values in the dataset.

### 2. Exploratory Data Analysis (EDA):
   - Correlation matrix and heatmap for numerical features.
   - Distribution plots for employee satisfaction, evaluation, and average monthly hours.
   - Bar plot to compare the number of projects between employees who stayed and those who left.

### 3. Clustering:
   - K-Means clustering based on satisfaction level, evaluation, and whether the employee left or stayed.
   - Insights drawn from employee clusters.

### 4. Class Imbalance Handling:
   - Applied SMOTE (Synthetic Minority Oversampling Technique) to handle class imbalance.

### 5. Model Training and Evaluation:
   - Logistic Regression, Random Forest, and Gradient Boosting models trained with 5-fold cross-validation.
   - Evaluation metrics like ROC/AUC and confusion matrix were used to determine the best model.

### 6. Retention Strategy:
   - Used the best model to predict the probability of employee turnover.
   - Categorized employees into risk zones (Safe Zone, Low-Risk, Medium-Risk, High-Risk) based on the turnover probability.
   - Suggested targeted retention strategies for each zone.

## Requirements

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - imbalanced-learn (for SMOTE)
  - xgboost (for Gradient Boosting)

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
