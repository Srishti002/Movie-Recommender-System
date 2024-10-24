# Movie Recommender System
## Types Of Recommender System:-

### 1. Collaborative Filtering :
Recommends items to you based on ratings of users who gave similar ratings as you. Means it finds similarity between users or items and according to that it recommends things.

### 2. Content based filtering:
Recommends items based on features of user and item  to find good match. Unlike collaborative filtering, it doesn't rely on other users' behaviors.
There are two methods for this Content based filtering :
    > Feature 








## Step by Step Guide :
 ### 1. Dataset:- 
 Link : https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?resource=download
 
 Here we are loading both *'tmdb_5000_movies.csv'* and *'tmdb_5000_credits.csv'*

 ### Data Preprocessing :
 - We merge both movies and credits on the basis of *title*.
 - We'll keep only few columns that are necessary like *'movie_id','title','overview','genres','keywords','cast','crew'*
 - The data in the columns is not the proper list format. So we have to convert that into proper list forms.
 - After applying all transformation to convert data into proper format, we then combine *'overview','genres','keywords','cast','crew'* into one single column *'tags'*
 - So, our final data looks like this :-
   ![](
