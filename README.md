# Crypto Clustering

![Decorative image.](Images/crypto-image.png)

## Background

In this notebook, we'll be analysing an approach that clusters cryptocurrencies by their performance in different time periods instead of focusing only on returns and volatility, to understand the factors that might impact crypto market. 
For this we'll be using *Unsupervised Learning* algorithms:
..* KMeans Clustering algorithm - finds observations in a dataset that are like each other and places them in a set. This algo aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean, serving as a prototype of the cluster.
..* Principal Component Analysis (PCA)- a method that uses patterns present in high-dimensional data (data with lots of independent variables) to reduce the complexity of the data while retaining most of the information.


## Files

1. [Crypto Clustering usin KMeans](crypto_investments.ipynb)

## Instructions

The steps for this analysis are divided into the following sections:

* Import the Data (provided in the starter code)

* Prepare the Data (provided in the starter code)

* Find the Best Value for k Using the Original Data

* Cluster Cryptocurrencies with K-means Using the Original Data

* Optimise Clusters with Principal Component Analysis

* Find the Best Value for k Using the PCA Data

* Cluster the Cryptocurrencies with K-means Using the PCA Data

* Visualise and Compare the Results

### Find the Best Value for k Using the Original Data

In this section, we will use the elbow method to find the best value for k.

1. Code the elbow method algorithm to find the best value for k. Using a range from 1 to 11.

2. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

3. Answer the question: What is the best value for k?

### Cluster Cryptocurrencies with K-means Using the Original Data

In this section, we will use the K-means algorithm with the best value for k (found in the previous section) in order to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.

1. Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model using the original data.

3. Predict the clusters to group the cryptocurrencies using the original data. View the resulting array of cluster values.

4. Create a copy of the original data and add a new column with the predicted clusters.

5. Using hvPlot, create a scatter plot by setting `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. Colour the graph points with the labels found using K-means. Then, add the crypto name in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

### Optimise Clusters with Principal Component Analysis

In this section, we will perform a principal component analysis (PCA) and reduce the features to three principal components.

1. Create a PCA model instance and set `n_components=3`.

2. Use the PCA model to reduce to three principal components. View the first five rows of the DataFrame.

3. Retrieve the explained variance to determine how much information can be attributed to each principal component.

4. Answer the question: What is the total explained variance of the three principal components?

5. Create a new DataFrame with the PCA data. Be sure to set the `coin_id` index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

### Find the Best Value for k Using the PCA Data

In this section, we will use the elbow method to find the best value for k by using the PCA data.

1. Code the elbow method algorithm and use the PCA data to find the best value for k. Use a range from 1 to 11.

2. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

3. Answer the questions: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

### Cluster Cryptocurrencies with K-means Using the PCA Data

In this section, you will use the PCA data and the K-means algorithm with the best value for k (found in the previous section) in order to cluster the cryptocurrencies according to the principal components.

1. Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model by using the PCA data.

3. Predict the clusters to group the cryptocurrencies by using the PCA data. View the resulting array of cluster values.

4. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.

5. Using hvPlot, create a scatter plot by setting `x="PC1"` and `y="PC2"`. Colour the graph points with the labels found using K-means. Then, add the crypto name in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

### Visualise and Compare the Results

In this section, you will visually analyse the cluster analysis results by observing the outcome with and without using the optimisation techniques.

1. Create a composite plot using hvPlot and the plus (`+`) operator to compare the elbow curve that you created to find the best value for k with the original data and the PCA data.

2. Create a composite plot using hvPlot and the plus (`+`) operator to compare the cryptocurrencies clusters using the original data and the PCA data.

3. Answer the following question: After visually analysing the cluster analysis results, what is the impact of using fewer features to cluster the data by using K-means?

### Reference

* [the hvPlot documentation](https://holoviz.org/tutorial/Composing_Plots.html).

