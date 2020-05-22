simple_glm : I converted the data to numeric and filled in the empty data
      with the median of the row

simple_rf : Same as simple_glm but use a randomforest instead

simple_gbm : Same as simple_glm but use a gbm instead

simple_census : I added in census data mostly focusing on income, education,
      age, and population. Additionally, I converted the zip code to a longitude
      and latitude for numeric input

simple_census_percentage : I added up the population from the census data for
      each zipcode and turned relevant values into percentages as well. From there
      I checked to see if a gbm works better when we have raw value, raw value
      plus percentage, or just the percentage

census_noise : I took the data and made it noisey - I took all the data and copied it,
      multiplied each value by a gaussian random variable with mean 1 and sd .03

census_depths : Since the model was predicting fairly well, I messed around with
      the gbm interaction depth in this one determining the optimal depth

*census_demographics : I added demographic and ethnicity data from the census data

census_pca : I removed different values from the dataset and did PCA analysis
      on the data and added the first 10 dimensions to the data

census_kmeans : I performed kmeans analysis on the data where I had k=5,10,25,50,100
      and averaged the number of PastDue in the cluster and added each of those
      to data before passing it into the gbm

* I believe that prediction was the best, I kind of lost track with version control
    and got lost sadly. Overall 91% isn't too bad...
