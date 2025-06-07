# Arxiv RDD Analysis

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
  - [Dataset Link](#dataset-link)
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [Author](#author)

## Overview
This project focuses on analyzing the Arxiv article dataset using PySpark and RDDs (Resilient Distributed Datasets). It demonstrates various data preprocessing, exploration, and visualization techniques applied to massive datasets. The goal is to extract meaningful insights from the dataset, such as identifying trends, frequent words, and category distributions.

## Features
- **Dataset Preprocessing**: Cleaning and preparing the dataset by removing null values, stopwords, and irrelevant characters.
- **Data Exploration**:
  - Count articles in each category.
  - Identify the category with the most articles.
  - Analyze the distribution of authors per article.
  - Filter articles based on specific criteria (e.g., number of authors).
- **Time Series Analysis**: Plot the number of articles submitted per year.
- **Text Analysis**:
  - Extract the top 20 most frequent words in abstracts.
  - Generate a word cloud visualization for frequent words.
- **Advanced Exploration**:
  - Find articles containing specific keywords (e.g., "algorithm").
  - Analyze word counts in abstracts and sort articles by abstract length.

## Dataset
The dataset used in this project is the Arxiv article dataset, which contains metadata about articles, including titles, abstracts, authors, categories, and submission dates.

### Dataset Link
[Download the Arxiv Dataset](https://drive.google.com/file/d/1-EhpZaY5gvbgNuEU5IskmlQ0EnNAG5cu/view?usp=drive_link)

## Requirements
To run this project, ensure you have the following installed:
- Python 3.x
- PySpark
- Findspark
- NLTK
- Matplotlib
- WordCloud

Install the required Python libraries using:
```bash
pip install pyspark findspark matplotlib wordcloud nltk
```

## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/mohamd7ali/BigData.git
   cd BigData/Arxiv_RDD_Analysis
   ```
2. Install dependencies as mentioned above.
3. Download the dataset and place it in the appropriate directory (`/content/Dataset`).

## Usage
1. Open the notebook file `Arxiv_RDD_Analysis.ipynb` in your preferred editor (e.g., VS Code or Jupyter Notebook).
2. Follow the step-by-step instructions in the notebook to preprocess, explore, and analyze the dataset.
3. Run the cells to generate visualizations and insights.

## Results
- **Category Analysis**: Distribution of articles across categories.
- **Author Analysis**: Insights into the number of authors per article.
- **Time Series**: Trends in article submissions over the years.
- **Text Analysis**: Frequent words and their visual representation using word clouds.

## Contributing
Contributions are welcome! Feel free to fork the repository and submit pull requests for improvements or new features.

## Author
- **Mohammad Ali Etemadi Naeen**