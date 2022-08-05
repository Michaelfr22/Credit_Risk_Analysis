# Credit_Risk_Analysis

## Overview

Credit risk is a perfect example of a classification imbalance. When it comes to determining if an individual's credit risk is low or high, their profile can be compared to historical data clusters to see what level of risk the profile represents. The purpose of this analysis is to employ different strategies to train and evaluate machine learning models using resampling. These models are expected to become increasingly accurate as new data is considered. The information being analyzed in this project is credit card data from a peer-to-peer lending services company; LendingClub.

### Strategies Employed

1. Naive (Random) Oversampling
2. Synthetic Minorty Oversampling Technique (SMOTE)
3. Cluster Centroid Undersampling
4. Combination - SMOTE & Edited Nearest Neighbors algorithms (SMOTEENN)
5. Machine Learning Model 1: BalancedRandomForestClassifier
6. Machine Learning Model 2: EasyEnsembleClassifier

## Results

**1. Naive (Random) Oversampling**
 - Balanced Accuracy Score: **54.5%**

![naive_report](https://user-images.githubusercontent.com/102773052/182994534-c07ee4c0-bf6e-465d-8e4a-970fcce7bfb2.png)

**2. Synthetic Minorty Oversampling Technique (SMOTE)**
- Balanced Accuracy Score: **65.8%**

![smote_report](https://user-images.githubusercontent.com/102773052/182994805-e7de5598-691d-4548-a3b4-34de6464742c.png)

**3. Cluster Centroid Undersampling**
- Balanced Accuracy Score: **64.9%**

![centroid_report](https://user-images.githubusercontent.com/102773052/182995124-25e5ac1e-9edf-497a-9c09-00c6fc7523c6.png)

**4. Combination - SMOTE & Edited Nearest Neighbors algorithms (SMOTEENN)**
- Balanced Accuracy Score: **64.9%**

![centroid_report](https://user-images.githubusercontent.com/102773052/182996787-5a218a46-eec2-4077-bff6-7a65151e3575.png)

**5. Machine Learning Model 1: BalancedRandomForestClassifier**
- Balanced Accuracy Score: **68.4%**

![forrest_report](https://user-images.githubusercontent.com/102773052/182996078-18b067c6-634d-4e6d-8629-e237eecaf4c1.png)

**6. Machine Learning Model 2: EasyEnsembleClassifier**
- Balanced Accuracy Score: ??

!! **AttributeError**: 'EasyEnsembleClassifier' object has no attribute 'n_features_in_'

## Summary

Comparing the _Balanced Accuracy Score_ between the the six strategies above is a great way to assess the model performance. _Accuracy_, _Precision_, and _Sensitivity_ are calculated as follows:

#### Accuracy = TP + TN / (TP + TN + FP + FN)
#### Precision = TP / (TP + FP)
#### Sensitivity = TP / (TP + FN)

- TP -> true positive: correctly predicted positive outcomes by model
- FP -> false positive: incorrectly predicted positive outcomes by model
- TN -> true negative: correctly predicted negative outcomes by model
- FN -> false negative: incorrectly predicted negative outcomes by model

### Model Recommendation

It's apparent that the sixth attempted method, Easy Ensemble Classifier, has yet to be completed. If we had to move forward with one of our active methods, it would be the _Balanced Random Forest Classifier_.
 - Highest Balanced Accuracy Score: 68.4%
 - Precision High Risk: 0%
 - Precision Low Risk: 100%
 - Sensitivity (Recall) High Risk: 100%
 - Sensitivity (Recall) Low Risk: 0%
