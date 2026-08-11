# Breast Cancer Classification Using Machine Learning

## 1. Problem Statement

The objective of this project is to implement and compare multiple
machine learning classification algorithms for predicting whether a
breast tumor is Benign or Malignant.

The following classification algorithms are implemented and evaluated:

1. Logistic Regression
2. Decision Tree Classifier
3. K-Nearest Neighbor (kNN) Classifier
4. Gaussian Naive Bayes
5. Random Forest Classifier
6. Support Vector Classifier (SVC) - Additional Model

The models are evaluated using:

- Accuracy
- AUC Score
- Precision
- Recall
- F1 Score
- Matthews Correlation Coefficient (MCC)

An interactive Streamlit application is also developed to allow users
to upload test data, select a classification model, and view the
evaluation results.

---

## 2. Dataset Description

### Dataset Name

Breast Cancer Wisconsin Diagnostic Dataset

### Dataset File

`Breast_cancer_dataset.csv`

### Dataset Characteristics

- Number of instances: 569
- Number of predictive features: 30
- Number of classes: 2
- Problem type: Binary Classification

### Target Variable

The target variable is `diagnosis`.

The target values are encoded as:

| Original Value | Encoded Value | Meaning |
|---|---:|---|
| B | 0 | Benign |
| M | 1 | Malignant |

### Features

The dataset contains 30 numerical features describing characteristics
of breast cell nuclei, including measurements related to:

- Radius
- Texture
- Perimeter
- Area
- Smoothness
- Compactness
- Concavity
- Concave points
- Symmetry
- Fractal dimension

Each of these measurements is available in mean, standard error and
worst-value forms.

### Data Preprocessing

The following preprocessing steps are performed:

1. Load the CSV dataset.
2. Check the dataset shape and structure.
3. Check for missing values.
4. Remove the `id` column because it is an identifier.
5. Remove the `Unnamed: 32` column because it does not contain useful
   predictive information.
6. Encode the target variable:
   - B → 0
   - M → 1
7. Separate independent features and dependent target.
8. Split the dataset into 80% training and 20% testing data.
9. Stratified sampling is used to preserve the class distribution.
10. Min-Max Scaling is applied to the features.

---

## 3. GitHub Repository

GitHub Repository:

**<PASTE YOUR GITHUB REPOSITORY LINK HERE>**

Example:

https://github.com/yourusername/Breast-Cancer-ML-Assignment

---

## 4. Models Used

### 4.1 Logistic Regression

Logistic Regression is a supervised classification algorithm used to
predict the probability of a binary outcome.

In this project, it is used to classify breast cancer cases as
Benign or Malignant.

---

### 4.2 Decision Tree Classifier

Decision Tree is a tree-based supervised classification algorithm.

It recursively divides the feature space using decision rules and
eventually assigns each observation to a class.

---

### 4.3 K-Nearest Neighbor (kNN)

K-Nearest Neighbor classifies a sample based on the classes of its
nearest training observations.

Feature scaling is important for kNN because it uses distance
calculations.

---

### 4.4 Gaussian Naive Bayes

Gaussian Naive Bayes is a probabilistic classification algorithm based
on Bayes' theorem.

It assumes that the numerical features follow Gaussian distributions
within each class and assumes conditional independence between
features.

---

### 4.5 Random Forest

Random Forest is an ensemble classification algorithm consisting of
multiple decision trees.

The final prediction is obtained by combining the predictions of
the individual trees.

---

### 4.6 Support Vector Classifier (SVC)

SVC is included as an additional classification model because the
reference classifier notebook also demonstrates Support Vector
Classification.

SVC attempts to find a decision boundary that separates the classes
while maximizing the margin between them.

---

## 5. Evaluation Metrics

The following six evaluation metrics are calculated for every model.

### Accuracy

Accuracy measures the proportion of correctly classified observations
among all observations.

### AUC Score

AUC measures the ability of the classifier to distinguish between the
two classes across different classification thresholds.

### Precision

Precision measures the proportion of predicted positive observations
that are actually positive.

### Recall

Recall measures the proportion of actual positive observations that
are correctly identified.

### F1 Score

F1 Score is the harmonic mean of Precision and Recall.

### Matthews Correlation Coefficient (MCC)

MCC measures the quality of binary classification predictions while
taking all four confusion-matrix categories into account.

---

## 6. Model Comparison

The following table presents the evaluation results obtained from the
test dataset.

| ML Model Name | Accuracy | AUC | Precision | Recall | F1 Score | MCC |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | XX.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX |
| Decision Tree | XX.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX |
| kNN | XX.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX |
| Naive Bayes | XX.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX |
| Random Forest | XX.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX |
| SVC | XX.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX | X.XXXX |

> Replace the `XX.XXXX` values with the actual values obtained after
> executing the program in BITS Virtual Lab.

---

## 7. Observations on Model Performance

### Logistic Regression

Logistic Regression provides strong classification performance on the
Breast Cancer dataset. It provides a good balance between precision,
recall, F1 score and AUC.

The model is also relatively simple and interpretable compared with
more complex ensemble models.

---

### Decision Tree

The Decision Tree provides reasonable classification performance.

However, its performance may be lower than ensemble methods because a
single decision tree can be more sensitive to the training data.

---

### kNN

kNN provides good classification performance after feature scaling.

Since kNN is a distance-based algorithm, Min-Max Scaling is important
to ensure that features with larger numerical ranges do not dominate
the distance calculation.

---

### Naive Bayes

Gaussian Naive Bayes provides reasonable classification performance.

Its performance can be affected by the assumption that the features
are conditionally independent, while several measurements in the
Breast Cancer dataset can be correlated.

---

### Random Forest

Random Forest provides strong classification performance.

Because it combines predictions from multiple decision trees, it can
provide better generalization than an individual Decision Tree.

---

### SVC

SVC provides strong classification performance on the scaled feature
set.

Since SVC is sensitive to feature scales, Min-Max Scaling is applied
before model training.

---

## 8. Overall Winner

The overall winner is selected by comparing the six evaluation metrics:

- Accuracy
- AUC
- Precision
- Recall
- F1 Score
- MCC

### Overall Winner:

**<ENTER FINAL WINNING MODEL HERE>**

### Reason

The winning model provides the strongest overall performance across
the evaluation metrics on the test dataset.

The final winner should be selected using the actual results generated
by the program rather than assuming a winner before execution.

---

## 9. Streamlit Application

An interactive Streamlit application has been developed for evaluating
the trained classification models.

### Application Features

The application provides:

1. CSV test-data upload.
2. Classification model selection.
3. Accuracy display.
4. AUC display.
5. Precision display.
6. Recall display.
7. F1 Score display.
8. MCC display.
9. Confusion matrix.
10. Classification report.
11. Prediction results.
12. Downloadable prediction results.

### Streamlit Application Link

**<PASTE YOUR STREAMLIT APP LINK HERE>**

Example:

https://your-app-name.streamlit.app

---

## 10. Project Structure

```text
Breast-Cancer-ML-Assignment/
│
├── app.py
├── train_models.py
├── README.md
├── requirements.txt
├── Breast_cancer_dataset.csv
├── test_data.csv
├── model_comparison.csv
│
└── model/
    ├── logistic_regression.pkl
    ├── decision_tree.pkl
    ├── knn.pkl
    ├── naive_bayes.pkl
    ├── random_forest.pkl
    └── svc.pkl
