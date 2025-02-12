# Project Title: Personalized Top 5 Movie Recommendations Model Using User Ratings

### 📌 Student Details

* Phase: DSF_PT08P3

* Student Name: Gilbert Kipkirui Cheruiyot
  
* Student Pace: Part Time
  
* Instructor Name: Daniel Ekale

![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation-Project_GKC/blob/main/Images/12713.jpg)

### 📌 Table of Contents
1. Project Overview
2. Business Problem
3. Business Objectives
4. Target Audience
5. Data Source
6. Data Understanding
7. Data Preprocessing
8. Modelling & Evaluation
9. Recommendation System Output
10. Conclusion
11. Recommendation
12. Future Optimizations

### 1. Project Overview
People from all walks of life can connect via movies. However, our personal tastes in movies still differ, ranging from concentrating on our favourite actors and directors to certain genres like romance, sci-fi, or thrillers. Although it's difficult to categorise movies that everyone would like, data scientists use behavioural patterns to find social groups with comparable movie tastes. As data scientists, we use machine learning to create a movie recommendation system by drawing insightful conclusions from audience behaviour and movies' characteristics. My project's objective is to create a model that, based on a user's assessments of previous movies, suggests the top five movies. By using the "classic" MovieLens dataset, which is widely utilised in scholarly research and proofs-of-concept for machine learning, we want to show the power of data-driven recommendations. The main focus of our recommendation system is to filter and predict only those movies that a user would prefer, given some data about the user.

### 2. Business Problem
The audience is in need of a model that provides top 5 movie recommendations to a user, based on their ratings of other movies.

### 3. Business Objectives
The objective of this project is to develop a model to:
* Develop a machine learning model that delivers personalized top 5 movie recommendations to users.

* Base recommendations on individual movie ratings provided by users.

* Achieve a more engaging and profitable recommendation system for the stakeholders.

* Boost user satisfaction through personalized movie recommendations.

* Expose movie users to new and diverse content, expanding their horizons and introducing them to items they might have overlooked.

### 4. Target Audience
The Target audience for this project are:
* Movie lovers

* Movie studios/distributors

* E-commerce business selling movies
    
### 5. Data Source
The data was sourced from https://grouplens.org/datasets/movielens/latest/ and has files named links.csv, movies.csv, ratings.csv and tags.csv. 

### 6. Data Understanding

📊 Data description:
#### df_links dataset:

* movieId: A unique identifier for each movie.

* imdbId: The unique identifier for the movie on IMDb.

* tmdbId: The unique identifier for the movie on TMDb (The Movie Database).

#### df_movies dataset:

* movieId: A unique identifier for each movie.

* title: The title of the movie, including the release year.

* genres: The genres associated with the movie, separated by pipes (|).

#### df_ratings dataset:

* userId: A unique identifier for each user.

* movieId: A unique identifier for each movie.

* rating: The rating given by the user to the movie, typically on a scale (e.g., 1 to 5).

* timestamp: The time when the rating was given, in Unix epoch format.

#### df_tags dataset:

* userId: A unique identifier for each user.

* movieId: A unique identifier for each movie.

* tag: A tag or keyword provided by the user for the movie.

* timestamp: The time when the tag was added, in Unix epoch format.

The data used for this project:
* For the purpose of the project, I have merged data frames relating to movies.csv, ratings.csv and tags.csv. 
* The merged dataset has 219,406 entries and 6 columns. The columns include userId and movieId with integer data type, rating in form of a float, and title, genres, and tag with object data type.

### 🧠 Exploratory Data Analysis
Insights from EDA are as illustrated below: 

* Top_10_most_popular_tags
![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC/blob/main/Images/TAGS.png)

* Top 10 Most Popular Genres
![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC/blob/main/Images/GENRE.png)

* Top 10 Movies by Number of 5-Star Ratings
![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC/blob/main/Images/RATING.png)

* Distribution of Movie Ratings
![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC/blob/main/Images/DISTR.png)

* Distribution of Average Ratings per User
![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC/blob/main/Images/USER.png)

* Scatter plot of Movie Ratings per User
![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC/blob/main/Images/SCATTER.png)

### 7. Data Pre_processing
The following processes were carried out to the training and test features before building the models:
* I prepared data in a format compatible with surprise by use of a reader

* Split the resulting dataframe into train and test splits

### 8. Modelling & Evaluation
In this project, I created 3 models, namely:
1. Collaborative Filtering Model with Singular Value Decomposition (SVD)
 - I prepared the SVD baseline model and tuned it.

2. Content-Based Filtering Model
- Vectorized the text data using TfidfVectorizer
-  Used Nearest Neighbors to find similar movies

3. Hybrid Approach
- Combined both collaborative filtering with SVD and content-based models to come up with Hybrid model.#

To evaluate the models, I have used __Root Mean Square Error (RMSE)__. A lower RMSE is indicative of improved performance and vice versa.

### 9. Recommendation System Output

* Collaborative Filtering with Singular Value Decomposition (SVD) Model

![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation-Project_GKC/blob/main/Images/SVD.png)

* Content- Based Filtering Model

![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation-Project_GKC/blob/main/Images/CBF.png)

* Hybrid Approach

![movie data erd](https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation-Project_GKC/blob/main/Images/HYBRID.png)

### 10. Conclusion

Based on the evaluation results, I was able to arrive at the following:

* All the three models were able to identify movies with the highest rating of 5.

* The collaborative filtering with Singular Value Decomposition model with a low RMSE indicates higher accuracy as compared to the hybrid and content based filtering model.

* Content-Based Filtering method provides moderate RSME, indicating fairly good accuracy. This can be a good alternative if the user has rich content features and want to recommend items based on the attributes of movies the user has liked.

* The hybrid model appears to take into consideration both collaborative filtering and content-based filtering model details. The moderately higher RMSE indicates slightly lower prediction accuracy compared to the other two models.


### 11. Recommendation

* Because of its accuracy and capacity to employ user-specific interaction data, Collaborative Filtering (SVD) model is the best option given the task's emphasis on user ratings. Its accuracy and simplicity makes it a favourable recommendation model.


### 12. Future Optimizations

* I plan to evaluate other models deep learning models that may offer better performance.

## 📌 Repository Navigation
- **data/**: Contains the raw and processed data files
  - `ratings.csv`: User ratings data
  - `movies.csv`: Movie information data
- **images/**: Contains the images used in the project
  - `12713.jpg`: Image used in presentation
  - `movie_concept.jpg`: Image to use in presentation
- **presentation/**: Contains the presentation ppt for the project
  - `presentation.csv`: Movie lense recommendation system presentation
- **notebooks/**: Jupyter notebooks for data analysis and modeling
  - `Index.ipynb`: Data understanding, preprocessing, Exploratory data analysis, model training and evaluation
- **README.md**: Project summary, machine learning steps, links, and navigation instructions

## 🚀 Instructions
To get started with the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/gkipkirui1/DSF-PT08P4-Movie_Recommendation_Project_GKC.git


2. Install Dependencies:

* pip install -r requirements.txt

* Run Jupyter Notebook:

* Jupyter notebook

## 📌 Dependencies

Python 3.x

pandas, 
numpy, 
matplotlib, 
seaborn, 
scikit-learn, 
surprise library





