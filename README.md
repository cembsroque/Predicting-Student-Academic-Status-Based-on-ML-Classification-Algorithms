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

- Gender, age, nationality
- Previous qualifications
- Application mode and education level
- Target (dropout/enrolled/graduated)

> Note: The dataset was preprocessed to handle categorical features and missing values. Classes were slightly imbalanced, with fewer examples in the “Enrolled” category.

---
## Exploratory Data Analysis (EDA)
Before modeling, an in-depth exploration of the dataset was conducted to uncover patterns, assess data quality, and guide feature engineering.

### Categorical Feature Mapping
Several categorical variables (e.g., education level, course, language, etc.) were originally encoded as numerical codes.

These were mapped to human-readable labels using dictionaries to improve interpretability and visualization.

### Visualizations
EDA was supported by visual insights using Matplotlib, Seaborn, and Plotly. The following types of plots were used:

  - Distribution Plots 
    - Admission Grades and Age at Enrollment were plotted using histograms with KDE (Kernel Density Estimate) overlays.
  These helped in analyzing the shape of the distributions and detecting skewness or anomalies.

  - Bar Charts 
    - Unemployment Rate by Course: Highlighted which academic programs were associated with higher post-graduation unemployment.

    - Nationality Distribution: Displayed using a log-scaled bar chart to better visualize less-represented groups.

    - Target Distribution: The target variable "Enrolled" (indicating students who remained enrolled) is underrepresented compared to the other two classes — "Graduate" and "Dropout" — revealing a class imbalance   that may impact model performance.

  - Pie Charts 
    - Illustrated the proportion of Mother’s and Father’s education levels in the dataset, as also gender and course distributions.

  - Boxplots 
    - Used to compare Previous Qualification types against admission grades. Helped identify variations in performance based on different academic backgrounds and detect outliers.

  -  Pairplot \
    - A Seaborn pairplot was generated to visualize pairwise relationships between key numerical variables, colored by the target class ("Enrolled", "Graduate", and "Dropout"). \
    - This helped in spotting potential clusters, linear separability, and overlapping regions between classes. \
    - Notably, some variables (such as Admission Grade and Age at Enrollment) showed distinguishable patterns among the classes, which can inform feature selection and model choice.

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

## Project Structure

├── data/ # Raw dataset (not uploaded) ├── notebooks/ # Jupyter Notebook with full workflow ├── README.md # You're here!


---

## Let's Connect

If you're a recruiter, data team, or fellow learner — feel free to reach out!  
I'm actively looking for **entry-level data science opportunities**.

- 📧 Email: eduroque109@gmail.com  
- 💼 LinkedIn: www.linkedin.com/in/carlos-roque-692b07239

---

*Thanks for reading — and I hope you find this project useful!*
