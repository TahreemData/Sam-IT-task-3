# Sam-IT-task-3
# Credit Card Fraud Detection — Machine Learning
 Project Overview
This project focuses on detecting **fraudulent credit card transactions using machine learning**. The dataset contains anonymized transaction features (`V1`–`V28`), transaction time, transaction amount, and a binary target variable called `Class`.
The project was completed as part of a **Data Science Internship – Task 5: Credit Card Fraud Detection**.
# 🎯 Objectives
* Detect fraudulent credit card transactions.
* Explore and clean the transaction dataset.
* Handle the highly imbalanced target variable.
* Preprocess and scale numerical features.
* Train multiple classification models.
* Evaluate models using:
  * Accuracy
  * Precision
  * Recall
  * F1-Score
  * ROC-AUC
* Analyze confusion matrices.
* Examine feature importance.
## 📊 Dataset
The dataset contains the following main variables:
* `Time` — Time elapsed between transactions.
* `V1` to `V28` — Anonymized numerical features.
* `Amount` — Transaction amount.
* `Class` — Target variable.

### Target Variable

| Class | Meaning                    |
| ----: | -------------------------- |
|     0 | Non-Fraudulent Transaction |
|     1 | Fraudulent Transaction     |

The dataset is **highly imbalanced**, with fraudulent transactions representing a small proportion of all transactions.

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Inspection
   ↓
Missing Value Check
   ↓
Duplicate Removal
   ↓
Class Distribution Analysis
   ↓
Feature & Target Separation
   ↓
Feature Scaling
   ↓
Stratified Train-Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Confusion Matrix
   ↓
ROC-AUC Analysis
   ↓
Feature Importance
```

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked dataset dimensions and column names.
3. Inspected data types and statistical summaries.
4. Checked for missing values.
5. Removed duplicate records.
6. Analyzed the distribution of fraudulent and non-fraudulent transactions.
7. Separated features from the target variable.
8. Standardized `Time` and `Amount`.
9. Used a stratified train-test split to preserve the class distribution.

## 🤖 Machine Learning Models

Two classification algorithms were implemented:

### 1. Logistic Regression

Logistic Regression was used as a baseline classification model. Class weighting was applied to give greater consideration to the minority fraud class.

### 2. Random Forest

Random Forest was used as an ensemble classification model. It was also configured with balanced class weights to address the imbalanced dataset.

## 📈 Model Evaluation

The models were evaluated using:

### Accuracy

Measures the overall percentage of correctly classified transactions.

### Precision

Measures how many transactions predicted as fraud were actually fraudulent.

### Recall

Measures how many actual fraudulent transactions were successfully detected.

### F1-Score

Provides a balance between Precision and Recall.

### ROC-AUC

Measures the model's ability to distinguish between fraudulent and non-fraudulent transactions across classification thresholds.
### Confusion Matrix
Used to analyze:
* True Negatives
* False Positives
* False Negatives
* True Positives
## 📊 Visualizations
The project includes visualizations for:
* Class distribution
* Fraud vs. non-fraud percentage
* Transaction amount distribution
* Confusion matrices
* Model performance comparison
* ROC curves
* Top feature importance
## 📌 Key Consideration
Credit card fraud datasets are highly imbalanced. Therefore, **accuracy should not be considered alone** when evaluating fraud detection models. Precision, Recall, F1-Score, and ROC-AUC provide additional information about the model's ability to identify the minority fraud class.
