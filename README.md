# Chicago-Food-Inspection
# Chicago_Food_Inspections_
## Problem Overview
> 1. Interest in food made me to analyse the data related to food.
> 2. This data is from the Chicago Data Portal. It is an analysis of food inspection in Chicago in various food outlets.
> 3. The project's goal is to analyze Chicago restaurants and determine if the Results are pass, pass with conditions, or fail based on the inspection type and Violations.

## Data Description
> 1. Chicago Food Inspection dataset contains information of the Inspection of Food related Companies like Restaurants, Grocery Stores, etc,. in Chicago from January 2010 to present (April 2022).
> 2. It Consists of 234319 rows and 17 columns.
> 3. Data: https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF
> 4. Dataset: https://data.cityofchicago.org/Health-Human-Services/Food-Inspections/4ijn-s7e5/data

## Exploratory Data Analysis
> 1. Majority of the data or almost all the data is from Chicago and IL. Therefore, there won't be any useful information from State and City columns.
> 2. There is already DBA Name. Therefore, there is no need of AKA Name which also contain some null values.
> 3. More than 50per of the data is Canvass Inspection type. 
> 4. Majority of them are Restaurants.
> 5. Large amount of data is with High Risk category and at the same time it has high Pass result.

## Feauture Selection
> 1. From the exploratory data analysis, the majority of the data is ‘Pass’ when the risk is high or at "Risk (High)". So, it could be the feature. After modeling, I found out that it is not useful to predict the Fail cases.
> 2. Therefore, the other feature that gives a better prediction is ‘Violations’. 
> 3. The target column is ‘Results’ (‘Pass’, ‘Fail’, ‘Pass w/ conditions’).

## Model Evaluation
> 1. Split the data into training and test data which is in 3:2.
> 2. Logistic regression, decision tree classifier, Random Forest Classifier, and hyper-parameters tuning of these models is done.
> 3. One vs one (macro and weighted by prevalence) and one vs rest (macro and weighted by prevalence) are done.

## Findings
> 1. ‘Violations’ is the feature column.
> 2. Using this data after hyper parameters tuning, the Random forest classifier has the highest accuracy of 87%, followed by a decision tree classifier of 86% and logistic regression of 60%.
> 3. Test score prediction score is 87% and train score prediction is 99%.
> 4. After one vs one and one vs rest, the accuracy or AUC ROC score is 93% and 94% respectively (macro).
> 5. After one vs one and one vs rest, the accuracy or AUC ROC score is 94% and 95% respectively (weighted by prevalence).

## Challenges
> 1. Selection of feature column.
> 2. Dealing with the columns because most of the columns are categorical columns.
> 3. Modelling, finding the best model to improve the accuracy of the prediction.

## Conclusion
> 1. Using the final model (one vs rest, weighted by the prevalence (in this case)), inspectors can easily predict that there will be a decrease in the chances of visiting each location for inspection. 
> 2. Even the owners of the restaurants or the food stores can predict the result and can take safety measures to avoid failing in the inspection. 
> 3. Therefore, this model helps in the detection of inspection results and improves the quality of food.

