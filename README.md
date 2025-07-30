# Week 8 - K-Nearest Neighbors

This notebook focuses on using the K-Nearest Neighbors (KNN) regression algorithm to predict hospital length of stay (LOS). The main goal was to find the best model through tuning and experimentation, and to evaluate how well KNN performs on unseen data.

- Loaded and cleaned the dataset, including fixing a categorical feature (`rcount`) and removing irrelevant columns.
- Encoded categorical variables and standardized the features.
- Built a baseline KNN model with `k=5`, achieving an RMSE of 1.14 and an R² of 0.77.
- Iterated over a range of `k` values (1–30) to explore their effect on RMSE.
- Used `GridSearchCV` to tune hyperparameters:
  - `n_neighbors` (1 to 20)
  - `weights` (`uniform` vs. `distance`)
  - `p` (1 = Manhattan, 2 = Euclidean)

##  Results

- The best performing model used:
  - `n_neighbors = 8`
  - `p = 1` (Manhattan distance)
  - `weights = distance`
- Final RMSE: **1.11**
- Final R²: **0.78**

##  Conclusion

Tuning the KNN model improved performance from the baseline. Manhattan distance with distance-based weighting led to the most accurate predictions. KNN turned out to be a solid option for this regression task, especially when properly tuned.
