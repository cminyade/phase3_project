# Phase-3 Project

# SYRIATEL CUSTOMER CHURN PREDICTION

Here is a snappy readme file for this project you're going to love !

**Author**: [Cindy Minyade](https://github.com/cminyade/phase3_project)

## Overview
This project analyzes the data set attached in the `data` folder. It invloves business understanding, data preparation and scaling, modeling and visualization to provide valuable insights for a business stakeholder to prevent customer churn and retain their clients.

## Business and Data Understanding
SyriaTel, a telecommunications company is facing a common issue in the telecom industry i.e; customer churn, when customers stop using the companies services. Churn directly affects revenue, increases cutomer acquisition costs and can damage brand loyalty initiatives.
The `goal` of this project is to help SyriaTel `predict` which customers are likely to churn using the historical data, to enable the company take measures to retain their customers.

## Data
The data [SyriaTel Customer Churn](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset) is from Kaggle, also provided in the Canva project description.
In my analysis, I worked with the following columns `international plan`, `voice mail plan` and dropped these `state`, and `phone number` as they are not likely useful for prediction.

## Modeling

We will build a machine learning model that can predict whether a customer will churn. We will use two models;
- Logistical Regression which is the baseline linear model
- Decision Tree Classifier which is the non-parametic model
Thereafter, we will evaluate the two models and recommend the better one


## Evaluation
Once the models have been trained, we use the results from the test data to see how well the model perfoms. 
The Logistical regression results are as follows:

                 precision    recall  f1-score   support

           0       0.87      0.98      0.92       566
           1       0.60      0.18      0.27       101

    accuracy                           0.86       667
   macro avg       0.73      0.58      0.60       667
weighted avg       0.83      0.86      0.82       667




 The Decision Tree Classifier results as follows:

                precision    recall  f1-score   support

           0       0.95      0.95      0.95       566
           1       0.73      0.73      0.73       101

    accuracy                           0.92       667
   macro avg       0.84      0.84      0.84       667
weighted avg       0.92      0.92      0.92       667

![alt text](image.png)

In the above summary, Decision Tree outperforms Logistic Regression, especially in recall.
Recall tells us how many actual churners we correctly identified, the Decision Tree is a better tool for early intervention. 
- The recall (0.73 vs 0.18), it was able to correctly capture 73% compared to the 18% by Logistic Regression.
- Accuracy is also higher in the Decision Tree model, showing it is the model that performs better.

## Recommendation
For business stakeholders at SyriaTel:

- The recommendation is to use the Decision Tree model to flag high-risk customers (those predicted to churn).
- Prioritize the metric recall to maximize the number of churners caught.
- Implement regular monitoring and retraining as customer behavior or offerings change.
- Apply retention strategies such as discounts, customer service follow-up and promotions to those high-risk customers. 
-Additional data collection such as customer satisfactory surveys understand what to improve to ensure clients are retained.

### Limitations
While the Decision Tree performs better, it can be more prone to overfitting. 

The model still misclassifies 27 actual churners (false negatives), which could mean some customers still leave without being flagged.

The data is historical and may not capture future shifts in the current customer behavior, such as changes in pricing or service policies.

Some of the data features may be correlated (e.g., service usage and contract type), and other features might be outdated or less actionable.

## Conclusion
In this porject, we built a machine learning classifier to predict customer churn for SYriaTel, which the goal of helping the business identify the cliets likely to churn and introduce customer retention measures such as promotions, discounts and ultimately improving customer support efforts. 

After exploring and evaluating the Logistic model and the Decision Tree model, we found that the Decision Tree model outperforms the logistic regression model in the key metric recall. 

We recommend the use of the Decision Tree model to be able to flag potential churners and intervene early. 