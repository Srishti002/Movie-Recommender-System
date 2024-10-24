# Movie Recommender System

## Introduction :
In this project we are making a movie recommender system using *'Content based Filtering'*

> ### Types Of Recommender System:-

  > #### 1. Collaborative Filtering :

  Recommends items to you based on ratings of users who gave similar ratings as you. 
  Means it finds similarity between users or items and according to that it recommends things.

  > #### 2. Content based filtering:

  Recommends items based on features of user and item  to find good match. Unlike collaborative filtering, it doesn't rely on other users' behaviors.
  There are two methods for this Content based filtering :
     > Feature 








## Step by Step Guide :
 ### 1. Dataset:- 
 Link : https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?resource=download
 
 Here we are loading both *'tmdb_5000_movies.csv'* and *'tmdb_5000_credits.csv'*

 ### 2. Data Preprocessing :
 - We merge both movies and credits on the basis of *title*.
 - We'll keep only few columns that are necessary like *'movie_id','title','overview','genres','keywords','cast','crew'*
 - The data in the columns is not the proper list format. So we have to convert that into proper list forms.
 - After applying all transformation to convert data into proper format, we then combine *'overview','genres','keywords','cast','crew'* into one single column *'tags'*
 - So, our final data looks like this :-
   
   ![](https://github.com/Srishti002/Movie-Recommender-System/blob/main/Screenshot%202024-10-25%20015510.png)
   
 - We have to apply stemming operation in the 'tags' column means we have to get the *root* word from the whole word like *run* from *running*.
 - Now , we have to convert our text data into some vector form. So we import *'CountVectorizer'*here as it converts text data into some numberical value.
 -  The max_features parameter specifies the maximum number of features (unique words) to consider in the vocabulary. Setting it to 5000 means that only the 5000 most frequent words will be used.
 -  The stop_words parameter specifies a list of words to be ignored during the vectorization process. Setting it to 'english' indicates that the built-in list of English stop words (common words like "the", "and", "in") will be used.

    ![](https://github.com/Srishti002/Movie-Recommender-System/blob/main/Screenshot%202024-10-25%20021246.png)

### 3. Cosine Similarity:
It actually measures the cosine of the angle between two vectors. Cosine similarity is a metric, helpful in determining, how similar the data objects are irrespective of their size.

Sc(x,y) = x . y / ||x|| × ||y||

The cosine similarity between two vectors is measured in ‘θ’.

### 4. Results:
![](https://github.com/Srishti002/Movie-Recommender-System/blob/main/Screenshot%202024-10-25%20022743.png)

