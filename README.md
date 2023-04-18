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