# wheat seeds clustering — Unsupervised Machine Learning
## Project Overview

This project explores whether unsupervised machine learning can identify meaningful groups of wheat seeds without using their known variety labels during clustering.

It was completed as part of the Machine Learning with Python Erasmus+ course.

## Dataset

The Seeds dataset contains 210 wheat kernels from three varieties, described by seven geometric measurements: area, perimeter, compactness, kernel length, kernel width, asymmetry, and groove length.

## Methodology

The analysis includes:

- StandardScaler to standardize the seven features.

- Principal Component Analysis (PCA) for two-dimensional visualization.

- K-Means clustering to identify groups without using the true labels.

- Elbow Method and Silhouette Score to select the number of clusters.

- Cross-tabulation and purity score to evaluate the clustering against the real varieties.

## Results

The Elbow Method suggested three clusters, while the Silhouette Score was highest for two clusters. I selected K=3 based on the elbow and the approximate structure observed in the initial PCA plot.

The resulting purity score was 0.919, with 193 out of 210 seeds belonging to the dominant variety in their assigned cluster. Variety 2 was separated most clearly, while varieties 1 and 3 showed more overlap.

## Limitations

The choice of K is not definitive because the clustering diagnostics disagreed. Also, although the PCA visualization preserves approximately 89% of the total variance, it cannot fully represent the clustering performed using all seven scaled features.

## Reflection

This project helped me understand how clustering can reveal structure without relying on predefined labels. One challenge was choosing the number of clusters when the Elbow Method and Silhouette Score gave different indications.

With more time, I would explore additional clustering methods and compare their results.

## Tools

Python, NumPy, pandas, Matplotlib, scikit-learn, Google Colab.

## Project Notebook

The completed Jupyter notebook is available in this repository, including the code, visualizations, results, and written interpretations.
