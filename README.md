MSCS 634 Lab 5: Hierarchical and DBSCAN Clustering
Purpose
The purpose of this lab is to apply Agglomerative Hierarchical Clustering and DBSCAN to the Wine dataset from scikit-learn. The lab examines data preparation, feature standardization, cluster formation, parameter selection, visualization, and clustering evaluation.

Methods
The dataset contains 178 observations and 13 numerical features. The features were standardized using StandardScaler before clustering.

The following methods were applied:

Agglomerative Hierarchical Clustering with Ward linkage
DBSCAN with multiple eps and min_samples combinations
Principal Component Analysis for two-dimensional visualization
Dendrogram analysis for Hierarchical Clustering
The clustering results were evaluated using:

Silhouette Score
Homogeneity Score
Completeness Score
Key Results
Agglomerative Hierarchical Clustering produced three clusters and assigned every observation to a cluster. It achieved:

Silhouette Score: 0.2774
Homogeneity Score: 0.7904
Completeness Score: 0.7825
The selected DBSCAN model used eps = 1.5 and min_samples = 3. It produced eight clusters and classified 147 observations as noise. It achieved:

Silhouette Score: 0.3311
Homogeneity Score: 0.1892
Completeness Score: 0.2510
Although DBSCAN produced the higher Silhouette Score for its non-noise observations, Hierarchical Clustering provided the more representative overall result. It included all observations and corresponded more closely to the known Wine dataset classes.

Challenges and Decisions
A significant challenge was selecting suitable DBSCAN parameters. Different values of eps and min_samples substantially affected the number of clusters and noise observations. The selected DBSCAN model classified most observations as noise, demonstrating the algorithm's sensitivity to density parameters in a standardized, high-dimensional dataset.

The number of Hierarchical clusters was selected by comparing Silhouette Scores for cluster counts from two through six. PCA was used only for visualization, while both clustering algorithms were fitted using all 13 standardized features.

Repository Contents
MSCS_634_Lab_5.ipynb: Complete Jupyter Notebook containing the code, visualizations, results, and analysis
README.md: Overview of the lab, methods, findings, and challenges
