# crypto-clustering

![crypto](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/crypto.webp)

---

[Scaled Data](https://github.com/caitlin-hartley/crypto-clustering/blob/main/README.md#scaled-data)

[PCA Data](https://github.com/caitlin-hartley/crypto-clustering/blob/main/README.md#pca-analysis)

--- 

## Scaled Data

### Prepared Scaled Data
* Used the StandardScaler() module from scikit-learn to normalize the data from the CSV file
* Created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame
* Found the Best Value for k Using the Scaled DataFrame
* Used the elbow method to find the best value for k, which was 4

Scaled Data Elbow Curve:

![s_e](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/scaled_elbow.png)


### Clustered Cryptocurrencies with K-means Using the Scaled DataFrame

* Initialized the K-means model with the value of k as 4
* Fitted the K-means model using the scaled DataFrame
* Predicted the clusters to group the cryptocurrencies using the scaled DataFrame.

Scatter Plot of Clustered Cryptocurrencies using Scaled Data:

![s_c](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/scaled_cluster.png)


---

## PCA Analysis

### Optimize Clusters with Principal Component Analysis
* Using the original scaled DataFrame, performed a PCA and reduce the features to three principal components
* Retrieved the explained variance to determine how much information can be attributed to each principal component
* Use the elbow method on the scaled PCA DataFrame to find the best value for k, which was 4

PCA Elbow Curve:

![e_e](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/pca_elbow.png)

### Clustered Cryptocurrencies with K-means Using the PCA DataFrame

* Initialized the K-means model with the value of k as 4
* Fitted the K-means model using the PCA DataFrame
* Predicted the clusters to group the cryptocurrencies using the PCA DataFrame

Scatter Plot of Clustered Cryptocurrencies using PCA Data:

![e_c](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/pca_cluster.png)

---

### What is the impact of using fewer features to cluster the data using K-Means?

    The elbow curve for the PCA-transformed data shows a lower inertia value compared to the elbow curve for the original data. This suggests that reducing the number of features resulted in tighter clustering, with smaller within-cluster distances. A lower inertia indicates better clustering performance, with more compact groupings of data points within each cluster.

      In the scatter plot for the original scaled data, the clusters appear to overlap, with no clear separation between them. This implies that the original data, which contains more features, may not have effectively captured the underlying patterns necessary for optimal clustering. In contrast, the scatter plot for the PCA-transformed data shows distinct, non-overlapping clusters, with clear separations. Four well-defined clusters are visible, indicating that reducing the number of features helped to reduce noise and reveal clearer patterns in the data.

    Overall, using PCA to reduce the number of features had a positive impact on clustering the cryptocurrency data with K-Means. The reduction in features highlighted the important patterns while minimizing noise, leading to more distinct, meaningful, and separable clusters compared to the original data.
