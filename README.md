# Classifiers
This Jupyter Notebook explores various classifiers and compares their performance.

## Dataset Overview
The dataset represents a Portuguese banking institution's direct marketing campaigns (phone calls). The classification goal is to predict if the client will subscribe to a term deposit.
The dataset contains information from 17 campaigns between May 2008 and November 2010. The phone campaign reached out to 79354 contacts. The dataset includes 6499 successes (8% success rate).
## Findings
1. After cleaning, the ratio of successes was 11%.
2. I started by using linear regression as my baseline.  This model resulted in a low accuracy of 3% for both training and testing.
3. I achieved an 88% accuracy for training and testing using a basic logistic regression.  Training time for the logistic regression was very fast, at 0.03 seconds.
4. Using other classifiers, I did not get a better result.  SVC had the worst training time at 25 seconds.
5. I attempted to improve the performance of the classifiers by adjusting classifier parameters using GridSearchCV.
6. I improved KNN training time and accuracy by a fraction relative to logistic regression. However, the test accuracy did not exceed the basic logistic regression.
7. Improved Decision Trees and Improved SVC achieved the same test accuracy as the basic logistic regression.  Improved decision trees had better training time than the basic logistic regression.

## Feature Importance
Using the number of occurrences of root features from 100 Decision Trees iterations, I found that the most important features are customer age followed by those that own their housing.  I also found many root features with an unknown loan status. This indicates that visibility to loan information may provide better predictions.

## Conclusion
Basic logistic regression performs very well.  After improvement, Decision Trees performed the best in terms of training time, train accuracy and test accuracy.
