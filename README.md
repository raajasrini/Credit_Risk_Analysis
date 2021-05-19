# Credit_Risk_Analysis

## Overview 

The Credit Risk Analysis is being performed to help LendingClub predict and classify a loan as a good loan vs a risky loan using different machine learning techniques to "Q1 2019 LoanStats" data in order to predict credit risk. 

Using different models/algorithms , we are trying to understand which technique is going to be the most effective in terms of precision and sensitivity to classify a loan. Higher the models sensitivity, higher the chances of accurately determining a risky loan vs a good loan.

Used below models/algorithms to Predict the Credit Risk.

* **Resampling Models to Predict Credit Risk**
  * ReandomOverSampler
  * SMOTE
  * Cluster Centroids
 
* **SMOTEENN algorithm to Predict Credit Risk**

* **Ensemble Classifiers to Predict Credit Risk**

## Results 

We used above different algorithms to determine which algorithm results in the best performance compared to the oversampling algorithms. The Q1 2019 LoanStats data has been splitted into "test" and "train" the data using the algorithms and predicted with the folliowing steps:

1) View the count of the target classes using Counter from the collections library.
2) Use the resampled data to train a logistic regression model.
3) Calculate the balanced accuracy score from sklearn.metrics.
4) Print the confusion matrix from sklearn.metrics.
5) Generate a classication report using the imbalanced_classification_report from imbalanced-learn.

### Resampling Models to Predict Credit Risk

* **RandomOverSampler**

  * **Balanced Accuracy Score    : 65.12%**
  * **Precision Score - High Risk: 0.01**
  * **Precision Score - Low Risk : 1.00**
  * **Recall Score Difference    : 0.18%**

    ![RandomOverSampler](https://github.com/raajasrini/Credit_Risk_Analysis/blob/main/images/1-Oversampling.png)

* **SMOTE**

  * **Balanced Accuracy Score    : 65.48%**
  * **Precision Score - High Risk: 0.01**
  * **Precision Score - Low Risk : 1.00**
  * **Recall Score Difference    : 0.07%**

    ![SMOTE](https://github.com/raajasrini/Credit_Risk_Analysis/blob/main/images/2-SMOTE.png)

* **ClusterCentroids**

  * **Balanced Accuracy Score    : 54.42%**
  * **Precision Score - High Risk: 0.01**
  * **Precision Score - Low Risk : 1.00**
  * **Recall Score Difference    : 0.29%**
 
     ![ClusterCentriods](https://github.com/raajasrini/Credit_Risk_Analysis/blob/main/images/3-ClusterCentriods.png)

 
### Deliverable 2 :  SMOTEENN algorithm to Predict Credit Risk

* **SMOTEENN**

  * **Balanced Accuracy Score    : 68.06%**
  * **Precision Score - High Risk: 0.01**
  * **Precision Score - Low Risk : 1.00**
  * **Recall Score Difference    : 0.24%**
 
     ![SMOTEEN](https://github.com/raajasrini/Credit_Risk_Analysis/blob/main/images/4-SMOTEEN.png)


### Deliverable 3 :  Ensemble Classifiers to Predict Credit Risk

* **BalancedRandomForestClassifier**

  * **Balanced Accuracy Score    : 78.85%**
  * **Precision Score - High Risk: 0.03**
  * **Precision Score - Low Risk : 1.00**
  * **Recall Score Difference    : 0.17%
  * **The features are sorted in descending order by feature importance**
 
    ![BalancedRandomForestClassifier](https://github.com/raajasrini/Credit_Risk_Analysis/blob/main/images/5-BRF.png)

* **EasyEnsembleClassifier** 

  * **Balanced Accuracy Score    : 93.17%**
  * **Precision Score - High Risk: 0.09**
  * **Precision Score - Low Risk : 1.00**
  * **Recall Score Difference    : 0.02%**
 
     ![EasyEnsembleClassifier](https://github.com/raajasrini/Credit_Risk_Analysis/blob/main/images/6-EE.png)

 
## Summary 

Based on the 6 different methods, EasyEnsembleClassifier is the preferred method. It had the highest accuracy score of 93.17%. The next highest was score 14% below EasyEnsembleClassifier. It had the highest percission for high-risk at 0.09, when most other models had 0.01. And the smallest difference in recall score with 0.02%
