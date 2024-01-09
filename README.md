# **Credit_card_Default_Prediction**

**AlmaBetter Capstone Project - Classification: Credit card default Prediction**

**This project is a part of the Almabetter Pro Program Curriculum(Full Stack Data Science)**

**Table of Contents**

1. Introduction
2. Dataset
3. Models Used
4. Evaluation Metrics
5. Conclusion and Future Considerations


# **Introduction**

This project aims to predict the likelihood of customer defaulting on their credit card payments in Taiwan. Predicting the estimated probability of default is valuable for risk management purposes, providing insights beyond binary classification.

**Business Objective:**

The goal is to predict the likelihood of customers defaulting on their credit card payments in Taiwan. This prediction is essential for risk management purposes.


# **Models Used**

To achieve our goal, I explored and evaluated several machine learning models:

**Logistic Regression:** A fundamental model for binary classification tasks, providing insights into the probability of credit card defaults.

**Random Forest:** A powerful ensemble model that combines multiple decision trees to make accurate predictions. Random Forest excels in capturing complex patterns in the data.

**Support Vector Machine (SVM):** A model capable of finding the optimal hyperplane to separate data points, often used for binary classification tasks.

**XGBoost Classifier:** A gradient boosting algorithm known for its high predictive accuracy and versatility.



# **Evaluation Metrics**


Model performance was assessed using the following evaluation metrics:

**Recall:** A crucial metric for identifying defaulters, measuring the ability to correctly identify positive cases.
**F1 Score:** A balanced metric considering both precision and recall, providing an overall measure of model performance.
**KS Statistic:** A metric measuring the model's ability to distinguish between positive and negative classes, important for credit risk assessment.

# **Conclusion **

* The main goal of the project was to create a machine learning model that predicts credit card payment defaults for the next month. After performing
data visualization, I identified several important features related to defaulters. During feature engineering, I added a new feature representing
the average bill amount over the past six months and removed individual variables. Additionally, since the data was heavily imbalanced, 
I applied the SMOTE technique to balance the dataset.

* Four models were developed and evaluated: Logistic Regression, Random Forest, SVM, and XGBoost Classifier. The evaluation metrics used were 
recall, f1 score, and KS statistic, focusing on the objective of predicting defaulters rather than simply classifying defaulters and non-defaulters.

* The optimized (tuned) Random Forest Classifier model showed promising results with a recall of 83%, f1 score of 86%, and KS statistic of 74%. 
These results were consistent on both the train and test datasets. However, the tuned XGBoost model exhibited overfitting, while SVM and Logistic
Regression yielded lower scores compared to Random Forest. XGBoost performed well in all evaluation metrics except for recall, where it achieved a 
score of approximately 79%.

* The important features that played a crucial role in prediction were identified as 'LIMIT_BAL', 'AGE', 'PAY_SEPT', 'PAY_AUG', 'PAY_JUL',
 'PAY_JUN', 'PAY_MAY', 'PAY_AMT_SEPT', 'PAY_AMT_AUG', 'PAY_AMT_JUN', 'PAY_AMT_MAY', 'PAY_AMT_APR', 'SEX_Female', 'SEX_Male',
 'EDUCATION_Graduation', 'EDUCATION_High_School', 'EDUCATION_University', 'MARRIAGE_Married', 'MARRIAGE_Single', and 'AVG_BILL_AMT'.

*  It is worth noting that if we had access to additional information such as customer income or annual spending, it could have greatly improved
  our model's ability to estimate whether a customer defaults or not.

*  Based on the evaluation and considering the business objective, the final model chosen is the tuned Random Forest model due to its high recall.
   However, if the business places a higher emphasis on precision and minimizing the misclassification of non-defaulters as defaulters,
   I would recommend the XGBoost model, which demonstrated high precision and f1 score. Given the dataset and features at hand, our model
   performs well on all data points. With such high recall, we can confidently deploy this model for further predictive tasks using future data.
