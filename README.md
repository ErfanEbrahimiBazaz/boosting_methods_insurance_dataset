# Making classifier by sing XGBoost, Lightgbm nd catBoost

The train data set has 11 features. Renewal is the target value. The objective is to make a classifier to predict if a user will remain by the insurance, or they will cancel. 0 
in target value means leaving the insurance, while 1 implies staying.

## Methodology

1. By using cross validation by kfold 5, train data set has been splitted. 
2. Fit an XGBoost model.
3. Predict the values and calculate f1_score.
4. Determine the significance of each feature on target value prediction.
5. The same process has been done with Lightgbm.

After determining the importance of each feature on prediction, in XGBoost model only few features have significant impact on target value. In this section features are filtered 
based on their importance and are normalized before being applied to each model.

Two normalization techniques are used:

+ min max scaling
+ Z score

#### Imprtant features for xgboost model
+ Count_6.12_months_late
+ Count_3.6_months_late
+ Count_more_than_12_months_late
+ perc_premium_paid_by_cash_credit


