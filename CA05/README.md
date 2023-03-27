# **CA05 - kNN based Movie Recommender Engine**

This assignment implements a kNN-based movie recommender engine using Python's scikit-learn library. The goal is to recommend movies that are most similar to a given movie based on the genre information and IMDb rating. 

**What question are we trying to answer?** - 
Given a movies data set, what are the 5 most similar movies to a movie query?

### **Data**
I used a small sub-set of the data extracted from the UCI’s IMDB data set. The data file is named movies_recommendation_data.csv and is located at the following URL: https://github.com/ArinB/MSBA-CA-Data/raw/main/CA05/movies_recommendation_data.csv.
The data contains thirty movies, including data for each movie across seven genres and their IMDB ratings. The implementation assumes that all columns contain numerical data - the data is already encoded and a value of 1 indicates that a movie belongs to a particular genre type and 0 indicates that it does not.
Additionally, there are relationships among the movies that will not be accounted for (e.g. actors, directors, and themes) when using the KNN algorithm simply because the data that captures those relationships are missing from the data set. Consequently, when I run the KNN algorithm on the data mentioned previously, similarity will be based solely on the included genres and the IMDB ratings of the movies.

### **Instructions**
Open the link with the ipynb extension on GitHub () to access the notebook immediately or download it and open it either through Jupyter or Google Colab if you want to run the code and try it yourself. The necessary libraries needed to run the models are included at the top of the notebook.

Building your own Recommender System
Imagine you are building your own movie recommendation website which uses your recommendation engine at the back-end. A user is navigating your recommendation website and encounters a movie named “The Post”. The user is not sure if he/she wants to watch it, but its genres intrigue the user; he/she is curious about other similar movies. The user can see recommended movies in the "More Like This" section of the website. When a user selects a movie, the back-end algorithm creates a feature vector for that movie and searches for the 5 most similar movies in the recommendation data set. The back-end then sends these recommended movies back to the website for the user to see.

**Following is the genre information about the movie “The Post”:**

*IMDB Rating = 7.2, Biography = Yes, Drama = Yes, Thriller = No, Comedy = No, Crime = No, Mystery = No, History = Yes*

The code uses the data from movies_recommendation_data.csv, creates a feature vector for "The Post" based on its genre information and IMDb rating, fits a kNN model to the genre information and IMDb rating of all movies, finds the 5 nearest neighbors to "The Post", and prints the titles of the recommended movies. 

To run the code, you will need to have scikit-learn installed. You can install it via pip using the following command:

*pip install scikit-learn*

### **Conclusion**
In this assignment, I implemented a kNN-based movie recommender engine that recommends movies based on their genre information and IMDb rating. I found the top 5 recommended movies that a user might like after watching “The Post”. Although this is a simplistic approach to creating a movie recommender system, it can be used as a starting point for building more advanced systems that take into account additional factors such as director, cast, and plot.
