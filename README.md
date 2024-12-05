# Heart Disease Prediction

This project uses machine learning models to predict heart disease based on patient data. It involves data preprocessing, exploratory data analysis, and model training to identify key factors and develop predictive models.

## Overview

- Objective: Predict the presence of heart disease using patient attributes and compare model performances.
- Dataset: Contains 303 patient records with 14 features, including age, cholesterol levels, maximum heart rate, and target (presence/absence of heart disease).
- Models Evaluated:
  - Logistic Regression
  - Naive Bayes
  - Decision Tree
- Performance Metrics: Accuracy, Sensitivity, Specificity, and Kappa.

## File Structure

- `Heart_Disease_Analysis.Rmd`: The main R Markdown file containing the analysis, model training, and performance evaluation.
- `Heart_Disease_Analysis_Report.docx`: A detailed report describing the dataset, preprocessing, models, and findings.
- `heart-disease.csv`: The dataset used for analysis.
- `Models/`:
  - `Logistic_Regression_Model.rds`: The saved Logistic Regression model.
  - `Naive_Bayes_Model.rds`: The saved Naive Bayes model.
  - `Decision_Tree_Model.rds`: The saved Decision Tree model.

## Key Steps

### Data Preparation
- Checked for missing values (none found) and removed outliers in numerical variables using the Interquartile Range (IQR) method.
- Converted categorical variables to factors and normalized the dataset for analysis.

### Exploratory Data Analysis (EDA)
- Created boxplots to analyze the relationship between age, cholesterol, heart rate, and ST depression levels with heart disease.
- Generated stacked bar charts to evaluate distributions across sex, chest pain type, and slope categories.

### Model Training and Evaluation
- Split the dataset into training (70%) and testing (30%) sets.
- Trained three models using default parameters:
  1. Logistic Regression
  2. Naive Bayes
  3. Decision Tree
- Evaluated model performance on the test set using:
  - Accuracy
  - Sensitivity
  - Specificity
  - Kappa statistic
  - Confusion Matrix

## Results

| Model              | Accuracy | Sensitivity | Specificity | Kappa   |
|---------------------|----------|-------------|-------------|---------|
| Logistic Regression | 83.91%   | 83.78%      | 84.00%      | 0.6731  |
| Naive Bayes         | 81.61%   | 76.74%      | 86.36%      | 0.6317  |
| Decision Tree       | 77.01%   | 74.36%      | 79.17%      | 0.5353  |

### Key Findings
- Logistic Regression: Best-performing model with balanced accuracy, sensitivity, and specificity.
- Naive Bayes: Strong at identifying individuals without heart disease but slightly weaker overall.
- Decision Tree: Simplest model but less accurate and sensitive.

## Recommendations
1. Logistic Regression is the most balanced and accurate model for predicting heart disease in this dataset.
2. Preprocessing steps, such as handling outliers and normalizing data, significantly improved model performance.
3. Future work could involve hyperparameter tuning or testing additional algorithms like Random Forest or SVM.

## Getting Started

### Prerequisites
- Software:
  - R (version ≥ 4.0.0)
- Required R Packages:
  - `tidyverse`
  - `caret`
  - `e1071`
  - `rpart`

### Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/rohantucker/Heart-Disease-Prediction.git
