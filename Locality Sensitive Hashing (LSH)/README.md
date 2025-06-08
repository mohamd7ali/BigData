# Locality Sensitive Hashing (LSH) for Big Data

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Results](#results)
8. [Visualization Examples](#visualization-examples)
9. [Contributing](#contributing)
10. [Author](#author)

## Overview

This project implements **Locality Sensitive Hashing (LSH)**, a technique for efficiently finding approximate nearest neighbors in large datasets. LSH is particularly useful for applications involving high-dimensional data, such as text similarity, image recognition, and recommendation systems.

The project demonstrates the use of LSH to identify similar articles in the **Arxiv Dataset**.

## Features

- **Data Preprocessing**: Includes cleaning, stopword removal, and normalization of text data.
- **K-Shingling**: Extracts overlapping substrings (shingles) of length `k` from text data to represent documents.
- **Min-Hashing**: Generates compact signatures for documents using hash functions to approximate Jaccard similarity.
- **Locality Sensitive Hashing**: Groups documents into buckets based on their Min-Hash signatures to identify candidate pairs for similarity comparison.
- **Similarity Computation**: Computes Jaccard similarity between candidate pairs to identify highly similar documents.
- **Visualization**: Provides heatmaps, network graphs, and other visualizations to analyze document similarities.

## Dataset

The project uses the **Arxiv Dataset**, which contains metadata and abstracts of research papers. The dataset is loaded as an RDD (Resilient Distributed Dataset) in PySpark for distributed processing.

## Methodology

1. **Initialization**:
   - Set up PySpark and load the dataset.
   - Perform initial exploration of the dataset.

2. **Preprocessing**:
   - Handle null values by removing or imputing missing data.
   - Remove stopwords using NLTK's English stopword list.
   - Clean text by removing punctuation, special characters, and extra spaces.

3. **K-Shingling**:
   - Extract shingles (substrings of length `k`) from the text.
   - Hash each shingle using MD5 for efficient storage and comparison.

4. **Min-Hashing**:
   - Generate random hash functions.
   - Compute Min-Hash signatures for each document.

5. **Locality Sensitive Hashing**:
   - Divide Min-Hash signatures into bands and hash each band into buckets.
   - Group documents in the same bucket as candidate pairs.

6. **Similarity Computation**:
   - Compute Jaccard similarity for candidate pairs.
   - Filter pairs based on a similarity threshold.

7. **Visualization**:
   - Generate heatmaps and network graphs to visualize document similarities.

## Installation

1. Install Python dependencies:
   ```bash
   pip install pyspark numpy pandas matplotlib seaborn networkx plotly nltk wordcloud
   ```

2. [Download the Arxiv Dataset](https://drive.google.com/file/d/1-EhpZaY5gvbgNuEU5IskmlQ0EnNAG5cu/view?usp=drive_link) and place it in the appropriate directory:
   ```
   /home/linux/BigData/Dataset/Arxiv-Dataset.json
   ```

3. Initialize PySpark:
   ```python
   import findspark
   findspark.init()
   ```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/mohamd7ali/BigData.git
   cd "BigData/Locality Sensitive Hashing (LSH)"
   ```

2. Run the notebook `LSH.ipynb` using Jupyter Notebook or VSCode.

3. Follow the steps in the notebook to preprocess the data, compute Min-Hash signatures, and apply LSH.

4. Visualize the results using the provided plots and graphs.

## Results

- **First Results**: Using 10% of the dataset, the average abstract length and candidate pairs are computed.
- **Second Results**: Using 30% of the dataset, the effect of LSH parameters (bands and rows per band) is analyzed.
- **Similarity Analysis**: Articles similar to specific IDs are identified and visualized.

## Visualization Examples

- **Heatmap**: Displays similarity scores between articles.
- **Network Graph**: Represents articles as nodes and similarities as weighted edges.
- **Chord Diagram**: Illustrates connections between similar articles.

## Contributing
Contributions are welcome! Feel free to fork the repository and submit pull requests for improvements or new features.

## Author
- **Mohammad Ali Etemadi Naeen**

