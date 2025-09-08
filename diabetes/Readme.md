### **Initial Report and Exploratory Data Analysis (EDA)** 

This notebook presents my initial exploratory data analysis on a dataset for predicting diabetes that I obtained from Kaggle. For this analysis I used the 'diabetes_binary_health_indicators_BRFSS2015.csv' file from the 'Diabetes Health Indicators Dataset' createdd by Alex Teboul.  

# **Business understanding**

The business goal is to find a model that can predict the risk of diabetes from the survey data. If so, which of the factors in the dataset can explain the risk of diabetes? I will do EDA to understand the data and build initial baseline models with different ML classifiers (e.g. logistic regression,RandomForest) to find the best one for this task.

# **Data Understanding**

In this section I explored the Diabetes Health Indicators Dataset dataset to understand the following aspects:

* **Data types:** how many variables are there? What data types? Are there only numeric variables or also categorigal ones?  
* **data quality:** How many missing values are there? How many variables have a single value for all rows?
*  **Correlations:** Which variables are correlated with each other or with price?
* **Data distributions:** What is the distribution of the variables? Which of them are skewed?
* **Outliers:** Are there aany outliers in the dataset? If so, how do we handle them?

1. The dataset has class imabalance: only 13.9% of respondents had diabetes.

2. The data is skewed left for cholesterol check: majority of respondents have checked their cholesterol in the last 5 years. 

3. The BMI variable is also heavily skewed right: majority of respondednts had BMI below 60

4. The Stroke variable is also heavily skewed right: majority of respondednts had no stroke

5. The BMI variable is also has serious outliers, as a number of respondents had very high BMI above the IQR.

6. The HeartDiseaseorAttack variable is also heavily skewed right: majority of respondednts had no previous heart disease or heart attack

7. In contrast the PhysActivity is skewed left: the majority of respondents had physical acitvity

8. The HvyAlcoholConsump variable is skewed right: majority of respondents reported not having high alcohol consumption

9. Majority of respondents reported having health coverage and having access to a Doctor

10. The MentHlth variable is skewed right as majority of respondents reported having under 5 days of poor mental health in last 30 days. The same is true of the physical health variable, PhysHlth

11. There is a moderaetly high correlation between some of the variables e.g. between GenHlth vs PhysHlth, GenHlth vs DiffWalk, PhysHlth vs DiddWalk 


# Baseline classifiier models

The following classifier models were built with the cleansed dataset:
1. Logistic Regression and
2. Random Forest


Of the two benchmark models, the RandomForest was the best with the highest AUC and F1 score.  I ignore accuracy due to class imbalance. The below table summarizes the performance of these models:
              **Model F1 Score   Precision Recall    AUC       Accuracy
        Random Forest 0.223248   0.580432  0.138202  0.826458  0.867372
  Logistic Regression 0.252747   0.546838  0.164356  0.826404  0.865973


# Most important drivers of response

The best RandomForest model I built shows the 4 most important drivers of response are BMI, GenHlth, HighBP and HighCol.  Here's the list of variables ranked by their importance: 

                  **Importance
BMI                     0.005984
GenHlth                 0.004198
HighBP                  0.002523
HighChol                0.002227
Age                     0.001510
DiffWalk                0.000690
PhysHlth                0.000635
HvyAlcoholConsump       0.000631
HeartDiseaseorAttack    0.000607
MentHlth                0.000497
Income                  0.000442
Sex                     0.000307
Education               0.000142
CholCheck               0.000095
AnyHealthcare           0.000083
Veggies                 0.000083
NoDocbcCost             0.000051
Stroke                  0.000024
Fruits                 -0.000008
Smoker                 -0.000075
PhysActivity           -0.000371


More details are in this Jupyter Notebook. 