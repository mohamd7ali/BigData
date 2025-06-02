# Book Recommendation System

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Dataset](#dataset)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Results](#results)
8. [Future Improvements](#future-improvements)
9. [Project Structure](#project-structure)
10. [Author](#author)

## Overview
This project implements a **Book Recommendation System** using **Big Data** techniques. It leverages **Apache Spark** for distributed data processing and machine learning algorithms to predict user ratings and recommend books. The system is designed to handle large-scale datasets efficiently and provide accurate recommendations.

## Features
- **Data Preprocessing**: Cleans and transforms raw data, including handling duplicates, null values, and filtering ratings.
- **Sampling**: Extracts subsets of data for efficient computation while preserving diversity in books and users.
- **Feature Extraction**: Computes book features based on user ratings for similarity calculations.
- **Similarity Calculation**: Uses **Pearson Correlation Coefficient** to measure similarity between books.
- **Rating Prediction**: Predicts user ratings for books using collaborative filtering techniques with bias adjustments.
- **RMSE Calculation**: Evaluates model accuracy using **Root Mean Squared Error (RMSE)**.
- **Recommendation**: Recommends books to users based on predicted ratings.
- **Evaluation File Completion**: Fills missing ratings in evaluation files with predicted scores.

## Technologies Used
- **Apache Spark**: Distributed data processing and machine learning.
- **Python**: Core programming language for implementation.
- **Pandas**: Data manipulation and analysis.
- **Seaborn & Matplotlib**: Data visualization.
- **NetworkX**: Graph-based analysis.
- **Numpy**: Numerical computations.

## Dataset
The system uses a dataset containing user ratings for books. Each record includes:
- `user_id`: Unique identifier for the user.
- `book_id`: Unique identifier for the book.
- `rating`: User's rating for the book (scale: 1 to 5).
- `timestamp`: Time of the rating.

## Installation
1. Install Python dependencies:
   ```bash
   pip install pyspark findspark pandas matplotlib seaborn networkx nltk wordcloud
   ```
2. Ensure **Java 8** is installed for Apache Spark:
   ```bash
   sudo apt install openjdk-8-jdk-headless
   ```
3. Mount Google Drive (if using Colab):
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

## Usage
1. **Preprocessing**:
   - Load the dataset and clean it.
   - Rename columns and filter ratings within the valid range (1 to 5).

2. **Sampling**:
   - Extract top books and users based on activity.
   - Save sampled data for further processing.

3. **Feature Extraction**:
   - Compute book features based on user ratings.
   - Generate hash values for features.

4. **Similarity Calculation**:
   - Compute similarity between books using Pearson Correlation Coefficient.

5. **Rating Prediction**:
   - Predict user ratings for books using collaborative filtering with bias adjustments.

6. **RMSE Calculation**:
   - Evaluate model accuracy using RMSE.

7. **Recommendation**:
   - Recommend books to users based on predicted ratings.

8. **Evaluation File Completion**:
   - Fill missing ratings in evaluation files with predicted scores.

## Results
- **RMSE**: Achieved a final RMSE of **0.863**, indicating high accuracy in predictions.
- **Recommendations**: Provides personalized book recommendations for users.

## Future Improvements
- **Weight Normalization**: Enhance similarity impact by normalizing weights.
- **Regularization**: Reduce overfitting by adding regularization terms to bias calculations.
- **Scalability**: Optimize algorithms for larger datasets.

## Project Structure
```
├── data/
│   ├── BookRates_DS.csv
│   ├── sampled_dataset.csv
│   ├── Evaluate_P2.csv
├── output/
│   ├── Evaluation_P2_Completed.csv
├── book_recommendation_system.ipynb
├── README.md
```

## Author
- **Mohammad Ali Etemadi Naeen**
