# Applied Machine Learning Project - BASIC #
# Breast Cancer Wisconsin (Diagnostic) - Benign vs Malignant using Logistic Regression #

This project focuses on the classification of breast cancer tumors as **malignant** or **benign** using machine learning techniques. The model is built using **Logistic Regression** and trained on the **Breast Cancer Wisconsin (Diagnostic)** dataset.
The goal is to demonstrate how computational methods can assist in early cancer detection by analyzing biological features of cell nuclei.

## Dataset Information ##

**Dataset: Breast Cancer Wisconsin (Diagnostic)**

**Source: UCI Machine Learning Repository**

# Description #

The dataset contains **569** samples obtained from **Fine Needle Aspiration (FNA)** biopsies of breast masses.

Each sample is described using **30 numerical features** that capture the characteristics of cell nuclei, including **(radius, texture, perimeter, area, smoothness and etc)**

These features are computed as:

* Mean values
  
* Standard error (SE)
  
* Worst (extreme) values

 ## Objectives ##

* To build a **binary classification model** using Logistic Regression model to accurately classify tumors as **benign (Cancerous)** or **malignant (Non-cancerous)** based on cellular morphology.

* Compare model performance against a **baseline classifier** to validate predictive improvement.

* Prioritize reducing false negatives, ensuring malignant cases are rarely missed.

## Challenges ##

* Class imbalance (**357 benign vs 212 malignant**)

* Presence of highly correlated features (mean, SE, worst values)
  
* Need for **feature scaling** due to varying ranges

## Methodology ##

**1. Data Preprocessing**

* Removed unnecessary columns (e.g., ID)

* Encoded target labels (M = 1, B = 0)

* Checked for missing values

**2. Exploratory Data Analysis (EDA)**

* Distribution of features.

* Correlation heatmap.

* Class distribution analysis.

**3. Feature Engineering**

* Identified and handled multicollinearity.

* Selected relevant features for model training.

**4. Data Splitting**

Train-test split to evaluate model performance.

**5. Baseline Model (Dummy Classifier)**

A **Dummy Classifier** was used as a baseline, predicting the most frequent class without learning from features. It achieved **63% accuracy**, serving as a reference to ensure the Logistic Regression model performs better than uninformed prediction.

**5. Feature Scaling**

Applied `StandardScaler` to normalize feature values

**6. Model Building**

Logistic Regression model used

Handled class imbalance using:

**class_weight = 'balanced'**

**Why Logistic Regression?**

* Simple and interpretable model

* Works well with structured tabular data

* Efficient and fast to train, provides probability outputs, useful in medical diagnosis

## Model Evaluation ##

The model performance was evaluated using:

* Accuracy

* Confusion Matrix

* ROC Curve - AUC Score

## Key Metrics ##

Accuracy: 98%

ROC-AUC Score: 0.99

## Results Interpretation ##

* The model successfully distinguishes between malignant and benign tumors.

* Balanced class weights improve detection of malignant cases.

* Feature scaling improves model performance.

## Bioinformatics Relevance ##

This project highlights the role of machine learning in bioinformatics and medical diagnostics, where computational models assist in analyzing biological data for disease prediction and decision-making.

## Author ##

Yusra Tahir

Bioinformatics - University of Bologna
