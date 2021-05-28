# Simple-Guide-to-Performance-Metrics
A simple guide to use understand how some of the often used performance metrics are calculated in machine learning 

# Project Aim
This project aims to provide a step-by-step manual calculation as to how some of the oftern used performance metrics are calculated, namely
1. Precision
2. Recall
3. F1 Score
4. Support
5. Accuracy
6. F1 Score (Macro Average)
7. F1 Score (Weighted Average)

# Methodology
1. Our data will be the Breast Cancer dataset from Sklearn's datasets where X contains features for each instances and y is their class
2. We will first explore the dataset to see how many are malignant (labelled as 0) and how many are benign (labelled as 1)
3. We will then split our data into 80% training data and 20% testing data to train and test our model respectively
4. We will then initialise a Logistic Regression Model which will be used to aid in our classification
5. We then fit the training data to the classifier and test it on the test data
6. A classification report is printed out and we will attempt to manually calculate most of the components in this classification report
7. We will then plot 2 confusion matrices: (The 1st matrix will be for 1 as positive and the 2nd matrix will be for 0 as positive)
8. Finding the True Negative (TP), False Positive (FP), False Negative (FN) and True Positive (TN) will be from these 2 confusion matrices
9. We will then manually calculate the 7 metrics using their general formulas (found in the section below) and compare it with the in-built function values and the values in the classification report (all 3 should tally)

# General formulas used
1. Precision = TP / (TP + FP)
2. Recall = TP / (TP + FN)
3. F1 Score = 2 * (Precision * Recall) / (Precision + Recall)
4. Support = Number of occurences of each class in y_test (y_true)
5. Accuracy = (TN + TP) / (TP + FP + FN + TN)
6. F1 Score (Macro Average) = (F1 Score of 0 as positive + F1 Score of 1 as positive) / 2
7. F1 Score (Weighted Average) = (Support of 0 as positive * F1 Score of 0 as positive + Support of 1 as positive * F1 Score of 1 as positive) / (Support of 0 as positive + Support of 1 as positive) 

# Conclusion
We have manually calculated most of the metrics of the classification report, only the macro average and weighted average of precision and recall and the total support is not calculated here, but the formulas for the macro average and weighted average of precision and recall is similar to how we calculate the macro average and weighted average of F1 score and the total support can be found by adding the support for both classes.

Other than that, I hope this project is able to help you better understand how each of the metrics are calculated, thank you.
