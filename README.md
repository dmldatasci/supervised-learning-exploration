# supervised-learning-exploration
A collection of exploratory exercises to improve supervised machine learning skills.

## Unit 19 - Unsupervised Learning

### Lesson Plans

* [19.1 - Lesson Plan](1/LessonPlan.md)
* [19.2 - Lesson Plan](2/LessonPlan.md)
* [19.3 - Lesson Plan](3/LessonPlan.md)


## Slideshows

* [19.1 Slideshow](https://docs.google.com/presentation/d/1oFYZxMIySdV8wl9ZAPM_nhsHv3JXCWdI861VnA8J2x0/edit?usp=sharing)

* [19.2 Slideshow](https://docs.google.com/presentation/d/11bEGLGXm871w5-EqYbew4izuNu2ZYObDXWUWhsMs0XY/edit?usp=sharing)

* [19.3 Slideshow](https://docs.google.com/presentation/d/1sG41nFHSatSU1SibFNqVCLGzBGeWoPPHeMedxY2OtGM/edit?usp=sharing)

# `03-segmenting_customers`

In this activity, you will create two K-means models to segment your customers: one with three clusters and one with four clusters. Then, you’ll compare these two models to the two-cluster model you previously created.

## Background

Your marketing department has just come back to you regarding the initial analysis you performed on the customer ratings for mobile application and in-person banker services. Although your initial analysis of grouping the customers into two segments was helpful, they are wondering if the data could be even more finely clustered.

You have been asked to review the customer ratings data when modeled with three and four clusters.

Using the information in the [starter file](Unsolved/segmenting_customers.ipynb), apply the K-means algorithm to the `service_ratings` data using both three and four clusters to segment the customer information.

## Instructions

1. Review the Pandas DataFrame and plot associated with `service_ratings.csv`.

2. Run the K-means algorithm identifying three clusters in the data. Make sure to do the following:

   - Create and initialize the K-means model for three clusters. Use a `random_state` value of 1 for the model.
   
   - Fit, or train, the model by using the `service_ratings_df` DataFrame.
   
   - Make predictions about the clustering by using the trained model. Save the predictions to a variable called `customer_segment_3` and print that variable.
   
   - Create a copy of the DataFrame and name it `service_ratings_predictions_df`.
   
   - Add a column to the `service_ratings_predictions_df` DataFrame called "customer_segment_3" and add the `customer_segment_3` information to the column.
   
   - Plot the data by using the DataFrame adjusted to include customer segment information for three clusters.

3. Run the K-means algorithm identifying four clusters in the data. Make sure to do the following: 

   - Create and initialize the K-means model for four clusters. Use a `random_state` value of 1 for the model.
   
   - Fit, or train, the model by using the `service_ratings_df` DataFrame.
   
   - Make predictions about the clustering by using the trained model. Save the predictions to a variable called `customer_segment_4` and print that variable.
   
   - Add a column to the `service_ratings_predictions_df` DataFrame called "customer_segment_4" and add the `customer_segment_4` information to the column.
   
   - Plot the data by using the DataFrame adjusted to include customer segment information for four clusters.

4. Answer the following question: Can any additional information be gleaned from the customer segmentation data when clusters of three and four are applied?









# Finding k

In this activity, you will use the elbow method to determine the optimal number of clusters that should be used to segment a dataset of stock pricing information.

## Background

You have been analyzing the pricing data on one of the stocks your firm owns. Specifically, you were examining the relationship between the day's trading volume and the spread between the high and low trading price.

Using the information contained in the starter file, use the elbow method to determine the optimal number of clusters, `k`, that should be used to segment these trades. Once the elbow curve has been established, evaluate the two most likely values for `k` using the K-means algorithm and a scatter plot.

## Instructions

1. Read in the `stock_data.csv` file from the Resources folder and create a DataFrame. Set the “date” column to create the DatetimeIndex. Be sure to include parameters for `parse_dates` and `infer_datetime_format`.

2. Scale the data by using the `StandardScaler` module to normalize the DataFrame values.

3. Create a new DataFrame with the scaled data and name it `spread_scaled_df`.

   > **Hint:** You can use the columns and index DataFrame's attributes to set the column names and the index of the new DataFrame. Review [this article from the Pandas documentation](https://pandas.pydata.org/docs/reference/frame.html#attributes-and-underlying-data) if you want a refresher.

4. Create two lists: one to hold the list of inertia scores, and another for the range of k values (from 1 to 11) to analyze.

5. Using a `for` loop to evaluate each instance of k, define a K-means model, fit the K-means model based on the DataFrame, and append the model’s inertia to the empty inertia list that you created in the previous step.

6. Store the values for k and the inertia in a dictionary called `elbow_data`. Use `elbow_data` to create a Pandas DataFrame called `df_elbow`.

7. Using hvPlot, plot the `df_elbow` DataFrame to visualize the elbow curve.

8. Perform the following tasks for each of the two most likely values of `k`:

   - Define a K-means model by using `k` to define the clusters, fit the model, make predictions, and add the prediction values to a copy of the scaled DataFrame named `spread_predictions_df`.

   - Plot the clusters. The x-axis should reflect the "hi_low_spread", and the y-axis should reflect the "volume".

9. Answer the following question: Considering the plot, what’s the best number of clusters or value of k to choose?