# Supervised Machine Learning and Credit Risk

## Overview of the Analysis  

For this project, we are helping a peer-to-peer lending company to evaluate machine learning models for their ability to accurately predict credit risk. Based on our findings, the company will leverage the best models to help find good loan candidates with lower default rates. Using a credit dataset from LendingClub, we trained and tested six machine learning algorithms, and have evaluated their results by looking at their accuracy score, confusion matrix, and imbalanced classification report.  

The six models evaluated were:  
- `RandomOverSampler` and `SMOTE` (oversampling), 
- `ClusterCentroids` (undersampling), 
- `SMOTEENN` (combination over- and undersampling), 
- `BalancedRandomForestClassifier` and `EasyEnsembleClassifier` (ensemble classifiers that reduce bias).  

## Results  

Below is a comparison of the six machine learning models, and how well they predicted credit risk in our study:  

- **Oversampling: RandomOverSampler**  
Balanced accuracy score of 0.64, precision for high-risk credit of 0.01, recall for high-risk credit of 0.69, and F1 score for high-risk credit of 0.02.  
![RandomOverSampler](/Screenshots/RandomOverSampler.PNG)  

- **Oversampling: SMOTE**  
Balanced accuracy score of 0.66, precision for high-risk credit of 0.01, recall for high-risk credit of 0.63, and F1 score for high-risk credit of 0.02.  
![SMOTE](/Screenshots/SMOTE.PNG)  

- **Undersampling: ClusterCentroids**  
Balanced accuracy score of 0.54, precision for high-risk credit of 0.01, recall for high-risk credit of 0.69, and F1 score for high-risk credit of 0.01.  
![ClusterCentroids](/Screenshots/ClusterCentroids.PNG)  

- **Combination over/undersampling: SMOTEENN**  
Balanced accuracy score of 0.67, precision for high-risk credit of 0.01, recall for high-risk credit of 0.76, and F1 score for high-risk credit of 0.02.  
![SMOTEENN](/Screenshots/SMOTEENN.PNG)  

- **Ensemble: BalancedRandomForestClassifier**  
Balanced accuracy score of 0.79, precision for high-risk credit of 0.03, recall for high-risk credit of 0.70, and F1 score for high-risk credit of 0.06.  
![RandomForest](/Screenshots/RandomForest.PNG)  

- **Ensemble: EasyEnsembleClassifier**  
Balanced accuracy score of 0.93, precision for high-risk credit of 0.09, recall for high-risk credit of 0.92, and F1 score for high-risk credit of 0.16.  
![EasyEnsemble](/Screenshots/EasyEnsemble.PNG)  

## Summary  

Of the six models assessed in our project, none of the results were particularly impressive, nor did they stand out as being reliable at predicting credit risk. All had low precision scores for high-risk credit, which indicates a large number of false positives and unreliable positive classification. All had modest recall scores for high-risk credit, except for `EasyEnsembleClassifier`. Low recall indicates a high number of false negatives, which is especially detrimental when trying to predict credit risk. The highest accuracy and F1 scores were produced by `EasyEnsembleClassifier`. However, its low F1 score of 0.16 is concerning.  

In summary, the two ensemble classifiers performed better than the other four models, and `EasyEnsembleClassifier` produced the highest scores. However, its low recall score brings down the F1 score to unacceptable levels. For these reasons, we would not recommend any of these six models for predicting credit risk.
