# Supervised-ML-Credit-Card-Default-Prediction

![credit card github image](https://github.com/Kovidk/Supervised-ML-Credit-Card-Default-Prediction/assets/20815224/9e379372-db05-461f-9b0f-fe32af6fb45a)

Problem Description

This project is aimed at predicting the case of customers default payments in Taiwan. From the perspective of risk management, the result of predictive accuracy of the estimated probability of default will be more valuable than the binary result of classification - credible or not credible clients.We can use the K-S chart to evaluate which customers will default on their credit card payments.

Data Desciption :

This dataset contains information on default payments, demographic factors, credit limit, history of payments, and bill statements of credit card clients in Taiwan from April 2005 to September 2005. It includes 30,000 rows and 25 columns, and there is no credit score or credit history information.

• ID: ID of each client

• LIMIT_BAL: Amount of given credit in NT dollars (includes individual and family/supplementary credit

• GENDER: Gender (1=male, 2=female)

• EDUCATION: (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)

• MARRIAGE: Marital status (1=married, 2=single, 3=others)

• AGE: Age in years

• PAY_0: Repayment status in September, 2005 (-1=pay duly, 1=payment delay for one month, 2=payment delay for two months,......,8=payment delay for eight months,9=payment delay for nine months and above)

• PAY_2: Repayment status in August, 2005 (scale same as above)

• PAY_3: Repayment status in July, 2005 (scale same as above)

• PAY_4: Repayment status in June, 2005 (scale same as above)

• PAY_5: Repayment status in May, 2005 (scale same as above)

• PAY_6: Repayment status in April, 2005 (scale same as above)

• BILL_AMT1: Amount of bill statement in September, 2005 (NT dollar)

• BILL_AMT2: Amount of bill statement in August, 2005 (NT dollar)

• BILL_AMT3: Amount of bill statement in July, 2005 (NT dollar)

• BILL_AMT4: Amount of bill statement in June, 2005 (NT dollar)

• BILL_AMT5: Amount of bill statement in May, 2005 (NT dollar)

• BILL_AMT6: Amount of bill statement in April, 2005 (NT dollar)

• PAY_AMT1: Amount of previous payment in September, 2005 (NT dollar)

• PAY_AMT2: Amount of previous payment in August, 2005 (NT dollar)

• PAY_AMT3: Amount of previous payment in July, 2005 (NT dollar)

• PAY_AMT4: Amount of previous payment in June, 2005 (NT dollar)

• PAY_AMT5: Amount of previous payment in May, 2005 (NT dollar)

• PAY_AMT6: Amount of previous payment in April, 2005 (NT dollar)

• default.payment.next.month: Default payment (1=yes, 0=no)

Algorithms Used :

(1) Logistic Regression

(2) Random Forest Classifier

(3) XGBoost Clssifier

(4) Support Vector Classifier


Conclusion:

I would recommend the Random Forest model due to its high recall value.

The best accuracy is obtained with both the Random Forest and XGBoost classifiers.

In general, all models have comparable accuracy. However, because the classes are imbalanced (the proportion of non-default credit cards is higher than default), accuracy can be misleading.

Furthermore, accuracy does not account for the rate of false positives (non-default credit cards predicted as default) and false negatives (default credit cards incorrectly predicted as non-default).

Both cases negatively impact the bank: false positives lead to unsatisfied customers, and false negatives lead to financial loss.

From the table, we can see that the Random Forest Classifier has Recall, F1-score, and ROC AUC values of 85.40%, 83.02%, and 91.15%, respectively. Similarly, the XGBoost Classifier has Recall, F1-score, and ROC AUC values of 85.11%, 82.77%, and 91.08%, respectively.

The Random Forest Classifier and XGBoost Classifier provide the best Recall, F1-score, and ROC AUC among the algorithms tested. We conclude that these two algorithms are the best for predicting whether a credit card will default according to our analysis.

To choose between these two algorithms, I would recommend the Random Forest Classifier due to its higher recall value, which is crucial since the ROC AUC scores are very similar.

Additionally, we found the optimal threshold value to be 0.506154, which is very close to the default threshold value of 0.50; therefore, we will not change the threshold value.

Key Points:
Model Recommendation: Random Forest due to higher recall.
Accuracy Considerations: Accuracy is not the best metric due to class imbalance.
Impact of False Positives/Negatives: Both have significant negative impacts.
Performance Metrics: Random Forest and XGBoost have the highest recall, F1-score, and ROC AUC.
Threshold Value: Optimal threshold is close to 0.50, so no change is needed.
This conclusion supports the use of the Random Forest model for its ability to better capture true positive cases, which is critical in minimizing financial losses due to undetected defaults.
