# Lab 3: Clustering Analysis Using K-Means and K-Medoids

## Purpose

The purpose of this lab was to explore and compare K-Means and K-Medoids using the Wine dataset. This involved applying both algorithms, evaluating the quality of clustering using metrics such as Silhouette Score and Adjusted Rand Index (ARI), and visualizing the cluster structures using PCA. 

## Key Insights

- K-Means produced better-defined more compact clusters in this dataset with higher Silhouette and ARI scores. This is expected since K-Means is well-suited for evenly distributed data.
- K-Medoids was more robust to outliers by selecting actual data points as cluster centers. However, its cluster boundaries were less distinct in this case, and a few samples appeared misclassified.
- The PCA-based visualizations clearly showed the differences in cluster shapes and centroids vs. medoids positioning.


## Challenges and Decisions

- The scikit-learn-extra library caused compatibility issues due to a numpy binary mismatch error. To resolve this, the pyclustering library was used as an alternative for implementing K-Medoids.
- Choosing appropriate medoid indices for initialization required a random sampling strategy, which introduced slight variability in results.
- Visualizing high-dimensional data was handled using PCA which preserved major variance directions and allowed clear side-by-side plots.



