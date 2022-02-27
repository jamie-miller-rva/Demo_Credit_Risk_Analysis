## Big Picture
* Lending Club investers want to imploy Machine Learning to classify credit risk as "high risk" or "low risk."

* The Ask: Train several machine learning models on the LoanStats_2019Q1 dataset to classify credit risk using the loans_status column as the "target". 

## The Problem Redefined: 
* Conduct Supervised Machine Learning
* to Classifiy loans as either "high risk" or "low risk"
* see [Lending Club Data Dictionary](https://www.kaggle.com/jonchan2003/lending-club-data-dictionary)
* using loan_status as the target variable within the LoanStats_2019Q1 dataset. Note: values in the loan_status column do not contain "high risk" or "low risk" this will need to be inferred from the current list of values.
* this is an imballanced problem (as per the customer) - less than 1% of loans are characterized as "low risk"
* A list of 86 columns (out of the possible 144 columns) in the LoanStats_2019Q1 have been identified (by the customer) to contain information currently used in determining if a loan is "high risk" or "low risk".
* python and the sklearn and imbalanced learn machine learning libraries have been identified as tools to be used in this analysis. 
* The following ML Classification Algorithms will be used in this analysis: 
    <br><br>
    * Logistic regression classifier
    * BalancedRandomForestClassifier
    * EasyEnsembleClassifier <br><br>
    
- Due to the imballanced nature of this problem the customer has requested the following undersampling / oversampling "pre-processing" algorithms be included in the analysis:
    <br><br>
    * RansomOverSampler
    * SMOTE
    * ClusterCentroids
    * SMOTEENN <br><br>
- Module selection will be based on the following:
    <br><br>
    * balanced accuracy score
    * confusion matrix
    * balanced classification report <br><br>

### Deliverables:
* Deliverable 1: Use Resampling Models to Predict Credit Risk
* Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
* Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
* Deliverable 4: A Written Report on the Credit Risk Analysis 

### Findings:
The logistics regression model using the over/under sampling techniques did not generate an acceptable model

The EasyEnsembleClassifier did the best in classifying the loan_status as high_risk with an f1 score of 0.16. While not a great model, it's performanced was the best of those considered.

### Deliverable 1: Use Resampling Models to Predict Credit Risk
* For all three algorithms, the following were completed:
  - An accuracy score for the model was calculated 
  - A confusion matrix was generated 
  - An imbalanced classification report was generated 

**Benchmark - No over/under sampling**
  - An accuracy score for the model was calculated as 0.9951
  - A confusion matrix was generated <br>
    ![Benchmark Confusion Matrix](./Images/Baseline_confusion_matrix.png)

  - An imbalanced classification report was generated <br>
  - Note: The terms (from left to right are) pre is precision, rec is recall, spe is specificity, f1 is f1-score, geo is geometric mean, iba is index balanced accuracy and sup is support.
    ![Benchmark imbalanced classification report](./Images/Baseline_imballanced_classification_report.png)

* **RandomOverSampler**
  - An accuracy score for the model was calculated as 0.8325
  - A confusion matrix was generated <br>
    ![RandomOverSampler Confusion Matrix](./Images/RandomOverSampler_confusion_matrix.png)

  - An imbalanced classification report was generated <br>
    ![RansomOverSampler imbalanced classification report](./Images/RandomOverSampler_imballanced_classification_report.png)
* **SMOTE**
  - An accuracy score for the model was calculated as 0.8325
  - A confusion matrix was generated <br>
    ![SMOTE Confusion Matrix](./Images/SMOTE_confusion_matrix.png)
  - An imbalanced classification report was generated <br>
    ![SMOTE imbalanced classification report](./Images/SMOTE_imballanced_classification_report.png)

* **ClusterCentroids**
  - An accuracy score for the model was calculated as 0.8325
  - A confusion matrix was generated <br>
    ![ClusterCentroids Confusion Matrix](./Images/ClusterCentroids_confusion_matrix.png)
  - An imbalanced classification report was generated <br>
    ![ClusterCentroids imbalanced classification report](./Images/ClusterCentroids_imballanced_classification_report.png)

### Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
* The combinatorial SMOTEENN algorithm had the following:
**SMOTEENN**
  - An accuracy score for the model was calculated 0.8389
  - A confusion matrix was generated <br>
    ![SMOTEENN Confusion Matrix](./Images/SMOTEENN_confusion_matrix.png)
  - An imbalanced classification report was generated <br>
    ![SMOTEENN imbalanced classification repor](./Images/SMOTE_imballanced_classification_report.png)


### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
* The BalancedRandomForestClassifier algorithm does the following:
  - An accuracy score for the model was 0.759
  - A confusion matrix was generated <br>
    ![BalancedRandomForestClassifier Confusion Matrix](./Images/BalancedRandomForestClassifier_confusion_matrix.png)
  - An imbalanced classification report was generated <br>
    ![BalancedRandomForestClassifier imbalanced classification report](./Images/BalancedRandomForestClassifier_imballanced_classification_report.png)
  - The features were sorted in descending order by feature importance <br>
    ![BalancedRandomForestClassifier feature importance](./Images/top_ten_feature_importance_df.png)

* The EasyEnsembleClassifier algorithm does the following:
  - An accuracy score of the model was 0.9319
  - A confusion matrix was generated <br>
    ![EasyEnsembleClassifier Confusion Matrix](./Images/EasyEnsembleClassifier_confusion_matrix.png)
  - An imbalanced classification report was generated <br>
    ![EasyEnsembleClassifier imbalanced classification report](./Images/EasyEnsembleClassifier_imballanced_classification_report.png)


### The ml-project-checklist.md was referenced for this project
[machine learning checklist](https://github.com/ageron/handson-ml/blob/master/ml-project-checklist.md)