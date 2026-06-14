# Fake News Detection using Machine Learning

## Project Overview

This project implements a Machine Learning based Fake News Detection system using Natural Language Processing (NLP) techniques.

The objective is to classify news articles as **Fake News** or **True News** based on their textual content. The project uses a publicly available dataset containing fake and genuine news articles and applies text preprocessing, TF-IDF vectorization, and machine learning algorithms for classification.

---

## Dataset

The dataset consists of two CSV files:

* **Fake.csv** → Contains fake news articles.
* **True.csv** → Contains genuine news articles collected from Reuters.

Each article contains:

* Title
* News Content
* Subject
* Date

For model training, a class label was added:

* **1** → Fake News
* **0** → True News

---

## Technologies Used

* Python
* Pandas
* Scikit-Learn
* Regular Expressions (re)
* Google Colab

---

## Machine Learning Workflow

### 1. Data Loading

The Fake and True news datasets are loaded using Pandas.

### 2. Data Labeling

A class column is added:

* Fake News = 1
* True News = 0

### 3. Data Merging and Shuffling

Both datasets are merged into a single DataFrame and shuffled to eliminate ordering bias.

### 4. Data Cleaning

Unnecessary columns such as:

* title
* subject
* date

are removed.

### 5. Text Preprocessing

The news text is cleaned by:

* Converting text to lowercase
* Removing URLs
* Removing special characters
* Removing extra spaces

### 6. Train-Test Split

The dataset is divided into:

* 75% Training Data
* 25% Testing Data

### 7. TF-IDF Vectorization

Text data is converted into numerical feature vectors using TF-IDF (Term Frequency – Inverse Document Frequency).

### 8. Model Training

The following machine learning models are used:

* Logistic Regression
* Decision Tree Classifier

### 9. Model Evaluation

Performance is evaluated using:

* Accuracy Score
* Precision
* Recall
* F1 Score
* Classification Report

### 10. Hyperparameter Tuning

GridSearchCV is used to identify the best parameters for the Logistic Regression model.

---

## Results

The Logistic Regression model achieved approximately **99% accuracy** on the testing dataset.

Best hyperparameters obtained through GridSearchCV:

```python
{'C': 10, 'solver': 'liblinear'}
```

This demonstrates the effectiveness of NLP and machine learning techniques in detecting fake news articles.

---

---

Developed as part of a Machine Learning internship project on Fake News Detection using Natural Language Processing and Classification Algorithms.
