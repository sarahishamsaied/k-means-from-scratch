# K Means Clustering Algorithm Implemented from Scratch
## Introduction
K-Means clustering algorithm is implemented from scratch to unveil hidden patterns and insights among the football players featured in ***FIFA 22***.


# Feature Selection
  a subset of features from the FIFA 22 player dataset are selected because they capture key attributes of football players, such as their current performance, future potential, market value, salary, and age..
These features include ***"overall," "potential," "wage_eur," "value_eur," and "age."***

## K means algorithm quick overview
K-Means is an unsupervised machine learning algorithm used for clustering or grouping data points into clusters.
It is widely used in data analysis and pattern recognition. The goal of K-Means is to find groups in the data, with the number of groups (clusters) denoted by ***"K."*** Here's how it works:

1. ***Initialization***: Starting by selecting K initial centroids. These centroids are initially chosen randomly from the dataset itself.

2. ***Assignment***: Assigning each data point to the nearest centroid. This is done by calculating the distance (Eucledian Distance) between each data point and each centroid. The data point is assigned to the cluster associated with the nearest centroid.
   - ### Eucledian Distance (In case of 2 dimensions)
        $$\sqrt{(x2-x1)^2 + (y2-y2)^2}$$

4. ***Re-generate new centroids***: Recalculating the centroids of each cluster by taking the ***geometric mean*** of all the data points assigned to that cluster.
    - ### Geometric Mean
       $$\left( x_1 \cdot x_2 \cdot x_3 \cdot \ldots \cdot x_n \right)^{\frac{1}{n}}$$
 
***Repeat***: Repeat steps 2, 3 until the new centroids are equal to the old centroids ***or*** the maximum number or iterations are reached
Result: The final centroids represent the center of each cluster. The data points are clustered based on their proximity to these centroids.

# Quick Demonstration
#### Before Clustering
<img src="https://github.com/sarahishamsaied/k-means-from-scratch/assets/71923204/48f04f23-33cc-4424-bef6-934536f4fe48" width="410" />



#### After Clustering

![cluster](https://github.com/sarahishamsaied/k-means-from-scratch/assets/71923204/134b4d06-1d26-40d9-a02d-64f197e64a62)

# Data
You can download the dataset from here https://www.kaggle.com/datasets/stefanoleone992/fifa-22-complete-player-dataset. Use the file `players_22.csv`
