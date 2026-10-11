# wheat seeds clustering — Unsupervised Machine Learning
## Project Overview

This project explores whether unsupervised machine learning can identify meaningful groups of wheat seeds without using their known variety labels during clustering.

It was completed as part of the Machine Learning with Python Erasmus+ course.

## Dataset

The Seeds dataset contains 210 wheat kernels from three varieties, described by seven geometric measurements: area, perimeter, compactness, kernel length, kernel width, asymmetry, and groove length.

## Tools

Python, NumPy, pandas, Matplotlib, scikit-learn, Google Colab.

## Methodology

The analysis includes:

- StandardScaler to standardize the seven features.

- Principal Component Analysis (PCA) for two-dimensional visualization.

- K-Means clustering to identify groups without using the true labels.

- Elbow Method and Silhouette Score to select the number of clusters.

- Cross-tabulation and purity score to evaluate the clustering against the real varieties.

## Results

The Elbow Method showed a clear decrease in inertia up to K=3, followed by a more gradual improvement for higher values of K. On the other hand, the Silhouette Score was highest for K=2 (0.466), but the score for K=3 (0.401) was not much lower. Considering the more noticeable elbow around K=3, the relatively small numerical difference between the two silhouette scores and the three approximate groups observed in the initial PCA plot, I decided to choose K=3.

The resulting purity score was 0.919, with 193 out of 210 seeds belonging to the dominant variety in their assigned cluster. Variety 2 was separated most clearly, while varieties 1 and 3 showed more overlap.

## Limitations

Although the results show a good agreement with the actual wheat varieties, the clusters do not match them perfectly.

The choice of K is not completely certain because the Elbow Method and Silhouette Score suggested different values. Also, the PCA plot shows only two dimensions, explaining approximately 89% of the variance, while K-Means used all seven scaled features.

Therefore, the PCA visualization cannot show the full structure of the clustering.

## Reflection

This project helped me understand how clustering can reveal patterns in data without using predefined labels. One thing that worked well was that K-Means recovered much of the real variety structure, as shown by the purity score of 0.919.

Although I expected choosing the number of clusters to be the most challenging part, I actually found writing and understanding the Python code more difficult, especially when trying to connect the different steps of the analysis. Working through the notebook step by step helped me better understand how these methods are applied in practice.

With more time, I would like to improve my Python programming skills and become more confident in implementing machine learning methods independently. I would also like to explore other clustering algorithms and compare their results.

## Project Notebook

The completed Jupyter notebook is available in this repository, including the code, visualizations, results, and written interpretations.
