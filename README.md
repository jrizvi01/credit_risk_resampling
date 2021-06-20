# credit_risk_resampling

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  * The purpose of the analysis is to use various techniques to train and evaluate models with imbalanced classes and to build a model that can identify the creditworthiness of borrowers.
* Explain what financial information the data was on, and what you needed to predict.
  * We needed to predict a risk profile for the loans based on the following criteria:
    * Loan size
    * Interest Rate
    * Borrower's Income
    * Debt-to-income Ratio
    * Number of Accounts
    * Derogatory Marks
    * Total Debt
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
   * By using a logistic regression model to compare two versions of the dataset, we found that a bias exists between the healthy loan to the high risk loan. The value count was        75036 vs. 2500.
* Describe the stages of the machine learning process you went through as part of this analysis.
   * We went through the following stages of the ML process as part of this analysis:
      * Splitting the Data into Training and Testing Sets
      * Created a Logistic Regression Model with the Original Data
      * Predicted a Logistic Regression Model with Resampled Training Data
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
  * We used the following method:
      * Splitting the Data into Training and Testing Sets
      * Created a Logistic Regression Model with the Original Data
      * Evaluated model’s performance by doing the following:
          * Calculated the accuracy score of the model.
          * Generated a confusion matrix.
      * We then created a new model that used resampled data for better results and repeated the above steps

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Balanced accuracy score: 95.28%
  * Precision score:
      * Healthy Loans - 100%
      * High Risk Loans - 85%
  * Recall score: 91%
        * Healthy Loans - 99%
        * High Risk Loans - 91%

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Balanced accuracy score: 99.36%
  * Precision score:
      * Healthy Loans - 100%
      * High Risk Loans - 84%
  * Recall score: 91%
        * Healthy Loans - 99%
        * High Risk Loans - 99%
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
  * The oversampled model seems to perform better because it has a higher recall ratio. Recall is the ratio of correctly predicted positive observations to the all observations in actual class - yes.


![image](https://user-images.githubusercontent.com/80922524/122681490-62ab3e00-d1a9-11eb-91ab-06ba46f30dba.png)

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  * Yes, it is more important to predict the '1's as they are the high risk loans.
  
If you do not recommend any of the models, please justify your reasoning.
  * I would recommend the oversampled model (Model 2) as it performed better in the overall score including the recall ratio and we know that recall ratio correctly predicts the positive observation which would be important in making the decision.
