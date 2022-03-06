# Credit_Risk_Analysis
Mod 17


## Purpose
The purpose of this loan prediction risk analysis was to look at current borrower data and try to extrapolate using machine learning the likelihood of predicting future high risk loan borrowers.

## Analysis 
- RandomOverSampler
  This had a 60% accuracy score with excellent precision, but midrange recall of about 60% for predicting low or high risk.  [ROS](../main/naive_oversampling.PNG) 
- SMOTE
  This was a little better with 62% accuracy and a slighty higher recall at about 62% for both low and high risk.  Precision remained high. [SOS](../main/smoteoversampling.PNG)
- ClusterCentroids
  Lowest one so far with 56% accuracy, interestingly the recall and precision results are nearly identical to SMOTE and ROS. [CC](../main/Clustercentroids.PNG) 
- SMOTEENN
  About 61% accuracy, with high precision. This one had a slightly greater disparity in the recall for high and low risk, with high risk showing 57 and low risk 64. Greated variance seen so far. [SMT](../main/smoteen.PNG)
- BalancedRandomForestClassifier
  Accuracy on this showed 100% with precision and recall also showing 100%.  I'm suspicious of these results. [BRF](../main/randomforest.PNG)
- EasyEnsembleClassifier
  Accuracy on this also showed 100% with precision and recall again showing 100%.  I'm suspicious of these results, as well. [EE](../main/EEC.PNG)

## Summary 
The under and oversampling done in the first and second deliverables showed somewhat realistic results with moderate ranges in accuracy and sensitivity.  I did not expect the precision to show 100%. That was disconcerting.  I'm pleased to see the variance in sensitivity for the SMOTEENN. 
## Recommendations 
I would recommend the SMOTEENN model due to the variances shown, however, I don't think any of them are that great at picking out high vs low risk borrowers. BalancedRandomForestClassifier and EasyEnsembleClassifier both had unrealistic data and I would not recommend using my models for those at all.  I think pruning the data given some more might be helpful. There were about 95 columns and pruning to even the top 20 would give both, a more manageable and more relevant data set.
