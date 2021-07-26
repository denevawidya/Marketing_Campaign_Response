# Increasing Customer’s Acceptance in Marketing Campaign

- Dataset : [Kaggle - Marketing_Campaign](https://www.kaggle.com/rodsaldanha/arketing-campaign)

## Project Background

Due to the Covid-19 pandemic, Guido's Market needs to conduct a marketing campaign to increase sales and customer engagement. In the last campaign, only 15% of customers received the campaign. This results in a difference of $3046 between Cost and Revenue.

To maintain a streak of increasing response rates, Guido's Market was tasked with finding ways to increase the response for the next campaign. To complete this task, the Data Science Guido's Market team created a model that provides recommendations on important criteria to determine which customers will be given the next campaign. The metric that will determine the success of the task assigned to the data science team is the customer response rate to the next campaign.

## Machine Learning Modelling Experiment

From the data owned and the engineering features that have been created, the data science team then creates a model to determine the features that have the most influence on the Response by using Feature Importance. Machine Learning Modeling steps are carried out as follows:

1. Data that has gone through the pre-processing stage is split into test and train sets with a ratio of 70:30 and a random state of 50.
2. After splitting, the data is balanced using the SMOTE, Oversampling, and Undersampling methods.
3. Create a model using the **Decision Tree, Random Forest, XGBoost,** and **AdaBoost** methods for data from each balancing method.
4. Make a model after Hyperparameter Tuning is done for each Machine Learning Modeling that is tried.
5. The results of each modeling contain the values of Accuracy (Test Set), Precision (Test Set), Recall (Test set), F-1 Score (Test Set), AUC, Train Score, and Test Score.
6. Shows Feature Importance score and plot.

### Modelling Results
Before Hyperparameter Tuning

![image](https://user-images.githubusercontent.com/87906938/127013202-642249a6-511f-4481-9c04-f7bea88e0732.png)

After Hyperparameter Tuning

![image](https://user-images.githubusercontent.com/87906938/127013540-b26e10c1-b782-478f-a45d-c40f573ee6f5.png)


## Model Evaluation

To determine the best model, the metric used is AUC because the data used is Balance. The modeling that has the best AUC is AdaBoost before performing Hyperparameter Tuning with an AUC value of 0.75. According to the results of the AUC, 75% of the campaign recipients from the predictions were correct. Looking at the Feature Importance, the four highest Feature Importances from the AdaBoost model are *MntMeatProducts* (16%), *Recency* (10%), *MntWines* (10%), and *NumStorePurchases* (10%). The results of the model and feature importance are quite good and can help to provide business recommendations.

## Business Recommendation

After going through the pre-processing, EDA, and modeling processes, it can be concluded that the best model for marketing campaign data is **AdaBoost** with an AUC of 0.75. From feature importance, it is known that the four highest Feature Importances of the AdaBoost model are *MntMeatProducts, Recency, MntWines,* and *NumStorePurchases*. The modeling results can then be used to predict which customers will respond to the next campaign so that the campaign can be directed to customers who are predicted to receive a response to increase the response rate.

The model that has been created is then used to predict the dataset that has been thoroughly cleansed to be used as a reference for the next marketing campaign. The next marketing campaign strategy is to send the campaign only to those customers that the model predicts will receive the campaign. That way the costs used for marketing campaigns can be reduced compared to sending marketing to all customers. Some additional recommendations that can be given to the business team are to adjust the marketing campaign with Recency and provide promos to customers who shop in-store. To adjust marketing campaigns with Recency, Guido's Market can provide promos to customers who haven't made transactions in Guido's Market for a long time to attract customers. Promos for customers who shop in-store are also recommended because compared to other buying platforms, in-store purchases are the type of shopping platform where customers respond the least to the campaign. In addition, promos for the wine and meat categories can also be given.

In the future, the follow-up that can be done is to improve the model so that the results can be even better. For now, the AUC value of 0.75 is the highest, but ideally the value chosen should be even higher. In addition, a calculation for ROI (Return on Investment) can be made as a basis for making decisions and determining the final result.


# People Behind the Completion of This Project:

This project was carried out to complete the final stage of the [Rakamin Academy Data Science Bootcamp](rakamin.com)

All stages of work are completed by Guido's Team which consists of:
- Abdullah Ilman Fahmi (Chairman)
- Deneva Widyaningtyas (me)
- Dimas Susanto
- Ghaisani Anindya Ayuningtyas
- Naufal Faherza Putra
- Rahmi Ramadhani

And our thanks go to Mr. Ade Irawan as our group mentor who has given a lot of advice and suggestions for this project.
