# CS5691 – Pattern Recognition and Machine Learning

## This repository contains the programming assignments, source code, and technical reports for the course CS5691: Patern Recognition and Machine Learning.
---

## Assignment 1 — Regression

**`PRML_Q1.ipynb` — Weighted Least Squares (WLS)**
- Fits OLS and WLS with their closed-form solutions. WLS uses a diagonal weight matrix built from each observation's noise variance.
- Compares the learned parameters of the two models.
- Plots residuals against the input for both models, on the train and test data.
- Shows scatter plots of predicted vs. actual output, and overlays the OLS and WLS regression lines.

**`PRML_Q2.ipynb` — Ridge Regression**
- Splits the training data into train and validation sets.
- Finds a polynomial degree where OLS overfits.
- Implements closed-form ridge regression and tunes λ on a log-spaced grid using validation MSE.
- Plots MSE against λ and reports train and test MSE for OLS and for the best ridge model.
- Shows scatter plots of predicted vs. actual output for the best model.

---

## Assignment 2 — Clustering

**`PRML_Q1.ipynb` — Fuzzy C-Means (FCM)**
- Implements FCM with K = 3 and fuzzifier m = 1.618.
- Shows a color-blended scatter plot, where each point's color reflects its membership in each cluster.
- Compares results for m = 1.1, 3.14 and 5.0, showing that cluster assignments become less certain as m increases.
- Compares FCM and K-Means centroids to check whether overlapping clusters pull the K-Means centroids closer together.

**`PRML_Q2.ipynb` — DBSCAN**
- Implements DBSCAN from scratch: a distance function, an ε-neighbourhood query, cluster expansion, and a function that labels each point as Core, Border or Noise.
- Clusters with ε = 0.4 and MinPts = 7, drawing an ε-circle around one representative core point in each cluster.
- Sweeps ε over [0.1, 1.5] and plots the number of clusters and the noise ratio against ε.
- Checks whether shuffling the data order changes the result (with ε = 0.35 and MinPts = 8); any change comes from border points.
- Compares the DBSCAN output with K-Means.

---

## Assignment 3 — Classification

**`PRML_Q1.ipynb` — Logistic Regression**
- Implements binary cross-entropy loss with gradient descent and early stopping (tolerance 10⁻⁴, at most 500 epochs).
- Plots loss against epochs for learning rates from 1 to 0.0001, and reports train and test accuracy for each.
- Plots the decision boundary and the confusion matrix for the best learning rate.

**`PRML_Q2.ipynb` — Decision Tree: Football Match Outcome Prediction** *(Question 3 in the assignment)*
- Implements a decision tree using entropy and information gain, with midpoint threshold search for continuous features.
- Reports train and test accuracy and prints the learned tree structure.
- Tunes max depth, with plots of train and validation accuracy against depth and of leaf count against depth.
- Applies Reduced Error Pruning and compares the full, depth-limited and pruned trees.
