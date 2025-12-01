# Credit Card Fraud Detection Capstone Project
## Problem Statement 
To predict fraudulent credit card transactions with the help of machine learning models. This is to analyse customer-level data that has been collected and analysed during a research collaboration of Worldline and the Machine Learning Group. The data set is taken from the Kaggle website and has a total of 2,84,807 transactions; out of these, 492 are fraudulent. Since the data set is highly imbalanced, it needs to be handled before model building.

## Understanding and defining fraud 
Credit card fraud is any dishonest act or behaviour to obtain information without proper authorisation from the account holder for financial gain. Among different ways of committing frauds, skimming is the most common one, which is a way of duplicating information that is located on the magnetic strip of the card. Apart from this, the other ways are as follows:

* Manipulation/alteration of genuine cards
* Creation of counterfeit cards
* Stealing/loss of credit cards
* Fraudulent telemarketing
## Project pipeline 
The project pipeline can be briefly summarised in the following five steps:

**Data Understanding**: Here, you need to load the data and understand the features present in it. This would help you choose the features that you will need for your final model.

**Exploratory data analytics (EDA)**: Normally, in this step, you need to perform univariate and bivariate analyses of the data, followed by feature transformations, if necessary. For the current data set, because Gaussian variables are used, you do not need to perform Z-scaling. However, you can check whether there is any skewness in the data and try to mitigate it, as it might cause problems during the model building phase.

**Train/Test split**: Now, you are familiar with the train/test split that you can perform to check the performance of your models with unseen data. Here, for validation, you can use the k-fold cross-validation method. You need to choose an appropriate k value so that the minority class is correctly represented in the test folds.

**Model building / hyperparameter tuning**: This is the final step at which you can try different models and fine-tune their hyperparameters until you get the desired level of performance on the given data set. You should try and check if you get a better model by various sampling techniques.

**Model evaluation**: Evaluate the models using appropriate evaluation metrics. Note that since the data is imbalanced, it is is more important to identify the fraudulent transactions accurately than the non-fraudulent ones. Choose an appropriate evaluation metric that reflects this business goal.

**Input Data**:

https://www.kaggle.com/mlg-ulb/creditcardfraud
## Design flow will be as below 
**Step 1** - Reading & Understanding data
* shape
* info
* describe
* Missing values
  
**Step 2** - EDA
* Bar plot Fraud vs non-fraud share
* Outlier Treatment
* Distribution plot Fraud vs non-fraud share
  * classes with time
  * classes with amount
    
**Step 3** - Data Preperation
* Train Test split
* Feature Scaling
* Checking the Skewness
* Mitigate skweness with PowerTransformer
  
**Step 4** - Building Model  and evaluating Model ( on imbalanced data set )
* Logistic regression
* Decision Tree
* XGBoost
  
**Step 5** - Choosing best model on the imbalanced data

**Step 6** - Handling data imbalance and process each model of Milestone step 7 on each imbalance technique one by one
* Oversampling
* SMOTE (Synthetic Minority Oversampling Technique)
* AdaSyn (Adaptive Synthetic Sampling)
  
**Step 7** - Building and evaluating Model ( on balanced data set )
* Logistic regression
* Decision Tree
* XGBoost
  
**Step 8** - Choosing best model on the balanced data
## Summary
### Strategic Selection of XGBoost Model for Credit Card Fraud Detection
In the pursuit of an effective solution to address credit card fraud detection, our primary objective is to achieve a high recall rate. A high recall is crucial to identifying a significant proportion of actual fraudulent transactions, offering a robust defense mechanism against potential high-value fraudulent activities.

Given the severe consequences that banking institutions face in terms of monetary losses, credibility, and trust due to fraudulent transactions, prioritizing recall becomes a strategic choice to safeguard both the financial well-being of banks and the interests of their customers.

### Model Evaluation and Selection Process
In our analysis, we systematically experimented with various machine learning models, leveraging the power of the SMOTE (Synthetic Minority Oversampling Technique) technique to balance the highly imbalanced dataset. Among the models considered, the XGBoost model emerged as a standout performer. Here are the key findings:

* **ROC Score**: The XGBoost model exhibited a commendable **ROC score of 99%**, showcasing its ability to effectively distinguish between positive and negative classes.

* **Recall Rate**: The standout feature was the exceptionally high **Recall rate of 88%** in the balanced dataset. This metric is crucial in ensuring that a substantial portion of actual fraudulent transactions is correctly identified.

### Rationale for Choosing XGBoost
* Therefore, based on a comprehensive evaluation of performance metrics, the XGBoost model, when coupled with the SMOTE technique on a balanced dataset, emerges as the preferred choice for our credit card fraud detection solution. This strategic decision is grounded in the model's ability to not only deliver an impressive ROC score but, more importantly, to prioritize recall—a critical factor in mitigating the impact of fraudulent transactions on both financial institutions and their clientele.

* By adopting the **XGBoost model within the framework of SMOTE**, we are poised to enhance the proactive monitoring and fraud prevention measures implemented by banks, thereby fortifying their defenses against the evolving landscape of credit card fraud.
