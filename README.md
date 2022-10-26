# Credit_Risk_Analysis

## Overview 
Credit risk is an inherently unbalanced classification problem, with good loans significantly outnumbering risky loans. Unbalanced classes require the use of different techniques to train and evaluate models and this analysis will utilize the ```imbalanced-learn``` and ```scikit-learn``` libraries to build and evaluate models using resampling.

Using the credit card credit dataset from a peer-to-peer lending services company called LendingClub, the data will be oversampled using the ```RandomOverSampler``` and ```SMOTE``` algorithms, then undersampled using the ```ClusterCentroids``` algorithm, and then a combinatorial approach of over- and undersampling will be performed using the ```SMOTEENN``` algorithm. 

Lastly, two new machine learning models that reduce bias, ```BalancedRandomForestClassifier``` and ```EasyEnsembleClassifier```, will be compared and their performance will be evaluated to determine whether they should be used to predict credit risk.

## Resources
### Data Source 
-  [LoanStats_2019Q1](https://github.com/lkachury/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv) csv file

### Software
- Python 3.7.13
- Conda 22.9.0
- Jupyter Notebook

## Results
### Deliverable 1: Use Resampling Models to Predict Credit Risk
Using the ```imbalanced-learn``` and ```scikit-learn``` libraries, three machine learning models will be evaluated by using resampling to determine which is better at predicting credit risk. First, the oversampling ```RandomOverSampler``` and ```SMOTE``` algorithms will be used, and then the undersampling ```ClusterCentroids``` algorithm will be used. Using these algorithms, the dataset will be resampled, the count of the target classes will be viewed, a logistic regression classifier will be trained, the balanced accuracy score will be calculated, a confusion matrix will be generated, and a classification report will be generated. The completed credit_risk_resampling Jupyter Notebook can be referenced [here]().

For all three algorithms, the following have been completed:
1. An accuracy score for the model is calculated:
    - Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144738-cdadc2df-7dec-4dc0-94dd-bb17c55e85e9.png)
    - Undersampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144848-0347f053-58cf-4483-9e71-40088b335f8d.png)
    - Combination: <br /> ![image](https://user-images.githubusercontent.com/108038989/198145077-fdb95642-de96-47c3-bf84-6e46a06e0ee3.png)

2. A confusion matrix has been generated:
    - Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144780-45a1a88f-2b6c-46f6-8534-c6911921b7bf.png)
    - Undersampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144883-84f06d21-e951-42b6-aa67-5db696d15358.png)
    - Combination: <br /> ![image](https://user-images.githubusercontent.com/108038989/198145019-e1d2f632-13c2-4e3c-8921-d6c03a3c3d06.png)
  
3. An imbalanced classification report has been generated:
    - Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144676-fa24c1cb-0ce3-4ae0-abd1-424a52ff76b1.png)
    - Undersampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144923-4884e5ad-c08d-4bdb-8fa6-675f91e8187b.png)
    - Combination: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144975-acbda87c-a55f-4c7d-986e-d024c87ec47a.png)

### Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk
Using the ```imbalanced-learn``` and ```scikit-learn``` libraries, a combinatorial approach of over- and undersampling will be used with the ```SMOTEENN``` algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the ```SMOTEENN``` algorithm, the dataset will be resampled, the count of the target classes will be viewed, a logistic regression classifier will be trained, the balanced accuracy score will be calculated, a confusion matrix will be generated, and a classification report will be generated.

The combinatorial ```SMOTEENN``` algorithm does the following:
1. An accuracy score for the model is calculated:

2. A confusion matrix has been generated: 

3. An imbalanced classification report has been generated:

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Using the ```imblearn.ensemble``` library, two different ensemble classifiers, ```BalancedRandomForestClassifier``` and ```EasyEnsembleClassifier```, will be trained and compared to predict credit risk and evaluate each model. Using both algorithms, the dataset will be resample, the count of the target classes will be viewed, the ensemble classifier will be trained, the balanced accuracy score will be calculated, a confusion matrix will be generate, and a classification report will be generated.

The ```BalancedRandomForestClassifier``` algorithm does the following:
1. An accuracy score for the model is calculated:

2. A confusion matrix has been generated:

3. An imbalanced classification report has been generated: 

4. The features are sorted in descending order by feature importance: 

The ```EasyEnsembleClassifier``` algorithm does the following:
1. An accuracy score of the model is calculated:

2. A confusion matrix has been generated:

3. An imbalanced classification report has been generated: 


## Summary 
The purpose of this analysis was to describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. 

Summarize the results of the machine learning models, 

There is a recommendation on which model to use, or there is no recommendation with a justification.
