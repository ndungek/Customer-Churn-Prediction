# **SyriaTel Customer Churn Prediction**
### Author : [Maureen Kitang'a](https://github.com/ndungek)

---

> This project is a part of the [Data Science (DSF-FT) Course](https://moringaschool.com/courses/data-science-course/) at [Moringa School](https://moringaschool.com/). The full project description can be found [here](https://github.com/learn-co-curriculum/dsc-phase-3-project-v2-3).


## Overview
Customer churn is a significant challenge for businesses, particularly in the telecom industry. Understanding the factors that contribute to customer churn and being able to predict it can help companies develop strategies to retain customers and reduce revenue losses. This project focuses on analyzing the churn dataset from the telecom industry to predict customer churn and gain insights into the key factors driving churn. 

## Business Understanding
Syriatel, a telecommunications company, is facing a high churn rate, with many customers discontinuing their services and switching to competitors. The company wants to address this issue by developing a customer churn prediction model. By analyzing the dataset, Syriatel aims to gain insights into factors associated with churn, with the goal of reducing churn rate, increasing customer retention, and improving overall profitability.  

## Data Understanding
In this project, we will work with a customer churn dataset from the telecom industry sourced from [Kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset). The dataset contains information about customers, their usage patterns, and whether they have churned or not. 
The dataset contains 3,333 records and spans 21 columns. Of these columns, we identified 4 to be categorical, and 17 as numerical.

## Data Preparation
In this phase, the dataset was cleaned, relevant features were extracted, and appropriate transformations were applied for modeling.
## Modeling
To begin, we point out that the dataset is imbalanced, with only 14.5% of the data being classified as "churn" and the rest being classified as "not churn." 

Our baseline model was LogisticRegression , just to test how our chosen attributes would perform on a basic level. We then explored other more sophisticated models like the RandomForest, Decision trees, and XGBoost. 

## Evaluation
XGBClassifier has the highest recall score, followed by RandomForestClassifier and, LogisticRegression. The DecisionTreeClassifier has the lowest recall score of 0.73. 

The ROC curve analysis shows that the XGBClassifier has the best performance, followed by the RandomForestClassifier, DecisionTreeClassifier, and LogisticRegression. The XGBClassifier has the highest AUC score of 0.884, while the LogisticRegression has the lowest AUC score of 0.79. 

### Model Tuning
We focused on improving the performance of two classification models: RandomForest and XGBoost. After conducting hyperparameter tuning using GridSearchCV, we evaluated the models based on the recall score.

For the RandomForest classifier, we obtained a tuned model that achieved a recall score of 0.76. This indicates its ability to correctly identify positive instances. For the XGBclassifier we got a recall score of 0.79 which was so close to our desired score.

## Conclusion
The recall score of our XGB classifier was 79%. While this is still a good predictive model, we would like to undertake further feature engineering to boost this recall score if we had more time. We achieved our objectives to be able to predict customer churn and had an acceptable recall score. 

### Recommendations
* Offer discounts or promotional offers to customers in area code 415 and 510, as these areas have a higher churn rate. 

* Improve customer service quality and reduce the number of customer service calls.

* Evaluate the pricing structure for day, evening, night, and international charges.

* Focus on customer retention strategies in states with higher churn rates, such as Texas, New Jersey, Maryland, Miami, and New York. 

* Enhance the value proposition of the voicemail plan to increase adoption among customers. 

## Repository Structure

```
├── LICENSE.md                           <- The license for the project                    
|
├── README.md                            <- The top-level README for reviewers of this project
|
├── index.ipynb                          <- Narrative documentation of analysis in Jupyter Notebook
|
├── presentation.pdf                     <- PDF version of project presentation
|
├── write_up.pdf                         <- PDF version of project write up
|
└── telecom.csv                          <- Dataset used in the analysis
     
```
## For More Information

* Please review the full analysis in the [Jupyter Notebook](/index.ipynb) or the [Presentation]
