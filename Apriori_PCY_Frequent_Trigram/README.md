# Frequent Trigram Mining with A-Priori and PCY Algorithms

## Table of Contents
1. [Overview](#overview)
2. [Algorithms Used](#algorithms-used)
   - [A-Priori Algorithm](#a-priori-algorithm)
   - [PCY Algorithm](#pcy-algorithm)
3. [Dataset](#dataset)
4. [Project Structure](#project-structure)
5. [Installation](#installation)
   - [Prerequisites](#prerequisites)
   - [Steps](#steps)
6. [Usage](#usage)
   - [Running the Notebook](#running-the-notebook)
   - [Key Outputs](#key-outputs)
7. [Evaluation](#evaluation)
   - [Jaccard Index](#jaccard-index)
8. [Conclusion](#conclusion)
9. [Author](#author)

## Overview

This project focuses on mining frequent trigram patterns from large datasets using two algorithms: **A-Priori** and **PCY**. It demonstrates the application of these algorithms for massive data mining tasks, evaluates their performance, and compares their results using the **Jaccard Index**.

### Key Features:
- **A-Priori Algorithm**: A classical approach for frequent itemset mining, suitable for small to medium datasets.
- **PCY Algorithm**: An optimized version of A-Priori, designed for large datasets with memory-efficient techniques.
- **Jaccard Index Evaluation**: Measures the similarity between the results of the two algorithms.

---

## Algorithms Used

### A-Priori Algorithm
- Iterative process to identify frequent itemsets.
- Prunes infrequent candidates early to reduce computational overhead.
- Suitable for smaller datasets or exploratory analysis.

### PCY Algorithm
- Uses hashing and bitmaps to reduce memory usage.
- Scales better for larger datasets.
- Employs bucket filtering to minimize the number of candidates.

---

## Dataset

The project uses the **Arxiv-Dataset.json**, which contains abstracts of research articles. The dataset is preprocessed to remove stopwords, irrelevant characters, and null values before applying the algorithms.

---

## Project Structure

- **Apriori_PCY_Frequent_Trigram.ipynb**: Contains the implementation of both algorithms, preprocessing steps, and visualization of results.
- **Description_of_Algorithms.ipynb**: Provides detailed explanations of the algorithms, their advantages, limitations, and hyperparameters.
- **README.md**: Project documentation.

---

## Installation

### Prerequisites
- Python 3.8 or higher
- Apache Spark
- Required Python libraries:
  - `pyspark`
  - `nltk`
  - `matplotlib`
  - `wordcloud`
  - `pandas`
  - `numpy`
  - `seaborn`
  - `plotly`

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/mohamd7ali/BigData.git
   cd BigData/Apriori_PCY_Frequent_Trigram
   ```

2. Install dependencies.

3. Initialize PySpark:
   ```python
   import findspark
   findspark.init()
   ```

---

## Usage

### Running the Notebook
1. Open `Apriori_PCY_Frequent_Trigram.ipynb` in Jupyter Notebook or VSCode.
2. Follow the steps to preprocess the dataset, apply the algorithms, and visualize the results.

### Key Outputs
- Frequent trigram patterns identified by A-Priori and PCY.
- Visualizations:
  - Bar charts
  - Word clouds
  - Pie charts
  - Treemaps
- Jaccard Index evaluation.

---

## Evaluation

### Jaccard Index
The similarity between the results of A-Priori and PCY is evaluated using the Jaccard Index:
- **True Positives (TP)**: Trigrams identified by both algorithms.
- **False Positives (FP)**: Trigrams identified by PCY but not A-Priori.
- **False Negatives (FN)**: Trigrams identified by A-Priori but missed by PCY.

---

## Conclusion

This project demonstrates the effectiveness of A-Priori and PCY algorithms for frequent trigram mining. While A-Priori is simpler and suitable for smaller datasets, PCY excels in scalability and memory efficiency for larger datasets. The Jaccard Index provides a robust metric for comparing their results.

---

## Author
- **Mohammad Ali Etemadi Naeen**

