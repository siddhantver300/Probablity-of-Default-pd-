# Probablity-of-Default-pd-
## 📊 Probability of Default (PD) Model

The Probability of Default (PD) model was developed to estimate the likelihood that a borrower will default on a loan. The target variable used for this model is `loan_status`, where a value of 1 indicates default and 0 indicates non-default. Given the binary nature of the outcome, a logistic regression model was implemented as a baseline approach for classification.

The dataset was first preprocessed by handling missing values, removing unrealistic observations (such as extreme ages and employment lengths), and converting categorical variables into factor format. The cleaned dataset was then split into training (70%) and testing (30%) subsets to evaluate model performance on unseen data.

The logistic regression model was trained using a combination of borrower-specific and loan-specific features, including income, employment length, loan amount, interest rate, loan-to-income ratio, credit history length, home ownership status, loan intent, and loan grade. These variables were selected based on their economic relevance and potential influence on credit risk.

Model performance was evaluated using multiple metrics. The model achieved an Area Under the ROC Curve (AUC) of 0.86, indicating strong discriminatory power in distinguishing between defaulters and non-defaulters. Initially, using a default classification threshold of 0.5 resulted in high overall accuracy but relatively poor detection of defaulters.

To improve risk detection, the classification threshold was reduced, leading to a significant increase in the model’s ability to correctly identify defaulters (specificity improved to approximately 71%). Although this adjustment resulted in a slight decrease in overall accuracy, it produced a more balanced and risk-sensitive model. This reflects a realistic credit risk strategy, where identifying potentially risky borrowers is more critical than maximizing overall accuracy.

The results highlight the trade-off between sensitivity and specificity in classification models. Lowering the threshold increases the detection of high-risk borrowers at the expense of more false positives, aligning the model with conservative lending practices commonly used in financial institutions.

Overall, the PD model demonstrates strong predictive capability and provides meaningful insights into the factors influencing default risk, making it a robust foundation for credit risk assessment.


####OUTPUT####
1.
Confusion Matrix and Statistics

          Reference
Prediction    0    1
         0 6627  579
         1  853 1444
                                         
               Accuracy : 0.8493         
                 95% CI : (0.842, 0.8564)
    No Information Rate : 0.7871         
    P-Value [Acc > NIR] : < 2.2e-16      
                                         
                  Kappa : 0.5715         
                                         
 Mcnemar's Test P-Value : 5.423e-13      
                                         
            Sensitivity : 0.8860         
            Specificity : 0.7138         
         Pos Pred Value : 0.9197         
         Neg Pred Value : 0.6286         
             Prevalence : 0.7871         
         Detection Rate : 0.6974         
   Detection Prevalence : 0.7583         
      Balanced Accuracy : 0.7999         
                                         
       'Positive' Class : 0              





2.  Area under the curve: 0.8694
# Roc curve is uploaded in repository
