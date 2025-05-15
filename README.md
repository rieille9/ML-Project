# ML-Project
# Stack Overflow Tag Prediction with NLP & Machine Learning

*Machine Learning Project – University of Geneva, MSc in Business Analytics*  
 **Submission Date**: December 22, 2023  
 **Kaggle Score**: 94.7%  
 Authors: Eva Battolla, Lima Madomi, Rachel Rieille

---

## 📌 Project Overview

This project aims to **predict missing tags** for Stack Overflow posts using advanced **Natural Language Processing (NLP)** techniques and a variety of **machine learning models**. The dataset consists of thousands of programming-related questions, and each post is associated with one correct tag.

We explored multiple models including:
- Logistic Regression
- Support Vector Machines (SVM)
- Random Forest
- GridSearchCV for hyperparameter tuning

Best result: **Random Forest model with custom preprocessing and TF-IDF vectorization**, achieving **94.7% accuracy** on the Kaggle public leaderboard.

---

## 🧠 Problem Statement

- **Goal**: Predict the appropriate programming tag (e.g., `python`, `c#`, `php`) for a given post.
- **Data**: Posts contain raw HTML and messy natural language, making preprocessing crucial.
- **Challenge**: Similar tags (`c#`, `c++`, `c`) and high vocabulary variety.

---

## 🔍 Key Steps

### 1. Exploratory Data Analysis (EDA)
- Dataset: ~28,000 posts with associated tags
- Balanced tag distribution across 20 classes
- Visualizations of tag frequency and token counts

### 2. Text Preprocessing
- HTML decoding, lowercase transformation, symbol cleaning
- Custom **tokenizer with POS tagging** and **lemmatization**
- Preserved important tokens like `c#` to avoid misclassification

### 3. Feature Engineering
- Applied **TF-IDF Vectorization** to represent posts as numerical features
- Minimized vocabulary noise with thresholds and lemmatized tokens

### 4. Model Training & Evaluation
- Models used: Logistic Regression, SVM, Random Forest
- Evaluation via confusion matrices and classification reports
- **GridSearchCV** used to tune hyperparameters for each model

### 5. Results
- **Random Forest** was the top-performing model with:
  - Custom tokenizer
  - Optimal parameters: `n_estimators=500`, `max_depth=None`, `min_samples_split=10`
  - Kaggle score: **0.94702**
- Logistic Regression and SVM also performed competitively (~0.91 and ~0.93)

---

## 📊 Performance Summary

| Model               | Training Accuracy | Kaggle Score |
|--------------------|-------------------|--------------|
| Logistic Regression| 79.9%             | ~91.1%       |
| SVM (RBF Kernel)   | 79.4%             | ~93.8%       |
| 🏆 Random Forest    | **81.2%**         | **94.7%**     |


