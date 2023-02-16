# Decision Tree Algorithm

**Data**:
The dataset is obtained from the Census Bureau and represents the salaries of people along with seven demographic variables. It can be accessed by passing this link into pd.read_csv function https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true. 

**Instructions**:
Open the link with the ipynb extension on GitHub(https://github.com/wrutkowska/BSAN6070/blob/main/CA03/CA03.ipynb) to access the notebook immediately or download it and open it either through Jupyter or Google Colab if you want to run the code and try it yourself. 

**Description**:
The purpose of this assignment was to develop the “best” (in our case) decision tree model by tunning the algorithm with different hyperparameters and then using that model to predict a new individual’s income category with given data about this person. First I needed to clean and prepare the data and this process included Data Quality Analsysis and one-hot encoding to transform categorical variables into dummy variables. Then I needed to split the data for train and test data based on the flag column. The next step consisted of extracting the target variable "y" from the train and test data and extracting all the other independent variables from the train and test data. All these pre-processing steps allowed me to build a decision tree model using DecisionTreeClassifier class from scikit-learn. Once the model was built, I needed to evaluate it by calculating Accuracy, Recall, Precision, and F1 Score. The next step was to tune decision tree performance using four hyperparameters (split criteria, maximum features, maximum sample leaf, and maximum depth) and to develop a tree with the highest accuracy score. By running four models I was able to find the best-performing tree, I visualized it, and eventually using the best decision tree model, I predicted a new person’s Income Category ((<=50K, or >50K ) having given a set of information. After doing the neccesary calculations I discovered that the predicted annual income category is > $50,000 and the probability that my prediction for the new individual is correct is 87.5%

**Conclusion**:
Even though the tree I developed was not the “best”, it was still performing pretty well and I was able to make some real-life predictions. The total runtime of the best tree was less than a second, however, creating the entire notebook, writing the codes for preparing the data and building the model, evaluating the performance, and tuning parameters took me probably 2-3 days. 
