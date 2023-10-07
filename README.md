# Multi-criteria-Recommender-system
# Aggregation Function based DeepFM & SVD++
This project focuses on building a recommendation system that integreates both DeepFM and SVD++ models. The DeepFM model predicts the overall user-item interaction based on the SVD++ predicted individual criterion ratings.
In other words, we leverage the combination of DeepFM and SVD++ to build a multi-criteria recommendation system that first predicts individual criteria and then aggregates them for an overall rating prediction.

# Table of Contents
- Overview
  -  Dataset
- Getting Started
  - Dependencies
  - Usage
- Methodology
  - DeepFM
  - SVD++
- Results
- Acknowledgements
# Overview
This project offers an innovative approach to building multi-criteria recommendation systems by fusing the strengths of both DeepFM and SVD++ models. By predicting individual criteria through SVD++ and subsequently using DeepFM to aggregate these for an overall rating prediction, the model achieves superior recommendation accuracy.
Our approach is three-pronged:
- Use SVD++ to predict individual criterion ratings.
- Aggregate these ratings using DeepFM to predict the overall user-item interaction.
- Predict the Top-N recommendation for each user.
  # Dataset
  The Yahoo Movies dataset was utilized for this project. The Yahoo Movies dataset is a multi-criteria rating dataset wherein users provide ratings for movies based on four distinct movie criteria: direction (cr1), action (cr2), story (cr3), and visuals (cr4), alongside an overall rating (cr0). Each criterion's ratings were gauged on a transformed scale of 1 to 13, initially gathered in a letter-grade format ranging from A+ to F—with A+ denoting the highest preference and F, the lowest. This dataset encompasses 62,156 ratings from 6,078 users across 976 movies, revealing a rating sparsity of 99.0%.

  
# Getting Started
  # Dependencies
  - Python 3.x
  - TensorFlow 2.x
  - Scikit-learn
  - Pandas
  - Numpy
  - Surprise
  # Usage
  - Run the main Python script to execute both the DeepFM and SVD++ models.

# Methodology
-  DeepFM
   DeepFM combines factorization machines for recommendation and deep learning for feature learning. The embeddings for user and item IDs, along with other criteria, are learned using this model to predict the overall rating.

-  SVD++
   SVD++ is a matrix factorization technique extended to incorporate implicit feedback. In this project, it specializes in predicting individual criteria such as 'Cr1', 'Cr2', 'Cr3', and 'Cr4'.
-  Top-N Recommendation
   The top N recommendations for each user will be generated based on the aggregated prediction.
# Results
After executing the script, we evaluated the recommendation's accuracy and performance based on the top-N recommendation task. We used different evaluation metrics to measure the rating prediction accuracy, usage prediction, and ranking accuracy such as RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), Recall, Precision, F-Measure, Mean Average Precision (MAP), Area Under the Curve (AUC) and Fraction of Concordant Pairs (FCP).

Acknowledgements
This project was made possible through the use of several open-source libraries and frameworks, including TensorFlow and Surprise.
