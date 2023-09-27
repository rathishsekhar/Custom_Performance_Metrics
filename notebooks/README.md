# CountVectorizer.ipynb README

# Table of Contents
1. Overview
2. Performance metrics used
3. Code acttivity

# Overview
 Performance metrics in machine learning measure the performance of a machine learning model. Given a machine learning tasks these metrics how close is the model predicting  or how close is the intended task acheived. In this code, we will see how performance metrics can be implemented as a code outside 'sklearn.metrics' module. We will run the metrics with various kinds of datasets to see how well the metrics measure and what data nuances bring about with the metrics. 

In the notebook, we will also try to estimate the threshold i.e. value of the probability score to be considered below which the proba score will be marked as belonging to 0, else marked as 1 for an arbitrary condition. This would familiarize us with the threshold determination calculations which are usually done using 'sklearn.metrics' modules. 

# Performance metrics used
1. Confusion matrix: is a tabular represenation of a classification model's performance. More typically in our case we will be using a binary classification confusion matrix. 

      True Positive (TP): Correctly predicted positive instances. \
      False Positive (FP): Incorrectly predicted positive instances (actual was negative). \
      False Negative (FN): Incorrectly predicted negative instances (actual was positive). \
      True Negative (TN): Correctly predicted negative instances. 



2. Accuracy: Accuracy measures the ratio of correctly predicted instances to the total number of instances in the dataset. Accuracy fails with imbalanced datasets.
3. Precision: Precision is the ratio of correctly predicted positive instances to the total predicted positive instances. It focuses on the accuracy of positive predictions. High precision indicates that the model has fewer false positives.
4. Recall (Sensitivity or True Positive Rate): Recall measures the ratio of correctly predicted positive instances to the total actual positive instances. It focuses on the ability to capture all positive instances. High recall indicates that the model has fewer false negatives.
5. F1 Score: The F1 score is the harmonic mean of precision and recall. It balances precision and recall and is particularly useful when you want to strike a balance between false positives and false negatives.
6. ROC Curve and AUC (Area Under the Curve): ROC (Receiver Operating Characteristic) curve is used to assess a model's ability to distinguish between classes. AUC measures the area under the ROC curve and provides a single value to summarize the model's performance. Higher AUC indicates better model performance.
7. R-squared (R2): R-squared measures the proportion of the variance in the dependent variable that is explained by the independent variables in a regression model. It ranges from 0 to 1, with higher values indicating a better fit.
8. Mean Squared Error (MSE): MSE is another regression metric that calculates the average squared difference between predicted and actual values. Squaring penalizes larger errors.




While we have provided the basic definitions, more details could be found at https://neptune.ai/blog/performance-metrics-in-machine-learning-complete-guide

# Code Activity
### What did we implement in the code for each dataset?

1. Dataset a: 
   1. Assuming the prediction threshold at 0.5 i.e. if 'y' < 0.5, we assume it is 0 else it is 1, we converted the 'proba' column to predicted labels. 
   2. We computed confusion matrix and then the Accuracy score, F1 score and AUC score to see how this data fares amongst these different metrics

2. Dataset b: Gather predicted labels similar to operations on the dataset a and then compute all the above mentioned metrics to see the contrast of results. 
3. Dataset c: Unlike the previous two datasets, we tried to predict the optimum threshold i.e. 'proba' value to be considered, so as to yield highest AUC value. To make things interesting we try to obtain the threshold value so as to have the minimum error obtainied from teh value 500*FP + 100*FN minimum. The minimum error is selected for demonstration purposes only. Usually setting the threshold values is a domain specific problem. 
4. Dataset d: This data is equivalent to a regression dataset and therefore, R-squared error, Mean squared error and mean absolute percentage errors are calculated. 


