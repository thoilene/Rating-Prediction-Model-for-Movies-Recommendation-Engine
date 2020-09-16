# Rating Prediction Model for Movies Recommendation Engine

## Introduction - Business Understanding

Ratings a commonly used in business by consumers for scoring the quality of products, services and articles. This information is then used by providers to make recommendations to other consumers. Many recommendation systems are rank-based, content based or based on collaborative filtering. The latter consists to group consumers with similar behavior and recommend them similar products, services or articles.
Predictive models try to predict the rating a consumer will assign to a product or service if he or she interacts with this. 

A movies streaming platform would like to make recommendations to registrated users. The current work will create a movie recommendation engine based on a movie rating prediction model which will be develop here. The model will be created on MovieTweetings dataset with contains movies details and review data.

# Data Understanding

The MovieTweetings dataset is a live movie rating dataset collected from Twitter. This dataset is availble here [movietweetings](https://data.world/sidooms/movietweetings) for free (e-mail registration may be necessary). It contains 3 sub-datasets.

- movies.dat: contains movie-id, movie title and genre 
- users.dat: contains details (will not be used here)
- ratings.dat: contains user-id, movie-id, rating and timestamp

## Results and Conclusion

The Movies Recommendation Engine built in the current work with a fast matrix factorization procedure known as ["Funk SVD"](https://github.com/gbolmier/funk-svd). It is an efficient matrix factorization algorithm which is well-adapted to sparse matrices as it is usually the case for rating data. 

The performance of the SVD-model is quite good with RMSE arround 1.68 and MAE arround 1.26 on validation data for ratings in a range of 1 to 10. 

|          | **Validation** | **Test**   |
|:---------| :-------------:| ---------: |
|**RMSE**  | 1.68491        | 1.7615     |
|**MAE**   | 1.26415        | 1.34874    | 

The SVD model on MovieTweeting data can predict the ratings with a mean absolute error of 1.35 point on unknown data (test data). This shows that this model is reliable.
