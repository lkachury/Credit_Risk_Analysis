# Credit_Risk_Analysis

## Overview 
Credit risk is an inherently unbalanced classification problem, with good loans significantly outnumbering risky loans. Unbalanced classes require the use of different techniques to train and evaluate models and this analysis will utilize the ```imbalanced-learn``` and ```scikit-learn``` libraries to build and evaluate models using resampling.

Using the credit card credit dataset from a peer-to-peer lending services company called LendingClub, the data will be oversampled using the ```RandomOverSampler``` and ```SMOTE``` algorithms, then undersampled using the ```ClusterCentroids``` algorithm, and then a combinatorial approach of over- and undersampling will be performed using the ```SMOTEENN``` algorithm. 

Lastly, two new machine learning models that reduce bias, ```BalancedRandomForestClassifier``` and ```EasyEnsembleClassifier```, will be compared and their performance will be evaluated to determine whether they should be used to predict credit risk.

## Resources
### Software
- Python 3.7.13
- Conda 22.9.0
- Jupyter Notebook

### Data Source 
-  [LoanStats_2019Q1](https://github.com/lkachury/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv) csv file
-  Confusion Matrix: <br /> ![image](https://user-images.githubusercontent.com/108038989/198169556-66c1f869-b852-4fb9-9193-3bd30971643f.png)

## Results
### Deliverable 1: Use Resampling Models to Predict Credit Risk
Using the ```imbalanced-learn``` and ```scikit-learn``` libraries, three machine learning models will be evaluated by using resampling to determine which is better at predicting credit risk. First, the oversampling ```RandomOverSampler``` and ```SMOTE``` algorithms will be used, and then the undersampling ```ClusterCentroids``` algorithm will be used. Using these algorithms, the dataset will be resampled, the count of the target classes will be viewed, a logistic regression classifier will be trained, the balanced accuracy score will be calculated, a confusion matrix will be generated, and a classification report will be generated. The completed credit_risk_resampling Jupyter Notebook can be referenced [here](https://github.com/lkachury/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb).

For all three algorithms, the following have been completed:
1. An accuracy score for the model was calculated:
    - Naive Random Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144738-cdadc2df-7dec-4dc0-94dd-bb17c55e85e9.png)
    - SMOTE Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198149934-8fc2ee32-7e29-4d93-bcb7-1569ee288f19.png)
    - Undersampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144848-0347f053-58cf-4483-9e71-40088b335f8d.png)

2. A confusion matrix has been generated:
    - Naive Random Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144780-45a1a88f-2b6c-46f6-8534-c6911921b7bf.png)
    - SMOTE Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198149972-397e56ea-116c-45e4-bd42-5e3377900d19.png)
    - Undersampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144883-84f06d21-e951-42b6-aa67-5db696d15358.png)
  
3. An imbalanced classification report has been generated:
    - Naive Random Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144676-fa24c1cb-0ce3-4ae0-abd1-424a52ff76b1.png)
    - SMOTE Oversampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198150034-53b51905-8090-44e6-8f1c-3c327810620f.png)
    - Undersampling: <br /> ![image](https://user-images.githubusercontent.com/108038989/198144923-4884e5ad-c08d-4bdb-8fa6-675f91e8187b.png)

### Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk
Using the ```imbalanced-learn``` and ```scikit-learn``` libraries, a combinatorial approach of over- and undersampling will be used with the ```SMOTEENN``` algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the ```SMOTEENN``` algorithm, the dataset will be resampled, the count of the target classes will be viewed, a logistic regression classifier will be trained, the balanced accuracy score will be calculated, a confusion matrix will be generated, and a classification report will be generated. The completed credit_risk_resampling Jupyter Notebook can be referenced [here](https://github.com/lkachury/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb).

The combinatorial ```SMOTEENN``` algorithm does the following:
1. An accuracy score for the model was calculated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198145077-fdb95642-de96-47c3-bf84-6e46a06e0ee3.png)

2. A confusion matrix has been generated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198145019-e1d2f632-13c2-4e3c-8921-d6c03a3c3d06.png)

3. An imbalanced classification report has been generated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198144975-acbda87c-a55f-4c7d-986e-d024c87ec47a.png)

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Using the ```imblearn.ensemble``` library, two different ensemble classifiers, ```BalancedRandomForestClassifier``` and ```EasyEnsembleClassifier```, will be trained and compared to predict credit risk and evaluate each model. Using both algorithms, the dataset will be resample, the count of the target classes will be viewed, the ensemble classifier will be trained, the balanced accuracy score will be calculated, a confusion matrix will be generate, and a classification report will be generated. The completed credit_risk_ensemble Jupyter Notebook can be referenced [here](https://github.com/lkachury/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb).

The ```BalancedRandomForestClassifier``` algorithm does the following:
1. An accuracy score for the model was calculated:
<br /> ![image](https://user-images.githubusercontent.com/108038989/198165983-26ef4258-0eaf-4c66-b576-8bf0b2b91999.png)

2. A confusion matrix has been generated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198166025-54797e2c-08d5-4c68-9813-e1fac5354374.png)

3. An imbalanced classification report has been generated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198166049-e30e99a4-5272-4003-9e6b-7e9ae8fc6099.png)

4. The features are sorted in descending order by feature importance: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198166166-d0ff6145-0fbc-4a07-8db8-0fe6f5a3ccfa.png)

The ```EasyEnsembleClassifier``` algorithm does the following:
1. An accuracy score of the model is calculated:
<br /> ![image](https://user-images.githubusercontent.com/108038989/198166215-34dd77a5-ab44-4b4d-aa70-57c3b245eb0f.png)

2. A confusion matrix has been generated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198166256-570175a3-5db7-418f-a7f4-6a0f91a3bd11.png)

3. An imbalanced classification report has been generated: 
<br /> ![image](https://user-images.githubusercontent.com/108038989/198166291-a2e81057-c830-4bd2-97d8-9fbc7cb73daf.png)

## Summary 
The purpose of this analysis was to describe the balanced accuracy, precision, and recall scores for all six machine learning models in order to determine whether they should be used to predict credit risk. 

Accuracy is based on the number of correct predictions as a percentage of the number of observations in the dataset. Accuracy scores range from 0% to 100%, where 100% is a perfect score and 0% is the worst. The accuracy for RandomOversampler=65%, SMOTE=65%, ClusterCentroids=52%, SMOTEENN=65%, BalancedRandomForestClassifier=79%, and EasyEnsembleClassifier=93%. 

Precision is a measure how reliable the model is at identifying the positive cases from the total predicted cases. It is a percentage of the number of true positives (TP) divided by the number of all positives (i.e., the sum of true positives and false positives, or TP + FP). A low precision score is a result of many false positives, thus the model which produces zero False Positives has a precision of 100%. The precision for RandomOversampler, SMOTE, ClusterCentroids, and SMOTEENN were all 1% for high-risk loans and 100% for low-risk loans, BalancedRandomForestClassifier=3% for high-risk loans and 100% for low-risk loans, and EasyEnsembleClassifier=9% for high-risk loans and 100% for low-risk loans. 

Recall is a measure of how sensitive the model is at identifying how many total positive cases were predicted correctly. It is a percentage of the number of true positives (TP) divided by the sum of true positives (TP) and false negatives (FN). A low recall score is a result of many false negatives, thus the model which produces zero False Negatives has a recall of 100%. The recal for RandomOversampler=61% for high-risk loans and 69% for low-risk loans, SMOTE=63% for high-risk loans and 66% for low-risk loans, ClusterCentroids=60% for high-risk loans and 43% for low-risk loans, SMOTEENN=68% for high-risk loans and 61% for low-risk loans, BalancedRandomForestClassifier=70% for high-risk loans and 87% for low-risk loans, and EasyEnsembleClassifier=92% for high-risk loans and 94% for low-risk loans. 

The F1 score is a harmonic mean and it is a single summary statistic of precision and recall. F1 scores range from 0% to 100%, where 100% is a perfect score and 0% is a model that failed completely. The F1 score for RandomOversampler=2% for high-risk loans and 82% for low-risk loans, SMOTE=2% for high-risk loans and 79% for low-risk loans, ClusterCentroids=1% for high-risk loans and 60% for low-risk loans, SMOTEENN=2% for high-risk loans and 76% for low-risk loans, BalancedRandomForestClassifier=6% for high-risk loans and 93% for low-risk loans, and EasyEnsembleClassifier=16% for high-risk loans and 97% for low-risk loans. 

Based on the summary above, the two Ensemble Classifiers performed better than the four Resampling Models. The EasyEnsembleClassifier was the better performing machine learning model based on its accuracy, precision, and recall scores and this is the recommended model that should be used to predict credit risk.
