# Big Data PySpark Projects
This repository contains a collection of big data projects implemented using PySpark. They focus on large-scale data processing, clustering, recommendation systems, real-time streaming, and text analysis. Each project is designed to solve a real-world data problem using scalable distributed computing techniques.

## Projects

### 1. [Arxiv Article Dataset Analysis](./Arxiv_RDD_Analysis/)
Preprocessing and exploratory data analysis on a dataset of Arxiv research articles. Includes:
- Counting articles per category
- Analyzing the number of authors per paper
- Filtering papers with a high number of authors
- Distribution of publications by year
- Identifying articles containing specific keywords

### 2. [Frequent Trigram Mining with Apriori and PCY](./Apriori_PCY_Frequent_Trigram/)
Mining the most frequent 3-word phrases (trigrams) in the Arxiv dataset using two popular algorithms:
- Apriori
- PCY (Park–Chen–Yu)

Includes evaluation of performance and memory usage.

### 3. [Article Similarity Search with Locality Sensitive Hashing (LSH)](./Locality%20Sensitive%20Hashing%20%28LSH%29/)
Implementation of the Locality-Sensitive Hashing (LSH) algorithm for finding similar articles based on their textual content. Given the ID of an article, the system retrieves a list of similar articles along with their similarity scores.

### 4. [Book Recommendation System (Collaborative Filtering)](./Book_Recommendation_System/)
A collaborative filtering-based recommendation engine using PySpark. The system analyzes user ratings of books and recommends books that a user is likely to enjoy.

### 5. [Geospatial Clustering and Dimensionality Reduction](./project-05-clustering-dim-reduction/)
Clustering and visualization of high-dimensional geographic data using:
- **PCA** (Principal Component Analysis)
- **UMAP** (Uniform Manifold Approximation and Projection)
- **BFR** (Bradley–Fayyad–Reina Clustering Algorithm)

Clustering quality is evaluated using:
- Silhouette Score
- Davies-Bouldin Index

### 6. [Real-Time News Stream Processing](./project-06-streaming-news-processor/)
A streaming application using PySpark's Structured Streaming to process incoming real-time news data from various categories. The system extracts and aggregates key information from live news feeds.

### 7. [Streaming Analysis with DGIM and FM Algorithms](./project-07-streaming-dgim-fm/)
Stream analysis using two approximate algorithms:
- **DGIM** (Datar-Gionis-Indyk-Motwani): Estimates the number of successful user requests over sliding time windows.
- **Flajolet-Martin (FM)**: Estimates the number of unique users visiting a website using multiple hash functions.

### 8. [Graph Algorithms: PageRank and HITS](./project-08-graph-algorithms/)
Implementation of:
- **PageRank**: Ranks nodes in a directed graph based on link structure.
- **HITS (Hyperlink-Induced Topic Search)**: Identifies hubs and authorities in the graph.

Both algorithms are tested and visualized on sample graph datasets.

---

## Technologies Used

- Python 3.x
- PySpark
- Apache Spark
- Structured Streaming
- MLlib
- NumPy, Pandas, Matplotlib (for preprocessing and evaluation)
- Jupyter / Google Colab

---

## Getting Started

Each project contains its own folder with a dedicated `README.md`, source code, and sample data or instructions for usage. You can run the scripts using:

```bash
spark-submit your_script.py
```

## Author

    Mohammad Ali Etemadi Naeen
