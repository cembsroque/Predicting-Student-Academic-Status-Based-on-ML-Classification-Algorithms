# Student Dropout Prediction

This project focuses on predicting student dropout status using machine learning. It was built as part of my portfolio to demonstrate core data science skills including data preprocessing, model training, evaluation, and interpretation.

---

## Problem Statement

Student dropout is a significant issue in educational institutions, impacting both student success and institutional performance. The goal of this project is to build predictive models that classify students into three categories:

- **0** — Dropped Out  
- **1** — Currently Enrolled  
- **2** — Graduated

By identifying students at risk of dropping out, institutions can intervene earlier and offer better support.

---

## Dataset

The dataset includes demographic and academic information on students, such as:

- Gender, marital status, age
- Previous qualifications
- Application mode and education level
- Target (dropout/enrolled/graduated)

> Note: The dataset was preprocessed to handle categorical features and missing values. Classes were slightly imbalanced, with fewer examples in the “Enrolled” category.

---

## Models & Techniques

Three classification models were implemented:

- **XGBoost** *(best performance)*
- **Random Forest**
- **Logistic Regression**

### Preprocessing:
- Label encoding and one-hot encoding for categorical variables
- Feature scaling where needed (e.g., Logistic Regression)

### Techniques:
- Class weighting to address imbalance
- Hyperparameter tuning using `RandomizedSearchCV`
- Model evaluation using accuracy, precision, recall, F1-score

---

## Results

- **Best Model**: XGBoost  
- **Accuracy**: ~77%  
- **Challenge**: Class 1 (Enrolled) consistently had low recall. Class weighting and tuning did not significantly improve this, suggesting the difficulty is due to the **transitional nature** of this group and **fewer training examples**.

---

## 📁 Project Structure

├── data/ # Raw dataset (not uploaded) ├── notebooks/ # Jupyter Notebook with full workflow ├── README.md # You're here!


---

## Let's Connect

If you're a recruiter, data team, or fellow learner — feel free to reach out!  
I'm actively looking for **entry-level data science opportunities**.

- 📧 Email: eduroque109@gmail.com  
- 💼 LinkedIn: www.linkedin.com/in/carlos-roque-692b07239

---

*Thanks for reading — and I hope you find this project useful!*
