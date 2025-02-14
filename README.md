## Comparing KNN and Logistic Regression on Student Data

Education is a key part of society, with higher rates often linked to lower crime and faster economic growth. Many students still struggle, however, so it is important for educators to allocate resources effectively. Machine learning can help predict performance and focus support where it’s most needed.

### The Dataset
A dataset on Portuguese Language students provides personal information, two prior exam grades (G1, G2), and a final exam grade (G3). Scoring 10 or above is required to pass. This forms a binary classification: predict whether a student passes (1) or fails (0) based on 32 input features.

### Methods
A k-nearest neighbors (KNN) model serves as a baseline, but a logistic regression (LR) model is also proposed. LR uses the sigmoid function to estimate the probability of passing. The parameters from LR can indicate how each feature impacts the likelihood of passing.

### Results
Although KNN can perform well with proper preprocessing and tuning, LR generally outperforms KNN and is less likely to overfit. In cases where the dataset is large or imbalanced, LR’s ability to generalize is advantageous. Addressing dataset size and imbalance is crucial for future improvements.

