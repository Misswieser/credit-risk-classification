# credit-risk-classification

This is a supervised learning challenge. 

The purpose is to implement machine learning model to develop credit risk classification analysis, in this challenge logistic regression model is used. The model is used to predict loan defaults on the basis of the financial information from lending_data.csv. The model uses the financial information to classify loans as either healthy or high-risk in order provide insight and assist in the decision making of loan approval.  

The stages of the machine learning process to get the analysis is as follows:
  * Data prepartion: Loading lending_data into Panda dataframe then splitting the data into training and testing sets.
  * Model building:  
      1. Original data: creating logistic regression model with the prepared original data. The model is trained and fitted, to finally evaluate the model's performance in accuracy score, confusion matrix and classification report.
      2. Resampling data: RandomOverSample from the imbalanced-learn libray is used to address imbalance in the dataset, and instantiate and fit the RandomOverSampler model, then logistic regression model is implemented to train the resampled data and evaluated. 
        
The methods used was Logistic Regression and RandomOverSampler.

# Original Logistic Regression Model

  # Result:
    * Accuracy Score: 0.9521352751368186
    * Classification Report:
        * Precision Score:
              * '0' (healthy loans): 1.00
              * '1' (high-risk loans): 0.86
          * Recall Score:
              * '0' (healthy loans): 1.00
              * '1' (high-risk loans): 0.91

  # Summary:
The logical regression model accuracy score is 0.95, this shows that this model has high predictability on both healthy loans and high-risk loans on overall accuracy. 

The confusion model predicts both the `0` (healthy loan) and `1` (high-risk loan) labels with a relatively low number of false positives and false negatives. 
The results of confusion matrix indicates that the healthy loans ('0') label, has predicted true prositives are 14,926 healthy loans, and the incorrectly predicted false negatives are 75 high-risk loans as healthy loans. 
The results for the high-risk loans ('1') label, indicted the predicted true positives are 461 for high risk loans, and the incorrectly predicted false negatives are 46 healthy loans as high-risk loans.
The confusion matrix of the original logistic regression model, indicates a low number of false positives of 46 healthy loans is identified as high-risk loans, and the matrix indicates the false negatives of 75 high-risk loans as healthy loans. 

Additionally, the classification report provides detailed insights into the logistic regression model's performance for each '0' (healthy loan) and '1' (high-risk loan) labels. The report includes metrics such as precision, recall, f1-score, and support for each label, along with acuracy of macro and weighted averages.


# Logistic Regression with Resample model:

  # Result:
    * Accuracy Score: 0.9941749445500477
    * Classification Report (Resampled):
          * Precision Score:
              * '0' (healthy loans): 1.00
              * '1' (high-risk loans): 0.85
          * Recall Score:
              * '0' (healthy loans): 0.99
              * '1' (high-risk loans): 0.99

  # Summary
The  logistic regression model with resampled accuracy score is 0.99, this shows that this model has an excellent predictability on both healthy loans and high-risk loans on overall accuracy, this is 0.04 more compared to the original logistic regression model. 

The results of confusion matrix shows that the healthy loans ('0') label, has predicted true prositives are 14,915 healthy loans, and the incorrectly predicted false negatives are 86 high-risk loans as healthy loans. 
The results for the high-risk loans ('1') label, indicates the predicted true positives are 504 for high risk loans, and the incorrectly predicted false negatives are 3 healthy loans as high-risk loans.

The confusion matrix of the logistic regression model with resampled data demonstrates a significantly lower number of false positives compared to the original model. Specifically, the resampled model identifies only 3 healthy loans as high-risk loans, whereas the original model incorrectly identifies 46 healthy loans as high-risk loans. This indicates that the model with resampled data effectively reduces the occurrence of false positives.
On the other hand, the logistic regression model with resampled data shows an increase in false negatives compared to the original model. The resampled model identifies 86 high-risk loans as healthy loans, whereas the original model incorrectly identifies 75 high-risk loans as healthy loans. This suggests that the model with resampled data has a higher tendency to misclassify high-risk loans as healthy loans compared to the original model.

The classification report of logistic regression with resample model has a stronger perdictive performance after oversampling the data than the original model's classification report.

# Recommendation

Logistic Regression with Resampled data performs better than the Original Logistic Regression Model in terms of accuracy, confusion matrix, and on classification report: precision, and recall. Hence, the performance model of the Logistic Regression with Resampled Data in predicting loan status is superior in providing insight and assisance in the decision making of loan approval. 
    
