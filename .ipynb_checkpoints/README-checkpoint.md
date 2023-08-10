# Crypto Clustering

![Decorative image.](Images/crypto-image.png)

## Background

In this notebook, we'll be analysing an approach that clusters cryptocurrencies by their performance in different time periods instead of focusing only on returns and volatility, to understand the factors that might impact crypto market. 
For this we'll be using *Unsupervised Learning* algorithms:
..* KMeans Clustering algorithm - finds observations in a dataset that are like each other and places them in a set. This algo aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean, serving as a prototype of the cluster.
..* Principal Component Analysis (PCA)- a method that uses patterns present in high-dimensional data (data with lots of independent variables) to reduce the complexity of the data while retaining most of the information.


## Files

1. [Crypto Clustering usin KMeans](crypto_investments.ipynb)

## Steps followed

The steps for this analysis are divided into the following sections:

* Import the Data (provided in the starter code)

* Prepare the Data (provided in the starter code)

* Find the Best Value for k Using the Original Data

* Cluster Cryptocurrencies with K-means Using the Original Data

* Optimise Clusters with Principal Component Analysis

* Find the Best Value for k Using the PCA Data

* Cluster the Cryptocurrencies with K-means Using the PCA Data

* Visualise and Compare the Results


### Reference

* [the hvPlot documentation](https://holoviz.org/tutorial/Composing_Plots.html).

