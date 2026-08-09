# Iris Flower Classification

## Project Overview

This project focuses on classifying Iris flowers into three different species using supervised machine learning.

The three species are:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

The model uses four flower measurements as input features:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

A Logistic Regression model is trained after standardizing the numerical features using StandardScaler.

## Objective

The main objective of this project is to build a simple and complete machine learning classification pipeline that can predict the species of an Iris flower from its sepal and petal measurements.

The project covers:

- Dataset loading
- Data inspection
- Data cleaning
- Exploratory Data Analysis
- Feature selection
- Train-test splitting
- Feature scaling
- Logistic Regression model training
- Model evaluation
- Visualization
- Model saving and verification

## Dataset

The dataset used in this project is the classic Iris dataset from the UCI Machine Learning Repository.

The dataset contains:

- 150 samples
- 4 numerical features
- 3 target classes

The four features are:

1. Sepal Length
2. Sepal Width
3. Petal Length
4. Petal Width

Each species contains 50 samples.

## Technologies Used

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Google Colab

## Machine Learning Model

Logistic Regression was selected as the classification algorithm.

Before training the model, StandardScaler was used to standardize the four numerical features.

The complete preprocessing and model were combined into a Scikit-learn Pipeline.

This makes the saved model easier to reuse because the same preprocessing is automatically applied before prediction.

## Project Workflow

The project follows this workflow:

1. Load the Iris dataset
2. Inspect the dataset
3. Check data types
4. Check missing values
5. Check duplicate records
6. Analyze class distribution
7. Perform exploratory data analysis
8. Visualize feature relationships using a pairplot
9. Generate a correlation heatmap
10. Generate feature distribution plots
11. Generate boxplots
12. Select input features and target variable
13. Split the dataset into training and testing sets
14. Standardize the features
15. Train Logistic Regression
16. Generate predictions
17. Evaluate the model
18. Visualize the confusion matrix
19. Save the trained model
20. Load the saved model and verify its performance

## Data Preprocessing

The Iris dataset was checked for missing values and duplicate records.

No missing values were found in the dataset.

Three duplicate rows were detected. These were retained because the dataset is the standard Iris dataset and the duplicate measurements are valid records within the original dataset.

The target variable contains three classes:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

## Train-Test Split

The dataset was divided into:

- 80% training data
- 20% testing data

This resulted in:

- Training samples: 120
- Testing samples: 30

Stratified splitting was used so that each species remained equally represented in both training and testing datasets.

## Exploratory Data Analysis

Several visualizations were created during the project.

### Class Distribution

The dataset contains 50 samples for each Iris species.

### Pairplot

A pairplot was used to visualize relationships between the four numerical features and observe how the different species are distributed.

### Correlation Heatmap

A correlation heatmap was created to understand relationships between the numerical features.

### Histograms

Histograms were generated to examine the distribution of each feature across the three species.

### Boxplots

Boxplots were created to compare the feature distributions between the different Iris species.

### Confusion Matrix

A confusion matrix heatmap was created to visualize the classification performance of the Logistic Regression model.

## Model Performance

The Logistic Regression model achieved the following results:

| Metric | Result |
|---|---:|
| Training Samples | 120 |
| Testing Samples | 30 |
| Number of Features | 4 |
| Model | Logistic Regression |
| Preprocessing | StandardScaler |
| Accuracy | 93.33% |
| Incorrect Predictions | 2 |

## Classification Report

The model achieved the following performance on the test dataset:

| Class | Precision | Recall | F1-Score |
|---|---:|---:|---:|
| Iris-setosa | 1.00 | 1.00 | 1.00 |
| Iris-versicolor | 0.90 | 0.90 | 0.90 |
| Iris-virginica | 0.90 | 0.90 | 0.90 |

Overall accuracy:

**93.33%**

The model correctly classified 28 out of 30 test samples.

Two predictions were incorrect:

- Iris-virginica was predicted as Iris-versicolor
- Iris-versicolor was predicted as Iris-virginica

Iris-setosa was classified correctly for all 10 test samples.

## Model Saving

The complete preprocessing and Logistic Regression pipeline was saved using Joblib.

The saved model file is:

```text
iris_logistic_regression_model.pkl
