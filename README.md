# Loan_ML
An analysis of the relative risk of loans based on a variety of factors using various machine learning models.

## Summary

### Oversampling with Naive Random Oversampling 
#### Precision
- High risk: 0.01
- Low risk: 1.00
- Average: 0.99
#### Recall:
- High risk: 0.66
- Low risk: 0.62
- Average: 0.62
#### Balanced Accuracy: 
0.6175530369078757

### Oversampling with SMOTE
#### Precision
- High risk: 0.01
- Low risk: 1.00
- Average: 0.99
#### Recall:
- High risk: 0.61
- Low risk: 0.69 
- Average: 0.69
#### Balanced Accuracy:
0.6514992150524688

### Undersampling with Cluster Centroid
#### Precision
- High risk: 0.01
- Low risk: 1.00
- Average: 0.99
#### Recall:
- High risk: 0.68
- Low risk: 0.41
- Average: 0.41
#### Balanced Accuracy:
0.5474424371810427

### Combination with SMOTEENN
#### Precision
- High risk: 0.01
- Low risk: 1.00
- Average: 0.99
#### Recall:
- High risk: 0.71
- Low risk: 0.57
- Average: 0.57
#### Balanced Accuracy:
0.6428891047430281

## Analysis and Recommendation
All of the models do a great job of categorizing low-risk loans (as demonstrated by the high "low risk" precision across the board). That's not a huge surprise given the imbalance. Because of that, focusing on which models do the best job of locating high-risk loans is the best for determining the efficacy of the model, and that's done by looking at the Recall (or Sensitivity) of the "High risk" category. That also has the benefit of protecting the company from lending to risky borrowers and potentially losing money.

With that as a target, the combination SMOTEENN model does the best job with a Recall score of .71. It also has a relatively high balanced accuracy as compared to the other models which indicates that we're not sacrificing too much accuracy in the other fields by using a model with a higher sensitivity to high risk loans.
