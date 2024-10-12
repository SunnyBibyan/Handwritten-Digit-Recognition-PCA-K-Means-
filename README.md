# Handwritten Digit Recognition Using PCA and K-Means Clustering

## Overview

This project demonstrates a machine learning pipeline to recognize handwritten digits from the MNIST dataset using **Principal Component Analysis (PCA)** for dimensionality reduction and **K-Means Clustering** for grouping similar digits. The project also incorporates **t-SNE** for visualizing the clusters in 2D space.

The goal is to reduce the high-dimensional pixel data to lower dimensions for effective clustering, without relying on digit labels, and to visualize how well the clustering algorithm performs.

## Project Workflow

1. **Data Loading and Preprocessing**: 
   - The MNIST dataset is loaded using `fetch_openml()`.
   - Features are standardized to ensure effective dimensionality reduction.

2. **Dimensionality Reduction Using PCA**:
   - PCA is applied to reduce the 784-dimensional dataset to 50 components.
   - The reduced features retain the majority of variance in the data and remove noise.

3. **Clustering Using K-Means**:
   - K-Means is applied to the reduced features to form 10 clusters, corresponding to the 10 possible digit classes (0-9).
   - A confusion matrix is generated to compare true digit labels with cluster assignments.

4. **Visualization Using t-SNE**:
   - t-SNE is employed to visualize the clusters in a 2D space, making it easier to interpret how well the clustering worked.


## Results

The following visualizations provide insight into the performance of the K-Means clustering algorithm on PCA-reduced MNIST data:

### Confusion Matrix

The confusion matrix compares the true labels of the digits with the predicted clusters, giving an indication of how well the clustering algorithm is grouping the digits.

### t-SNE Visualization

This 2D scatter plot generated using t-SNE shows how the clusters of digits form in a lower-dimensional space. Each point represents a digit, and similar digits are grouped together.

## Key Learnings

- **Dimensionality Reduction**: PCA can significantly reduce the dimensionality of large datasets while preserving most of the data variance. This helps in speeding up the computation and removing noise from the data.
- **Unsupervised Learning**: K-Means clustering, despite being unsupervised, can effectively group similar data points (in this case, digits) based on their features.
- **Visualization**: t-SNE helps in visualizing high-dimensional data, making it easier to interpret the results of clustering.

## Future Work

- Experiment with more components in PCA to fine-tune dimensionality reduction.
- Try different clustering algorithms such as DBSCAN or Agglomerative Clustering.
- Apply deep learning models like Convolutional Neural Networks (CNNs) for comparison with unsupervised methods.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.






