# 30-Day Hospital Readmission Prediction

## Problem Statement
Hospital readmissions within 30 days of discharge are a major quality and cost concern in healthcare systems. High readmission rates increase operational costs and can trigger regulatory penalties.  
This project builds an end-to-end machine learning pipeline to predict whether a patient will be readmitted within 30 days of discharge using clinical and operational data.

## Dataset Description
The dataset contains patient-level records including demographics, admission characteristics, diagnoses, procedures, laboratory results, medications, and prior hospital utilization.

**Target Variable**
- `readmitted_30_days` (1 = readmitted within 30 days, 0 = not readmitted)

**Feature Categories**
- Patient demographics
- Admission type and length of stay
- Diagnoses and procedures
- Medication and lab indicators
- Prior hospital utilization

## Methodology
1. Exploratory data analysis to understand distributions, missingness, and class imbalance  
2. Data preprocessing and categorical encoding  
3. Feature engineering to derive clinically meaningful predictors  
4. Model development using baseline and ensemble methods  
5. Model evaluation using healthcare-relevant metrics  
6. Model explainability using SHAP  

## Modeling Approach
The following models were implemented and compared:
- Logistic Regression (baseline and interpretable)
- Random Forest
- Gradient Boosting (XGBoost)

Models were evaluated using ROC-AUC, precision-recall analysis, and confusion matrices to assess trade-offs between sensitivity and specificity.

## Explainability with SHAP
SHAP values were used to explain both global drivers of readmission risk and individual patient predictions. This ensures transparency and interpretability, which are critical for healthcare decision support.

## Key Findings
- Prior hospital utilization and length of stay were among the strongest predictors of readmission risk  
- Ensemble models outperformed baseline logistic regression  
- Explainability analysis provided actionable insights into readmission drivers  

## Repository Structure
- `data/` – raw and processed datasets  
- `notebooks/` – step-by-step analysis and modeling notebooks  
- `src/` – reusable preprocessing, modeling, and evaluation code  
- `results/` – figures and metrics  

## Tools & Technologies
Python, Pandas, NumPy, Scikit-learn, XGBoost, SHAP, Matplotlib, Seaborn
