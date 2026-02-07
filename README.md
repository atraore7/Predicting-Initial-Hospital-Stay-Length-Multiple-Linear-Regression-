# Predicting Initial Hospital Stay Length (Multiple Linear Regression)

## Overview
This project uses Multiple Linear Regression to identify which patient factors most strongly influence the initial number of days spent in the hospital. By analyzing demographic, clinical, and admission‑related variables, the model helps uncover key predictors that impact hospital stay duration, supporting more informed operational and patient‑care decisions.

## Business Question
What factors most significantly influence the number of initial days a patient spends in the hospital?

## Dataset
- Medical records containing demographic, clinical, and lifestyle variables

Target variable: Initial_days (continuous)

Predictor variables include:
- Income
- Initial_admin
- Stroke
- Complication_risk
- Arthritis
- Diabetes
- Hyperlipidemia
- Asthma
- ReAdmis
- Anxiety

Cleaned datasets and model inputs are stored in the data/ folder.

## Data Preparation
- Checked for duplicates and missing values (none found)
- Identified and capped outliers using Z‑score thresholds
- Converted Yes/No variables to binary (1/0)
- Encoded multi‑category variables using LabelEncoder
- Created a cleaned dataset for modeling

## Modeling Approach
- Technique: Multiple Linear Regression
- Checked for multicollinearity using Variance Inflation Factor (VIF)
- Built an initial model using all predictors
- Applied Backward Stepwise Elimination (α = 0.1) to remove non‑significant variables
- Compared initial and reduced models using:
- Adjusted R‑squared
- Residual Standard Error (RSE)

## Results
- Reduced model predictors: Arthritis, ReAdmis, Anxiety
- Regression equation: Y = 17 + 0.67 (Arthritis) + 46.43 (ReAdmis) + 0.54 (Anxiety)
- Adjusted R‑squared improved slightly in the reduced model
- Residual Standard Error decreased, indicating better model fit

## Insights
- Readmission status has the strongest impact on hospital stay length
- Patients with arthritis or anxiety tend to stay longer
- Reduced model performs similarly to the full model while being more interpretable
- Identifying these predictors helps hospitals understand which patient groups may require additional support or resources

## Conclusion
The Multiple Linear Regression model identifies key factors influencing hospital stay duration, with readmission status being the most impactful predictor. The reduced model provides a simpler, more interpretable solution without sacrificing performance. These insights can guide hospitals in resource allocation, patient care planning, and targeted interventions.
