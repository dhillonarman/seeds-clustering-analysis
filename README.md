# seeds-clustering-analysis

🌾 Seeds Dataset Clustering Analysis
This project performs unsupervised clustering on the Seeds dataset from the UCI Machine Learning Repository using various preprocessing techniques and clustering algorithms. The goal is to evaluate how preprocessing impacts clustering performance and determine the best approach.

📚 Dataset Information
📌 Dataset: Seeds Dataset - UCI ML Repository

📈 Number of Features: 7

🧬 Feature Names:

area

perimeter

compactness

length

width

asymmetry

groove

🔢 Number of Instances: 210

🎯 Target Column: class (Not used in clustering)

🛠️ Clustering Algorithms Used
KMeans

Agglomerative Clustering (Hierarchical)

MeanShift

⚙️ Preprocessing Techniques Explored
none (raw data)

normalize (StandardScaler)

transform (PowerTransformer)

pca (PCA after StandardScaler)

t+n (PowerTransformer followed by StandardScaler)

t+n+pca (PowerTransformer → StandardScaler → PCA)

🧪 Evaluation Metrics
Silhouette Score

Calinski-Harabasz Index

Davies-Bouldin Index

🥇 Best Result Summary

Algorithm	Preprocessing	Clusters	Silhouette Score
MeanShift	none	3	0.518287
MeanShift without any preprocessing yielded the highest silhouette score.

📊 Result Graphs
Three performance graphs are generated and saved:

seeds_silhouette.png

seeds_calinski_harabasz.png

seeds_davies_bouldin.png

These compare different algorithms and preprocessing methods with respect to evaluation metrics.

Example (Silhouette Score vs Clusters):



🧾 Output Table (Sample)
The complete results were saved in a CSV file: seeds_clustering_results.csv

Example row:


Algorithm	Preprocessing	Clusters	Silhouette	Calinski-Harabasz	Davies-Bouldin
KMeans	t+n+pca	3	0.405547	236.82	0.955
📁 Files in Repository
seeds_clustering.ipynb → Complete clustering and evaluation code

seeds_clustering_results.csv → Tabular result of all runs

seeds_silhouette.png → Silhouette score comparison

seeds_calinski_harabasz.png → CH index comparison

seeds_davies_bouldin.png → DB index comparison

README.md → Project documentation

✅ Conclusion
The MeanShift algorithm with no preprocessing achieved the best clustering performance on the Seeds dataset, with a silhouette score of 0.518.

Preprocessing and PCA sometimes improved KMeans and Hierarchical results, but not always.

The dataset is well-suited to 3-cluster separation, matching the actual number of classes.
