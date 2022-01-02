# Credit_Risk_Analysis

## Analysis 

There are a varitety of well established machine learning algorithms that are tested and true. Whilst many caviates exist, selecting the right algorithm based on the data available and the desired outcomes takes a bit of time and preperation to optimize the results. Choosing the right data is the beginning, follow closely by a variety of sampling techniques.  

There are many advantages to sampling data, some include:
  - Less information to process by sampling a portion of the data set.
  - Enable the appropriate devision of training and test sets to compensate for a significant variances in feature sample sizes
  - Mitigate anomolies
  - Establishing the importance of features and / or reducing the number of features to increase efficiency

## Overview of the loan prediction risk analysis:

The nature of credit lending, according to LendingClub, is the amount of good loans far outweight the number of bad loans.  This can provide interesting challenges due to the imbalance between outcomes.

Please see the various methods used to determine which algorithms perform better against each other and sampling methods to increase the overall accuracy and sensitivity of the results.

### Naive Random Oversampling

![naive_random_oversampling](https://user-images.githubusercontent.com/31022640/123569463-38deb200-d77b-11eb-8cfe-7475b258f09b.png)

### SMOTE Oversampling

![SMOTE_oversampling](https://user-images.githubusercontent.com/31022640/123569480-3f6d2980-d77b-11eb-923e-3515428790bb.png)

### Undersampling

![undersampling](https://user-images.githubusercontent.com/31022640/123569521-514ecc80-d77b-11eb-8b07-99856d09821b.png)

### Combination Sampling (Over and Under)

![combination_sampling](https://user-images.githubusercontent.com/31022640/123569541-5875da80-d77b-11eb-97a3-681b80deee52.png)

### Balanced Random Forest Classifier

![balanced_random_forest_classifier_setup](https://user-images.githubusercontent.com/31022640/123569561-6a577d80-d77b-11eb-89c5-0550ee4d3d94.png)

![brfc_classification_report](https://user-images.githubusercontent.com/31022640/123577504-ce347300-d788-11eb-83e8-bc948387e2bf.png)

### Easy Ensemble AdaBoost Classifier

![easy_ensemble_adaboost_classifier](https://user-images.githubusercontent.com/31022640/123575406-801e7000-d786-11eb-92c0-8ee2090f8f55.png)

The purpose of this analysis is well defined (4 pt)
Results:

By analyzing and comparing the scores of 4 different we can determine the relative efficacy of individual methods on the same data set.  Based on a variety of metrics we can assertain the accuracy, recall, geometric mean score,

Summary:

  - Naive Random Oversampling - Balanced accurancy score: 1.0
    - Highest balanced accuracy score 
  - SMOTE Oversampling - Balanced accurancy score: 0.6621602612787003
    - Oversampling — Duplicating samples from the minority class in order to balance the dataset
  
  - Undersampling - Balanced accurancy score: 0.5442661782548694
    - Deleting samples from the majority class in order to balance dataset 
    
  - Combination Sampling (Over and Under) - Balanced accurancy score: 0.6621602612787003
    - By using both over and under sampling, increasing the data points for the minority class and 
      increasing the data points for the majority class moderately, improvements in the accuracy can be achieved
      
  - Balanced Random Forest Classifier - Balanced accurancy score: 0.7877672625306695
  
  ![credit_feature_importance_brfc](https://user-images.githubusercontent.com/31022640/123578801-73504b00-d78b-11eb-839c-2bd4e16d3bcf.png)

  - Easy Ensemble AdaBoost Classifier - Balanced accurancy score: 0.925427358175101

  ![image](https://user-images.githubusercontent.com/31022640/123578965-c0342180-d78b-11eb-84f7-6229fafd6e4b.png)

Easy ensemble classifier had promising results with f1, geo and recall clocking in at 97%, 93% and 94% respectively.
