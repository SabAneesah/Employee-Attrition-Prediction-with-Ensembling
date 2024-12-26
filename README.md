# Employee Attrition Prediction with Ensembling

Objective : To predict employee attrition and identify the key factors driving it.

### Dataset Overview

Source: HR Analytics Dataset from Kaggle  

Dataset Size:
  * No. of variables: 26
  * No of targets: 1
Target Variable: Attrition (Binary: Yes/No)

### Data Preprocessing

* Feature Encoding: Encoded categorical variables (e.g., Gender, OverTime) using Label Encoding
* Removed irrelevant columns (e.g., EmployeeCount, EmployeeNumber).
* Feature Scaling: Standardized numeric features.

Rationale: To prepare data for effective model training and avoid biases.

### Model Selection

1. Logistic Regression - Helps to understand which features (e.g., salary, satisfaction) have the most significant effect on attrition.

2. Random Forest - Employee attrition is influenced by nonlinear relationships (e.g., interactions between job satisfaction and workload), which Random Forest captures well.

3. XGBoost - Complex interactions and subtle patterns in employee behavior can be captured more effectively with gradient boosting.

Ensemble Models: Stacking Classifier was used, combining base models with Logistic Regression as the meta-model. Combining multiple classifiers enhances accuracy and robustness, capturing complex patterns. 

### Key Insights

* The Stacking Ensemble model has the highest AUC of 0.82, indicating that it performs slightly better than the other models in distinguishing between classes.
* Both Logistic Regression and XGBoost have AUC values of 0.80, showing comparable performance.
* The Random Forest model has the lowest AUC of 0.78, suggesting it performs less effectively compared to the others.

**Effectiveness of Ensemble Learning:** The Stacking Ensemble's superior AUC highlights the effectiveness of combining multiple models to leverage their strengths, leading to better overall predictive performance.

