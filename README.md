# Comparing KNN and Logistic Regression on Student Data

_Read the paper [here](https://github.com/Theosdoor/KNN-vs-Logistic-Regression/blob/main/Report.pdf)._

Education is a key part of society, A high education level of a country is well-known to indicate lower crime, faster economic growth and greater civic engagement. It's also essential to individual lives, for both personal and economic reasons. Despite this, many societies grapple with high student drop-out and failure rates. One reason for this is a lack of resources and support for struggling students.

As such, it is vital that educators use these resources optimally, typically targeting the students needing the most help first. In this way, machine learning (ML) could be used to predict student performance.
A typical method of doing this is using previous grades, but it would be much more useful to be able to predict based on personal information, since exam results may be unreliable. 
This gives us an insight into what factors have the greatest effect on student success, so limited resources can be targeted accordingly.

## The Dataset
A dataset on Portuguese Language students provides personal information, two prior exam grades (G1, G2), and a final exam grade (G3) for which scoring 10 or above is required to pass. This forms a binary classification task: using personal information as well as previous years’ grades, predict whether a student will pass or fail their final year exam.

More formally: given 32 input features and an unseen instance, predict whether it falls into category 0 (fail) or category 1 (pass). Using a k-nearest neighbours (KNN) model as a baseline, I propose using a logistic regression (LR) model for this task. 

## Methods
LR uses the logit function to predict the odds of a given instance being in class 0 or 1 based on the input features, meaning the parameters reflect how influential each feature is on the likelihood of a given instance being in class 1. The parameters are applied to the input features to give logit(p) where p is probability of being in class 1.  The hypothesis function represents p and is given by the sigmoid function. This function outputs the probability that an instance is in class 1. 

It is predicted to be in class 1 if it is more likely than a certain threshold (0.5 is used in this paper) that it is, and class 0 otherwise. This process of selecting parameters is called maximum likelihood estimation (MLE).

Hyperparameter tuning was achieved using k-fold cross-validation and an exhaustive grid search.

## Results
Although KNN can perform well with proper preprocessing and tuning, LR generally outperforms KNN and is less likely to overfit. In cases where the dataset is large or imbalanced, LR’s ability to generalize is advantageous. The small dataset size and imbalance were the most limiting factors on the performance, so these must be tackled for future improvements.

## References
This project builds on the approach of using data mining to predict student performance[^1], using the same dataset (from the UCI Machine Learning Repository[^2]).

_scikit-learn_[^3] was used for implementation.

[^1]: Cortez, P. & Gonçalves Silva, A. M. (2008). *Using data mining to predict secondary school student performance*.
[^2]: Cortez, P. (2014). *Student Performance*. UCI Machine Learning Repository. [Online]. DOI: [https://doi.org/10.24432/C5TG7T](https://doi.org/10.24432/C5TG7T)
[^3]: F. Pedregosa et al., “Scikit-learn: Machine learning in Python,” Journal of Machine Learning Research, vol. 12, pp. 2825–2830, 2011
