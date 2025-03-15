# Diabetes Prediction Using Linear Models

## Overview
This project focuses on predicting diabetes using health-related features while adhering to competition constraints that **only allowed linear models**. The analysis covers data preprocessing, feature selection, model training, and evaluation.

## Methodology

### 1. Data Loading and Preprocessing
- The dataset was loaded from a CSV file.
- Missing values were handled using imputation techniques.
- Feature scaling and encoding were applied where necessary.

### 2. Exploratory Data Analysis (EDA)
- **Correlation Analysis**:  
  - Analyzed numerical variables such as **age, BMI, HbA1c level, and blood glucose level** for their relationship with diabetes.
  - Generated a heatmap to visualize correlations.
- **Class Distribution**:  
  - Identified class imbalance but **did not use SMOTE**, as it led to worse model performance.

### 3. Feature Engineering
- **Feature Selection**:  
  - Selected the most relevant features using statistical tests and correlation analysis.
- **Handling Imbalance**:  
  - Instead of oversampling methods, adjustments were made to ensure models were not biased by class imbalance.

### 4. Model Training & Evaluation
- **Competition Constraint**:  
  - **Only linear models** were allowed, so non-linear models (e.g., Random Forest, Gradient Boosting) were **not used**.
- **Models Implemented**:
  - Logistic Regression
  - Linear Regression Variants
  - Regularization Techniques (Ridge & Lasso)
- **Evaluation Metrics**:
  - Accuracy, Precision, Recall, F1-score, ROC-AUC
  - **Brier Score Loss** was used as a key metric for model calibration.

### 5. Cross-Validation & Hyperparameter Tuning
- **Stratified K-Fold Cross-Validation** ensured robust evaluation.
- **Hyperparameter tuning** optimized model performance while maintaining interpretability.

## Key Findings
1. **Blood glucose level and HbA1c level were the strongest predictors** of diabetes.
2. **Using SMOTE worsened results**, so alternative balancing techniques were considered.
3. **Feature selection improved model generalization** and reduced overfitting.
4. **Regularization techniques (Ridge, Lasso) improved model stability** and reduced variance.
5. **Stratified K-Fold Cross-Validation provided consistent performance across different splits.**

## Future Improvements
- Experiment with **more complex linear models** within competition constraints.
- Improve feature selection to **reduce collinearity and improve interpretability**.
- Investigate **alternative ways to handle class imbalance** without affecting model performance.

This project demonstrates a **rigorous and competition-compliant approach** to diabetes prediction using statistical methods, feature engineering, and optimized linear models.
