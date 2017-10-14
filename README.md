# machine_learning_benchmark

The objective of this exercise is to benchmark machine learning algorithm from different libraries and platforms

The algorithms studied are

- Random Forest in scikit-learn
- Decision Tree in scikit-learn
- Logistic Regression in scikit-learn
- Neural Network in Keras.io
- Random Forest in H2O
- Gradient Boosting in H2O
- Deep Learning in H2O
- Naive Bayes in H2O

in various commonly used open source implementations like
- Python scikit-learn
- H2O
- xgboost
- Spark MLlib


Random forest, boosting and more recently deep neural networks are the algos expected to perform the best on the structure/sizes described above (e.g. vs alternatives such as k-nearest neighbors, naive-Bayes, decision trees, linear models etc). Non-linear SVMs are also among the best in accuracy in general, but become slow/cannot scale for the larger n sizes we want to deal with. The linear models are less accurate in general and are used here only as a baseline (but they can scale better and some of them can deal with very sparse features, so they are great in other use cases).

By scalability we mean here that the algos are able to complete (in decent time) for the given data sizes with the main constraint being RAM (a given algo/implementation will crash if running out of memory). Some of the algos/implementations can work in a distributed setting, although the largest dataset in this study n = 10M is less than 1GB, so scaling out to multiple machines should not be necessary and is not the focus of this current study. (Also, some of the algos perform relatively poorly speedwise in the multi-node setting, where communication is over the network rather than via updating shared memory.) Speed (in the single node setting) is determined by computational complexity but also if the algo/implementation can use multiple processor cores. Accuracy is measured by AUC. The interpretability of models is not of concern in this project.

In summary, we are focusing on which algos/implementations can be used to train relatively accurate binary classifiers for data with millions of observations and thousands of features processed on commodity hardware (mainly one machine with decent RAM and several cores).


Data

Setup

Results

