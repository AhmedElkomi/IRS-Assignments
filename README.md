# Intelligent Recommender Systems - Neighborhood CF Models (User-based and Item-based CF)

## Overview
This Assignment is part of the *AIE425 Intelligent Recommender Systems* course assignments, focusing on building and evaluating neighborhood-based collaborative filtering (CF) models. These models are designed to generate personalized recommendations by analyzing user and item similarities.

In this assignment, both **User-based CF** and **Item-based CF** approaches are implemented, utilizing **Cosine Similarity** and **Pearson Correlation** as similarity measures. The performance of each approach is evaluated using **Root Mean Square Error (RMSE)** and **Mean Absolute Error (MAE)**, which provide insights into prediction accuracy.

## Project Structure

- Data Collection: Data is collected from a chosen source, preprocessed, and transformed into a user-item rating matrix.
- User-Based CF: Recommends items by identifying users with similar preferences.
- Item-Based CF: Recommends items based on similarities between items.
- Evaluation Metrics: RMSE and MAE are used to measure prediction accuracy.

## Requirements

- Python 3.8+
- Libraries:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `scipy`
  - `seaborn`
  - `matplotlib`
  - `beutiful soup`


## Dataset

The dataset consists of user-item ratings on a scale of 1 to 5, representing each user’s rating of different products. The data was collected through web scraping from [Amazon](https://www.geeksforgeeks.org/scraping-amazon-product-information-using-beautiful-soup/), which provided product names, ratings, ratings count, and availability status.

## Models Implemented

1. User-Based Collaborative Filtering
   - Finds a peer group for each target user based on **Cosine Similarity** and **Pearson Correlation**.
   
2. Item-Based Collaborative Filtering
   - Finds similar items based on user ratings using **Cosine Similarity** and **Pearson Correlation**.

## Results

### Accuracy Metrics
Each model was evaluated using RMSE and MAE, calculated as follows:

| Model                      | RMSE   | MAE   |
|----------------------------|--------|-------|
| **User-Based CF (Cosine)** | 1.11   | 0.93  |
| **User-Based CF (Pearson)**| 1.05   | 0.84  |
| **Item-Based CF (Cosine)** | 1.17   | 0.99  |
| **Item-Based CF (Pearson)**| 1.74   | 1.46  |

Performance Summary
- User-Based CF (Pearson) showed the best performance with the lowest error rates, suggesting it effectively captures user preferences in this dataset.
- Item-Based CF (Pearson) performed the least accurately, with a relatively high RMSE and MAE.

Usage

1. Preprocess Data: Clean and structure your dataset to form a user-item matrix.
2. Run Models: Execute the User-based and Item-based CF models using `cosine` and `pearson` similarity.
3. Evaluate: Use RMSE and MAE to assess each model’s performance.


Future Enhancements

- Hybrid Recommender: Integrate content-based filtering for improved performance.
- Hyperparameter Tuning: Experiment with different similarity thresholds to improve accuracy.
