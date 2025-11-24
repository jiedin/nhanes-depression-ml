# NHANES Depression ML Reproduction

This repository aims to reproduce the results of
**"Prediction of depressive disorder using
machine learning approaches: findings
from the NHANES"**  and explore possible improvement.


## 1. Data
Data source: NHANES 2013-2014 (CDC)
- Demographics
- Questionnaire (PHQ-9)
- Examination
- Laboratory


NHANES 2013–2014 public-use files can be downloaded from:  
https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2013  


## 2. Pipeline
1. Data loading and
preprocessing 
    - Combine raw data file
    - Construct analysis dataset and outcome variable (Y=1)
    - Handling miss data (Separately on training and test but same method)
    - One-hot encoding of categorical variables and normalization of continuous variables.

2. Feature Engineering (only training sets)
    - feature selection (lasso)
    - deal with imbalanced data (e.g. random under sampling or SMOTE)

3. Develop Model (training datasets)
    - Logistic Regression, RF, NB, SVM, Xgboost, LightGBM
    - Hyperparameter Tuning(Grid search + Cross-Validation)

4. Model Evaluation (Testing datasets)
    - Accuracy, Sensitivity, Specificity, Precision, AUC, F1-score

5. Model Explanation
    - SHAP Scores to analysed feature importance.

