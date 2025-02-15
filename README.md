# Comparing KNN and Logistic Regression on Student Data

_Read the full paper [here](https://github.com/Theosdoor/KNN-vs-Logistic-Regression/blob/main/Report.pdf)._

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methods](#methods)
  - [k-Nearest Neighbours (KNN)](#k-nearest-neighbours-knn)
  - [Logistic Regression (LR)](#logistic-regression-lr)
- [Results](#results)
- [Conclusion and Future Work](#conclusion-and-future-work)
- [References](#references)

## Introduction

Education is a cornerstone of society, influencing crime rates, economic growth, and civic engagement. However, high student drop-out and failure rates remain a concern. Efficiently allocating educational resources is crucial, and machine learning (ML) offers a promising approach to predict student performance and identify those in need of additional support.

This project compares two ML models—**k-nearest neighbours (KNN)** as a baseline and **logistic regression (LR)** as an alternative—by leveraging personal information and historical grades to predict student outcomes.

## Dataset

The dataset, based on Portuguese Language students, includes:

- **Personal Information:** Demographic and background data.
- **Academic Scores:** Two prior exam grades (G1, G2) and a final exam grade (G3).

A score of 10 or above on G3 is required to pass. This results in a binary classification task where the goal is to predict whether a student will pass (1) or fail (0) using 32 input features.

## Methods

### k-Nearest Neighbours (KNN)

KNN serves as the baseline model. Its performance heavily depends on:
- Preprocessing the data appropriately.
- Fine-tuning hyperparameters to optimize its performance.

### Logistic Regression (LR)

Logistic Regression is applied using the following approach:

- **Logit Function:** Computes the odds that an instance belongs to class 1.
- **Sigmoid Function:** Transforms the logit output into a probability \( p \) of being in class 1.
- **Decision Rule:** If \( p > 0.5 \), the instance is classified as pass (1); otherwise, it is classified as fail (0).
- **Parameter Estimation:** Parameters are determined using Maximum Likelihood Estimation (MLE).
- **Hyperparameter Tuning:** Achieved via k-fold cross-validation and an exhaustive grid search.

## Results

While KNN can perform well with proper preprocessing and parameter tuning, logistic regression generally:
- **Outperforms KNN:** Offers better generalization and is less prone to overfitting.
- **Handles Imbalanced Data:** More robust when the dataset size is small and classes are imbalanced.

**Limitations:**  
- The current dataset’s small size and imbalance hinder performance.  
- Future improvements should focus on addressing these issues for better accuracy.

## Conclusion and Future Work

In conclusion, logistic regression proves to be a robust method for predicting student performance. Future work could explore:
- **Data Augmentation:** Collecting a larger and more balanced dataset.
- **Feature Engineering:** Incorporating additional features or refining existing ones.
- **Model Exploration:** Experimenting with other classification algorithms and ensemble methods.

## References

1. **Cortez, P. & Gonçalves Silva, A. M. (2008).** _Using data mining to predict secondary school student performance_.
2. **Cortez, P. (2014).** _Student Performance_. UCI Machine Learning Repository. [DOI: 10.24432/C5TG7T](https://doi.org/10.24432/C5TG7T)
3. **Pedregosa, F., et al. (2011).** _Scikit-learn: Machine learning in Python._ *Journal of Machine Learning Research*, 12, 2825–2830.

