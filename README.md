# MSK - Redefining Cancer Treatment

This project is based on the Kaggle competition [MSK - Redefining Cancer Treatment](https://www.kaggle.com/c/msk-redefining-cancer-treatment), where the goal is to classify genetic mutations in tumors to assist in treatment planning.

## Project Overview

In this project, I explored various machine learning models to predict the classification of genetic mutations. The primary focus was on performing univariate analysis on gene, variant, text data and experimenting with different encoding techniques (one-hot encoding and response coding). The models were evaluated based on misclassification (percentages), training, cross-validation (CV), and test (Log loss).

## Final Results

|                  Models                  | Misclassified(%) | Train (Log Loss) |  CV (Log Loss)  | Test (Log Loss) |
|------------------------------------------|------------------|-------------------|------------------|------------------|
| Naive Bayes (One hot encoding)           | 0.41             | 0.9               | 1.25             | 1.2              |
| KNN (Response)                           | 0.35             | 0.59              | 1.05             | 1.05             |
| Logistic Regression (Class balanced)     | 0.35             | 0.45              | 1.11             | 1.08             |
| Logistic Regression (Class unbalanced)   | 0.34             | 0.43              | 1.12             | 1.09             |
| SVM (One hot encoding)                   | 0.37             | 0.51              | 1.14             | 1.13             |
| Random Forest (One hot encoding)         | 0.39             | 0.62              | 1.16             | 1.16             |
| Random Forest (Response coding)          | 0.5              | 0.06              | 1.33             | 1.38             |
| Stacking classifier                      | 0.35             | 0.39              | 1.08             | 1.05             |

## Key Steps

1. **Data Preprocessing**:
   - Univariate analysis of gene variant text data.
   - Encoding the categorical features using One-Hot Encoding and Response Coding.

2. **Model Selection**:
   - Tested several models including Naive Bayes, KNN, Logistic Regression (class balanced and unbalanced), SVM, Random Forest, and Stacking classifier.
   - Evaluated models based on misclassification percentage, Log loss on training, cross-validation (CV), and test sets.

3. **Evaluation**:

   - The **Stacking Classifier** performed quite well, achieving a **test log loss of 1.05**, which is among the best results. However, despite its strong performance, **Logistic Regression** (with class unbalanced) was selected as the preferred model.
  
   - Although **Logistic Regression** had a slightly higher test log loss of **1.09**, it offers greater **interpretability**. Logistic Regression provides clear insights into how different gene mutations contribute to classification, which is valuable in the context of cancer treatment, where understanding the impact of features is as important as predictive accuracy. This makes it a more practical choice for real-world applications in the medical field.

