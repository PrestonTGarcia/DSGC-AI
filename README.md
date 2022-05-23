# DSGC-AI
This is a project I worked on as my final project in my Machine Learning Fundamentals course. The goal was to create the "best" model to predict whether a electrical grid with four nodes is stable or unstable. The entire notebook was made by me, and the dataset was retrieved from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Electrical+Grid+Stability+Simulated+Data+)

### Inputs/Outputs
The input to the model is the reaction time (tau), power consumed/produced (p), and a coefficient representing the changing of price (g) of each node in the electrical grid. After a classifier model processes the data, a Boolean value is output, where a 0 represents a stable electrical grid and a 1 represents an unstable electrical grid.

### Dataset Splits
The entire dataset consists of 10,000 instances of data on four node electrical grids. The data is randomly permuted and split into two subsets: 70% training and 30% testing. Models are trained on the training set using 5 fold cross validation. Models are trained on the training set, and the validation set is used to measure performance on a clean dataset. The test set is then used to evaluate the model's final performance.

### Hyperparameter Optimization
To optimize the hyperparameters, sklearn's GridSearchCV module was used. This would try each of the hyperparameter permutations specified in the first cell of each model. For the neural network section, a random grid search was done by hand instead of using GridSearchCV with neurons in the set of {2, 4, 8, 16, 32, 64, 128, 256, 512, 1024} and activation functions in the set of {relu, elu, selu, tanh, exponential}.
