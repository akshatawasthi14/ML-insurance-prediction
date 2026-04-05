# Insurance Cost Analysis and Classification

## Overview

This project applies **data analysis, data cleaning, feature engineering, and machine learning** techniques to an insurance dataset to understand the factors influencing medical charges and to predict whether an individual is likely to incur **high or low insurance costs**.

The workflow follows a structured machine learning pipeline, including exploratory data analysis (EDA), statistical feature analysis, and building a **Logistic Regression classification model**.

---

## Problem Statement

Medical insurance charges vary significantly based on individual characteristics such as age, lifestyle, and health indicators. This project aims to:

* Identify key factors affecting insurance charges
* Evaluate feature importance using statistical methods
* Convert the problem into a classification task (high vs low charges)
* Build a model to predict insurance cost categories

---

## Dataset Description

### Features

* **age** – Age of the individual
* **sex** – Gender
* **bmi** – Body Mass Index
* **children** – Number of dependents
* **smoker** – Smoking status
* **region** – Residential region

### Target Variables

* **charges** – Continuous insurance cost
* **high_charges** – Binary variable created using the median of charges
  * 0 → Low charges
  * 1 → High charges

---

## Methodology

### 1. Exploratory Data Analysis (EDA)

* Examined dataset structure and summary statistics
* Checked for missing values and duplicates
* Analyzed distributions of numerical features
* Explored relationships between features and charges

---

### 2. Data Cleaning

* Removed duplicate records
* Verified data types
* Converted categorical variables (sex, smoker) into numerical format

---

### 3. Feature Engineering

* Applied one-hot encoding to the region column
* Created a binary gender feature (**is_female**)
* Generated a new target variable (**high_charges**) using the median of charges

---

### 4. Feature Analysis

Statistical techniques were used to evaluate relationships between features and insurance charges:

* **Pearson Correlation** for numerical relationships
* **Chi-square Test** for categorical relationships

#### Key Insights

* Smoking status is the strongest predictor of insurance charges
* BMI and age have moderate positive relationships with charges
* Number of children has minimal impact
* Gender and region have negligible influence

These insights were used to guide feature selection for the model.

---

### 5. Model Building

A **Logistic Regression classifier** was used to predict whether an individual falls into the high or low insurance cost category.

Steps:

* Selected relevant features (age, bmi, smoker)
* Split the dataset into training and testing sets
* Applied feature scaling using StandardScaler (after splitting to avoid data leakage)
* Trained the model on the training data

---

### 6. Model Evaluation

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

The model achieved approximately **91% accuracy** with balanced precision and recall, indicating reliable performance across both classes.

---

## Results and Interpretation

The model successfully distinguishes between high and low insurance cost individuals. The results align with the feature analysis.

---

## Conclusion

This project demonstrates how data analysis and feature engineering can be combined with machine learning to solve a real-world problem. By transforming the dataset into a classification task and using statistical insights for feature selection, a reliable model was developed to predict insurance cost categories.

---

## Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## Learning Outcomes

* Understanding of end-to-end machine learning workflow
* Experience with data cleaning and preprocessing
* Application of feature engineering techniques
* Use of statistical methods for feature analysis
* Building and evaluating classification models

---
