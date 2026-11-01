Adult Census Income Prediction Using Deep Learning

Project Overview

This project uses the Adult Census Income dataset to predict whether a person's annual income is greater than 50,000 dollars. It applies data preprocessing, exploratory data analysis, and artificial neural network experiments to understand how different deep learning choices affect binary classification performance.

Project Objectives

The main objective is to build and evaluate a multilayer perceptron model for income classification. The project also compares activation functions, weight initialization methods, loss functions, batch normalization, optimizers, and learning rates.

Dataset

The project uses the Adult Census Income dataset. It contains demographic and employment related information such as age, education, occupation, marital status, working hours, and other census attributes. The target column is income, which is converted into two classes. The value less than or equal to 50,000 dollars is encoded as zero, and income greater than 50,000 dollars is encoded as one.

Project Workflow

Data Loading and Cleaning

The notebook loads the dataset from adult.csv or adult.csv.zip. It removes extra whitespace, converts question mark values into missing values, and drops rows containing missing values. It also removes the fnlwgt column and the redundant education text column when present.

Exploratory Data Analysis

The project explores income class distribution, age distribution, weekly working hours, education level, and relationships between numerical features. These visualizations help identify class imbalance and possible relationships between the input features and income.

Data Preprocessing

Categorical features are converted into numerical indicators using one hot encoding. Numeric features are standardized. The data is split into training and testing sets using stratification to preserve the income class distribution. The scaler is fitted on training data only to reduce data leakage.

Artificial Neural Network

A multilayer perceptron is created with two hidden layers containing 128 and 64 neurons and a single sigmoid output neuron. The output represents the probability that a record belongs to the income greater than 50,000 dollars class.

Deep Learning Experiments

The notebook compares ReLU, tanh, sigmoid, and ELU activation functions. It evaluates Glorot Uniform, Glorot Normal, He Uniform, He Normal, and zero weight initialization. It also compares binary cross entropy, mean squared error, weighted binary cross entropy, and focal loss.

Batch Normalization and Optimizers

Batch normalization is evaluated to study its effect on training stability and model performance. The notebook compares SGD, SGD with momentum, RMSprop, and Adam. Different learning rates are also tested to observe their influence on model convergence.

Model Evaluation

The models are evaluated using accuracy, precision, recall, F1 score for the higher income class, and ROC AUC. Confusion matrices, training curves, and ROC curves are used to compare model behavior. Since the dataset is imbalanced, accuracy is not used as the only measure of performance.

Technologies Used

Python
Jupyter Notebook
Pandas
NumPy
Matplotlib
Seaborn
Scikit learn
TensorFlow and Keras

Installation and Setup

Install the required libraries using the following command.

pip install numpy pandas matplotlib seaborn scikit-learn tensorflow jupyter

Place adult.csv or adult.csv.zip in the same folder as the notebook. Open DL_PR2.ipynb in Jupyter Notebook or Visual Studio Code and run the cells in order.

Expected Results

The notebook produces data cleaning summaries, exploratory visualizations, training and validation curves, activation and initialization comparisons, loss function comparisons, batch normalization experiments, optimizer comparisons, and a final model evaluation table.

The best model should be selected based on the metrics produced when the notebook is executed. Results can vary depending on the environment and training run.

Conclusion

This project demonstrates a complete deep learning workflow for a binary classification problem using census data. It shows how preprocessing decisions and neural network configurations can affect predictive performance. It also highlights the importance of evaluating precision, recall, F1 score, and ROC AUC when the target classes are imbalanced.

Author

Smit Patel
