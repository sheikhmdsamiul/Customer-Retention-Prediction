# Customer Retention Prediction


## Project Overview
This repository contains an exploratory and modeling pipeline aimed at predicting customer churn (`Target_Churn`) using a customer dataset. The notebook walks through data understanding, feature engineering, baseline models (Logistic Regression, XGBoost, LightGBM), and an advanced model (ANN). The objective is to evaluate whether the available features can reliably predict churn and to provide actionable recommendations.


## Dataset Description
The dataset includes customer-level features such as demographics, purchase behavior, spending metrics, engagement indicators, and a binary churn target `Target_Churn`.


Representative columns used in the notebook (not exhaustive):
- `Customer_ID` (dropped during preprocessing)
- `Age`
- `Gender`
- `Annual_Income`
- `Total_Spend`
- `Years_as_Customer`
- `Num_of_Purchases`
- `Average_Transaction_Amount`
- `Num_of_Returns`
- `Num_of_Support_Contacts`
- `Satisfaction_Score`
- `Last_Purchase_Days_Ago`
- `Promotion_Response`
- `Email_Opt_In`
- `Target_Churn` (binary: churn vs no churn)


During EDA correlation results and the distribution plots, were not meningful enough. The distributions show that both churn and non-churn groups have almost identical distributions for most features!


Engineered features such as `Spend_to_Income_Ratio`, `Purchase_Frequency`, `Loyalty_Index`, and log-transformed spend variables.






## Evaluation
- Trained multiple models and evaluates performance on the test set. Despite using different architectures (including a feedforward neural net), all models converged around AUC ≈ 0.5. This indicates the issue lies in the data, not in the modeling.


## Key Results
- All evaluated models (Logistic Regression, XGBoost, LightGBM, ANN) produced performance near random (AUC ≈ 0.5, accuracy near 0.5).
- Confusion matrices demonstrate difficulty separating churn vs non-churn; ROC curves are close to the diagonal.
- EDA indicated very weak correlations between available features and the churn target, suggesting limited predictive information in the current dataset.


## Conclusions
- The current dataset does not contain sufficient predictive power to build an effective churn prediction model. The lack of meaningful correlations and visuals in EDA and the poor performance across various models suggest that the features are not capturing the underlying factors that drive customer churn in this context. Further investigation into the data collection process or the inclusion of new, more relevant features would be necessary to improve model performance.




## Files in this repository
- `Customer_Retention_Prediction.ipynb` — Notebook with Data Processing & EDA, feature engineering, model training, and evaluation.


