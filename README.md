# crypto-clustering

![crypto](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/crypto.webp)

---

[Scaled Data]

[PCA Data]

[Conclusion]

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

![e_e](pca_elbow.png)

### Clustered Cryptocurrencies with K-means Using the PCA DataFrame

* Initialized the K-means model with the value of k as 4
* Fitted the K-means model using the PCA DataFrame
* Predicted the clusters to group the cryptocurrencies using the PCA DataFrame

Scatter Plot of Clustered Cryptocurrencies using PCA Data:

![e_c](https://github.com/caitlin-hartley/crypto-clustering/blob/main/images/pca_cluster.png)

---

### What is the impact of using fewer features to cluster the data using K-Means?
