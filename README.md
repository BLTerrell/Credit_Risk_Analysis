# Credit Risk Analysis

## Overview of Project

### Purpose

Our objective is to employ different Machine Learning techniques to evaluate credit card risk, while focusing on the unbalanced nature of good loans far outnumbering risky loans.

### Resources
- Data: [2019 Q1 Loan Stats](Module-17-Challenge-Resources/LoanStats_2019Q1.csv)
- Software: Python, pandas, numpy, skikit-learn, imbalanced-learn, VS Code

## Project Results

### Over Sampling
#### RandomOverSampler
<img src='Module-17-Challenge-Resources/images/random_over_sample_report.png'>

- <strong>Accuracy score:</strong> 0.6742
- <strong>True positives:</strong> 75, <strong>false postives:</strong> 6740, <strong>false negatives:</strong> 26, <strong>true negatives:</strong> 10364
- <strong>Precision:</strong> 0.99, <strong>recall:</strong> 0.61, <strong>f1 score:</strong> 0.75

#### SMOTE
<img src='Module-17-Challenge-Resources/images/smote_report.png'>

- <strong>Accuracy score:</strong> 0.6623
- <strong>True positives:</strong> 64, <strong>false postives:</strong> 5285, <strong>false negatives:</strong> 37, <strong>true negatives:</strong> 11819
- <strong>Precision:</strong> 0.99, <strong>recall:</strong> 0.69, <strong>f1 score:</strong> 0.81

### Under Sampling
#### ClusterCentroids
<img src='Module-17-Challenge-Resources/images/cluster_centroid_report.png'>

- <strong>Accuracy score:</strong> 0.5443
- <strong>True positives:</strong> 70, <strong>false postives:</strong> 10340, <strong>false negatives:</strong> 31, <strong>true negatives:</strong> 6764
- <strong>Precision:</strong> 0.99, <strong>recall:</strong> 0.40, <strong>f1 score:</strong> 0.56

### Combinatorial Sampling
#### SMOTEENN
<img src='Module-17-Challenge-Resources/images/smoteenn_report.png'>

- <strong>Accuracy score:</strong> 0.6434
- <strong>True positives:</strong> 72, <strong>false postives:</strong> 7288, <strong>false negatives:</strong> 29, <strong>true negatives:</strong> 9816
- <strong>Precision:</strong> 0.99, <strong>recall:</strong> 0.57, <strong>f1 score:</strong> 0.72

### Ensemble Classifiers
#### BalancedRandomForestClassifier
<img src='Module-17-Challenge-Resources/images/random_forest_report.png'>

- <strong>Accuracy score:</strong> 0.7475
- <strong>True positives:</strong> 152, <strong>false postives:</strong> 6315, <strong>false negatives:</strong> 94, <strong>true negatives:</strong> 45051
- <strong>Precision:</strong> 0.99, <strong>recall:</strong> 0.88, <strong>f1 score:</strong> 0.93

#### EasyEnsembleClassifier
<img src='Module-17-Challenge-Resources/images/easy_ensemble_report.png'>

- <strong>Accuracy score:</strong> 0.8229
- <strong>True positives:</strong> 186, <strong>false postives:</strong> 5662, <strong>false negatives:</strong> 60, <strong>true negatives:</strong> 45704
- <strong>Precision:</strong> 0.99, <strong>recall:</strong> 0.89, <strong>f1 score:</strong> 0.94

## Summary

### Conclusion

From all our models we can see that they all have accuracy scores greater than 50%. This means that they will make the correct prediction more than half the time. The highest accuracy scores belong to our two Ensemble Classifier models which had accuracies of 75% (`BalancedRandomForestClassifier`) and 83% (`EasyEnsembleClassifier`). 
<strong>Precision</strong> is a measure of how reliable a positive classification is. For our loaner this would be how reliable our risky designation is. A low precision is okay because it means that we are over-flagging loans as risky.
<strong>Recall</strong> is a measure of how many truly risky loans were properly flagged. Based on these definitions I would recommend the model with the highest recall value and that is the `EasyEnsembleClassifier`. Not only does it have the highest recall value associated with flagging risky loans it also has the highest overall accuracy, overall precision, overall recall, and overall f1 score.