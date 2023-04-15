# biostats626
biostats 626 midterm 1 Instruction

## Task 1 (Binary):
Build a binary classifier to classify the activity of each time window into static (0) and dynamic (1). For this task, consider postural transitions as static (0).

### Baseline Algorithm: 
Train test split with a test size of 0.3 is applied to the training data for future evaluation. The baseline model is a random forest classifier with n_estimators=100, max_depth=7. The accuracy of the prediction reaches 0.99914, which is extremely high. It seems that there is limited potential for improvement with this dataset.

### Final Algorithm:
I then tried different supervised approaches including logistic regression, logistic regression with a L1 penalty, SVM with a linear kernel, and XGBoost. I ensembled those methods and random forest in the baseline all together. I trained all those models separately and each of them generated a prediction for the original test data. The final prediction is created as the majority vote of these methods. For instance, if RF gives a prediction of 0, logistic regression gives a prediction of 0, SVM predicts as 1, the final outcome will be 0. 


## Task 2 (Multi-class):
Build a refined multi-class classifier to classify walking (1), walking_upstairs (2), walking_downstairs (3), sitting (4), standing (5), lying (6), and static postural transition (7)

### Baseline Algorithm:
Train test split with a test size of 0.3 is applied to the training data for future evaluation. The baseline model is a logistic regression model, which has an accuracy of 0.9803 when evaluating on the test data from train-test-split.

### Final Algorithm:
I then applied 7 different supervised approaches including logistic regression with a L2 penalty, SVM with a linear and rbf kernel and other parameters after tuning, LDA, random forest with top 300 important features, XGBoost, and KNN. As in the binary task, I ensembled those methods all together. I tuned and trained all of them separately on the 0.7 training data and each generated a prediction for the original test data. The final prediction is created as the majority vote of these methods.



