Week 8
======

- Unsupervised Learning
    - Clustering
        - Unsupervised Learning: Introduction
        - K-Means Algorithm
        - Optimization Objective
        - Random Initialization
        - Choosing the Number of Clusters
    - Review
        - Quiz: Unsupervised Learning
- Dimensionality Reduction
    - Motivation
        - Motivation I: Data Compression
        - Motivation II: Visualization
    - Principal Component Analysis
        - Principal Component Analysis Problem Formulation
        - Principal Component Analysis Algorithm
    - Applying PCA
        - Reconstruction from Compressed Representation
        - Choosing the Number of Principal Components
        - Advice for Applying PCA
    - Review
        - Quiz: Principal Component Analysis
        - Assignment: K-Means Clustering and PCA

--------------------------------------------------------------------------------

Unsupervised Learning
=====================

- Clustering
    - Unsupervised Learning: Introduction
    - K-Means Algorithm
    - Optimization Objective
    - Random Initialization
    - Choosing the Number of Clusters
- Review
    - Quiz: Unsupervised Learning

\[Clustering] Unsupervised Learning: Introduction
-------------------------------------------------

Unsupervised learning is contrasted from supervised learning because it uses an **unlabelled** training set rather than a labeled one.

In other words, we don't have the vector `y` of expected results, we only have a dataset of features where we can find structure.

Clustering is good for:

- Market segmentation
- Social network analysis
- Organizing computer clusters
- Astronomical data analysis

\[Clustering] K-Means Algorithm
-------------------------------

The K-Means Algorithm is the most popular and widely used algorithm for automatically grouping data into coherent subsets.

1. Randomly initialise two points in the dataset called the *cluster centroids*.
2. Cluster assignment: assign all examples into one of two groups based on which cluster centroid the example is closest to.
3. Move centroid: compute the averages for all the points inside each of the two cluster centroid groups, then move the cluster centroid points to those averages.
4. Re-run (2) and (3) until we have found our clusters.

TODO: TBA

\[Clustering] Optimization Objective
------------------------------------

TODO: TBA

\[Clustering] Random Initialization
-----------------------------------

There's one particular recommended method for randomly initialising your cluster centroids.

1. Have `K < m`. That is, make sure the number of your clusters is less than the number of your training examples.
2. Randomly pick `K` training examples.
3. Set µ<sub>1</sub>, ..., µ<sub><i>k</i></sub> equal to these `K` examples.

K-means **can get stuck in local optima**. To decrease the chance of this happening, you can run the algorithm on many different random initialisations.

```
for i = 1 to 100:
  randomly initialise k-means
  run k-means to get 'c' and 'm'
  compute the cost function (distortion) J(c,m)
pick the clustering that gave us the lowest cost
```

\[Clustering] Choosing the Number of Clusters
---------------------------------------------

Choosing `K` can be quite arbitrary and ambiguous.

**The elbow method**: plot the cost `J` and the number of clusters `K`. The cost function should reduce as we increase the number of clusters, and then flatten out. Choose `K` at the point where the cost function starts to flatten out.

However, fairly often, the curve is **very gradual**, so there's no clear elbow.

**Note:** `J` will **always** decrease as `K` is increased. The one exception is if k-means gets stuck at a bad local optimum.

Another way to choose `K` is to observe how well k-means performs on a **downstream purpose**. In other words, you choose `K` that proves to be most useful for some goal you're trying to achieve from using these clusters.

\[Review] Quiz: Unsupervised Learning
-------------------------------------

TODO: TBA

--------------------------------------------------------------------------------

Dimensionality Reduction
========================

- Motivation
    - Motivation I: Data Compression
    - Motivation II: Visualization
- Principal Component Analysis
    - Principal Component Analysis Problem Formulation
    - Principal Component Analysis Algorithm
- Applying PCA
    - Reconstruction from Compressed Representation
    - Choosing the Number of Principal Components
    - Advice for Applying PCA
- Review
    - Quiz: Principal Component Analysis
    - Assignment: K-Means Clustering and PCA

\[Motivation] Motivation I: Data Compression
--------------------------------------------

TODO: TBA

\[Motivation] Motivation II: Visualization
------------------------------------------

TODO: TBA

\[Principal Component Analysis] Principal Component Analysis Problem Formulation
--------------------------------------------------------------------------------

TODO: TBA

\[Principal Component Analysis] Principal Component Analysis Algorithm
----------------------------------------------------------------------

TODO: TBA

\[Applying PCA] Reconstruction from Compressed Representation
-------------------------------------------------------------

TODO: TBA

\[Applying PCA] Choosing the Number of Principal Components
-----------------------------------------------------------

TODO: TBA

\[Applying PCA] Advice for Applying PCA
---------------------------------------

TODO: TBA

\[Review] Quiz: Principal Component Analysis
--------------------------------------------

TODO: TBA

\[Review] Assignment: K-Means Clustering and PCA
------------------------------------------------

TODO: TBA

