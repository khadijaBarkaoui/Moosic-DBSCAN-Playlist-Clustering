# Moosic — Spotify Playlist Clustering with DBSCAN

Exploring how machine learning can group songs by their audio features and support playlist creation at scale.

## About the Project

Moosic is a music startup that relies on music experts to create playlists. As its music catalogue grows, organising thousands of songs manually becomes increasingly difficult.

In this project, I explore whether unsupervised machine learning can help group songs based on their audio characteristics.

Using a dataset of approximately 5,000 songs, the project focuses on DBSCAN, a clustering algorithm that groups data points based on density.

The main question is:

**Can audio features help us group songs into meaningful playlists?**

## Project Goals

- Explore and prepare the Spotify audio features.
- Apply dimensionality reduction with Principal Component Analysis (PCA).
- Select suitable DBSCAN parameters using a k-distance graph.
- Analyse the resulting clusters and identify outliers.
- Visualise the clustering results with t-SNE.
- Evaluate whether the resulting groups make sense for playlist creation.

## Dataset

The dataset contains approximately 5,000 songs with audio features such as danceability, energy, acousticness, tempo, valence, loudness and instrumentalness.

These features describe different characteristics of a song and can be used to compare tracks numerically.

## Approach

### 1. Data Preparation

Inspect the dataset, check for missing values and duplicates, select relevant numerical features, and scale the data before clustering.

### 2. Dimensionality Reduction

Use PCA to reduce the number of dimensions while retaining as much information as possible.

### 3. DBSCAN Clustering

Explore different values of `eps` and `min_samples` to understand how they affect the number of clusters and the songs classified as noise.

### 4. Visualisation

Use t-SNE to project the clustering results into two dimensions and make their structure easier to inspect.

### 5. Evaluation

Examine songs within selected clusters and assess whether their audio characteristics and musical styles are sufficiently similar to support playlist creation.

## Tools and Technologies

- Python
- pandas and NumPy
- scikit-learn
- Matplotlib and Seaborn
- PCA, t-SNE and DBSCAN
- Jupyter Notebook

## Limitations

Audio features can describe aspects of a song, but they do not capture every factor that makes music similar to a human listener. Genre, lyrics, cultural context and personal preferences may also influence playlist quality.

The clustering results therefore need to be evaluated before the approach can be recommended for a real-world recommendation system.

## Next Steps

- Validate the clustering results.
- Compare DBSCAN with K-Means and Agglomerative Clustering.
- Evaluate cluster quality using quantitative metrics and musical examples.
- Explore listening behaviour and user feedback as additional sources of information.

## Project Status

Exploratory prototype. The final results and conclusions will be documented after the analysis has been reproduced and evaluated.
