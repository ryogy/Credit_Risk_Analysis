# Credit Risk Analysis

## Overview of Analysis
The purpose of this analysis was to apply resampling and oversampling techniques to a credit card credit dataset and utilize machine learning algorithims to determine potential risk.  These tests will then be assesed for viability to determine real time credit-risk.

## Results
###  Naive Random Oversampling
* Balanced Accuracy Score: 64.6%

* In the high risk group, the precision is 1%, the sensitivity is 61% and the F1 score is 2%.  

* In the low risk group, the precision is approximately 100%, the sensitivity is 68%, and the F1 score is 81%.

* This model is very accurate at predicting low risk loans, but is less sufficient at identifying high risk loans with low precision and a generally high sensitivity.

### SMOTE Oversampling
* Balanced Accuracy Score: 62.3%

* In the high risk group, the precision is 1%, the sensitivity is 61%, and the F1 score is 2%.  

* In the low risk group, the precision is approximately 100%, the sensitivity is 64%, and the F1 score is 2%.

* This sampling method combined with the supervised machine learning linear regression produces very similiar results to the Naive Random Oversampling.

### Cluster Centroids 
* Balanced Accuracy Score: 52.9%

* In the high risk group, the precision is 1% and the sensitivity is 61%.  The F1 score is 1%.  Within the high risk group, the machine learning predictions are very similiar to the previous models. 

* In the low risk group, the precision is approximately 100%, the sensitivity is 45%, and the F1 score is 1%.

* The low risk group has a sensitivity of only 45% which is much lower than the other sampling methods wich both have sensitivities in 60-70% range.  This accounts for the lower F1 and balanced accuracy score in this model.  Due to the very high number of low risk loans it still is able to achieve precision rate of 100%.  However, if the dataset was a more balanced ratio of low risk to high risk loans the precision rate would likely to drop within the low risk loan group. 

### SMOTEENN 
* Balanced Accuracy Score: 61.6%

* In the high risk group, the precision is 1%, the sensitivity is 69%, and the F1 score is 2%.  

* In to low risk group, the precision is approximately 100%, and the sensitivity is 54%, and the F1 score is 70%.

* This test seems quie similiar to the others in overall performance metrics.  All are quite similiar when it comes to predicting low risk loans.

### Balanced Random Forest Classifier

* Balanced Accuracy Score: 78.8%

* In the high risk group, the precision is 4%, the sensitivity is 67%, and the F1 score is 7%.

* In the low risk group, the precision is approximately 100%, the sensitivity is 91%, and the F1 score is 95%

* Based on the above performance metrics. This is a fantastic model for predicting both low risk and high risk loans.

### Easy Ensemble AdaBoost Classifier

*  Balanced Accuracy Score: 92%

* In the high risk group, the precision is 7%, the sensitivity is 91%, and the F1 score is 14%

* In the low risk group, the precision is approximately 100%, the sensitivity is 94%, and the F1 score is 97%

*  This machine learning classifier produced the best performance metrics of ll the models, and would be the go to choice in using machine learning to accurately predict risky loans.



## Summary
The results indicate that predicting high risk loans with supervised machine learning is difficult.  All models proved to be very successfull at identifying low risk loans, so most of the models could be used at scale to predict loans with all high risk loans subject to human review.  From the testing, it is clear that the EasyEnsemble AdaBoost Classifier is the superior model.  The testing metrics are far better than the other models, boasting the highest precision, sensitivity, and F1 scores for both the high risk and low risk loans.

