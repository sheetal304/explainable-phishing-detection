# Explainable Machine Learning for Phishing Website Detection

## Overview
This project compares Logistic Regression and Random Forest for detecting phishing websites, and uses SHAP to explain which features influence the Random Forest's predictions.

## Research question
How accurately can different machine learning models detect phishing websites, and which features influence their predictions?

## Dataset
- UCI Phishing Websites dataset, loaded through OpenML (data_id=4534)
- 11,055 websites, 30 features, no missing values
- Label: -1 = phishing (4,898 websites), 1 = legitimate (6,157 websites)
- All features are pre-computed and take the values -1, 0 or 1

## Method
- Stratified 80/20 train-test split (random_state=42): 8,844 training and 2,211 test websites
- Models: Logistic Regression (max_iter=1000) and Random Forest (100 trees, random_state=42)
- Explainability: Random Forest feature importance and SHAP, computed on a random sample of 300 test websites
