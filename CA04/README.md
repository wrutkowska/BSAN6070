## CA04 – Ensemble Models

**Data**

The dataset is obtained from the Census Bureau and represents the salaries of people along with seven demographic variables. The following is a description of the dataset:
- Number of target classes: 2 ('>50K' and '<=50K') [Labels: 1, 0]
- Number of attributes (Columns): 7
- Number of instances (Rows): 48,842
It can be accessed by passing this link into "pd.read_csv" function:
https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true

**Instructions**

Open the link with the ipynb extension on GitHub() to access the notebook immediately or download it and open it either through Jupyter or Google Colab if you want to run the code and try it yourself. The necessary libraries needed to run the models are included at the top of the notebook.

**Description**

The purpose of this assignment was to train four ensemble models and compare the best values of accuracy and AUC using n estimator values of 50,100,150,200,250,300,350,400,450,500. First I needed to clean and prepare the data and this process included Data Quality Analsysis and one-hot encoding to transform categorical variables into dummy variables. Then I needed to split the data for train and test data based on the flag column. The next step consisted of extracting the target variable "y" from the train and test data and extracting all the other independent variables from the train and test data. All these pre-processing steps allowed me to build a random forest classifier model using RandomForestClassifier from sklearn.ensemble. Next, I built AdaBoost, Gradient Boost, and XGB models following the steps from the Random Forest model. The last step was to compare the performance of all models - I calculated the best accuracy score and the best AUC score for four models and created a table with the best metrics for all models. One issue that I encountered was with training the XGBoost model - since the features’ names in the data included special characters such as period or dash, I couldn’t run the model because the names were not compatible with some XGBoost versions. I removed all special characters and replaced the old column names in x_test, x_train,  y_test, y_train with the new, clean column names.

**Conclusion**

Although the models have similar best Accuracy and AUC values (the differences are only by 0.01), the XGB Classifer seems to be the one that has the highest Accuracy Score and the highest AUC Score out of all four models. Please note that further tuning of the hyperparameters may result in even better performance.
