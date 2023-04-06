# **CA06: Customer Segmentation using K-Means Clustering**

### **Dataset Description**

The Mall Customers dataset contains information about customers who visit a shopping mall. The dataset has 5 columns which include CustomerID, Gender, Age, Annual Income (in thousands of dollars), and Spending Score (a score assigned by the mall based on customer behavior and spending nature, ranging from 1 to 100). There are no missing values in the dataset and the data types of each column are appropriate.

### **Exploratory Data Analysis and Data Preparation**

First, I loaded the dataset and performed EDA where I checked the variables, visualized their distributions, and checked for any missing values or duplicated rows. The dataset did not contain any missing values or duplicated rows, so I did not have to handle them. I then performed feature scaling using the StandardScaler from scikit-learn to scale the annual income and spending score features. Next, I selected the appropriate features for clustering, which were Annual Income and Spending Score. Finally, I created a new data frame with only the selected features.

### **K-Means Clustering**

To determine the optimal number of clusters, I used the Silhouette Method and plotted the silhouette scores for different numbers of clusters. I selected the number of clusters with the highest silhouette score, which was 5. KMeans clustering with 5 clusters was used to group the customers based on their Annual Income and Spending Score. Each cluster was described as follows:
•	Cluster 0: Medium income, Medium spending
•	Cluster 1: High income, Low spending
•	Cluster 2: Low income, Low spending
•	Cluster 3: Low income, High spending
•	Cluster 4: High income, High spending

### **Insights and Recommendations**

The analysis can help the mall to develop marketing strategies that are tailored to the needs and preferences of each group. The recommendations for each cluster are:
•	Cluster 0: offer discounts on high-end products to incentivize spending and develop loyalty programs.
•	Cluster 1: conduct customer research and offer personalized services and experiences.
•	Cluster 2: offer more affordable products and provide discounts or promotions.
•	Cluster 3: provide financing options and discounts on complementary products.
•	Cluster 4: offer exclusive products and personalized services to enhance the high-end shopping experience.

The mall can use this analysis to improve customer satisfaction, increase sales, and boost profitability.
