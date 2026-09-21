# Student Performance Analysis Using Machine Learning

## Project Overview

This project focuses on analyzing student-related data and predicting their **Grade Class** using a wide range of machine learning algorithms.

The dataset contains information about students such as **age, gender, ethnicity, study time, absences, tutoring, parental support, extracurricular activities, sports, volunteering, and GPA**.

Instead of relying on a single machine learning algorithm, this project evaluates multiple models on the same dataset to understand how differently they perform and which models are most suitable for predicting student performance.

The main focus of this project is **model comparison and evaluation**. Rather than comparing models only by accuracy, I also evaluate them using:

* Accuracy
* F1-score
* Sensitivity (Recall)
* Specificity
* ROC-AUC
* False Positive Rate (FPR)
* False Negative Rate (FNR)
* Confusion Matrix

This makes the comparison more informative and provides a better understanding of how each model handles different types of predictions.

---

## Dataset

The dataset was collected from **Kaggle** and contains student demographic, academic, and behavioral information.

### Main Features

* Age
* Gender
* Ethnicity
* Parental Education
* Study Time Weekly
* Absences
* Tutoring
* Parental Support
* Extracurricular Activities
* Sports
* Music
* Volunteering
* GPA
* Grade Class (Target)

The target variable is **Grade Class**, which represents the student's academic performance category.

---

## Project Workflow

The project follows a step-by-step machine learning workflow.

### 1. Data Collection

First, the dataset is loaded from Kaggle and prepared for analysis.

### 2. Initial Data Exploration

The dataset is explored using:

* First 5 rows
* Last 5 rows
* Dataset shape
* Dataset columns
* Dataset information
* Data types
* Statistical summary


This helps provide an initial understanding of the structure and characteristics of the dataset.

### 3. Data Quality Checking

Before training the models, the dataset is checked for common data-quality problems.

I specifically checked for:

* Missing values
* Duplicate rows

In this dataset, **no missing values or duplicate records were found**.

### 4. Exploratory Data Analysis

Several visualization techniques are used to understand relationships and patterns within the dataset.

The visualizations include:

* Count plots
* Histograms
* Scatter plots
* Box plots
* Correlation heatmap

The correlation heatmap is particularly useful for understanding relationships between numerical features and identifying potentially important variables.

### 5. Train-Test Split

The target variable, **Grade Class**, is separated from the input features.

The dataset is then divided into:

* **75% Training Data**
* **25% Testing Data**

Since this is a relatively small dataset, a separate validation set was not used in the initial experiment.

### 6. Model Training and Evaluation

A wide range of machine learning algorithms are trained and evaluated on the same dataset.

The models include:

#### Ensemble and Tree-Based Models

* Random Forest
* Gradient Boosting
* AdaBoost
* Bagging
* Extra Trees
* HistGradientBoosting
* Balanced Random Forest
* RUSBoost

#### Other Machine Learning Models

* Decision Tree
* Support Vector Machine (SVM)
* XGBoost
* CatBoost
* LightGBM
* Logistic Regression
* Naïve Bayes
* Linear Discriminant Analysis (LDA)
* Quadratic Discriminant Analysis (QDA)
* K-Nearest Neighbors (KNN)
* MLP Classifier

#### Ensemble Learning

Additional ensemble approaches are also explored, including:

* Voting Classifier
* Stacking Classifier

#### Deep Learning

A simple **Recurrent Neural Network (RNN)** is also included to compare its performance with traditional machine learning approaches.

---

## Model Comparison

One of the main goals of this project is to make model comparison simple and easy to understand.

Instead of looking at individual model outputs separately, the results are summarized in a single comparison table containing:

| Metric         | Description                                    |
| -------------- | ---------------------------------------------- |
| Training Score | Performance on training data                   |
| Test Score     | Performance on unseen test data                |
| Accuracy       | Overall prediction accuracy                    |
| F1-Score       | Balance between precision and recall           |
| Specificity    | Ability to correctly identify negative classes |
| Sensitivity    | Ability to correctly identify positive classes |
| ROC-AUC        | Overall classification performance             |
| FPR            | False Positive Rate                            |
| FNR            | False Negative Rate                            |

This allows the performance of all models to be compared quickly.

---

## Why Use So Many Machine Learning Models?

Using many models is intentional.

The goal is not simply to find a model with the highest accuracy. Instead, I wanted to understand:

* How different algorithms behave on the same dataset
* How ensemble models compare with individual models
* Whether a model performs consistently across different metrics
* How hyperparameter tuning affects model performance
* Which models generalize better to unseen data
* Whether the model with the highest accuracy is also the best model according to other evaluation metrics

This approach provides a broader view of the dataset and helps avoid selecting a model based on **accuracy alone**.

---

## Results

The experiments showed that different models performed best under different evaluation criteria.

**AdaBoost** achieved the strongest overall performance in several important metrics, with an accuracy of **93.14%**, F1-score of **93.01%**, and sensitivity of **93.14%**.

On the other hand, the **Decision Tree** achieved the highest specificity at **98.17%** and the lowest false positive rate (FPR) at **1.83%**.

**CatBoost** also performed very strongly, achieving **92.98% accuracy**, **92.97% F1-score**, and an impressive **ROC-AUC of 0.99**.

These results demonstrate an important point: **there is not always a single best model across every evaluation metric**.

For example, one model may provide better overall accuracy, while another may be better at minimizing false positives or identifying negative cases.

Therefore, the final model selection should depend on the specific objective of the application and which evaluation metric is most important.

---

## Key Takeaways

* Multiple machine learning algorithms were evaluated on the same student dataset.
* Ensemble models were given particular attention.
* Model performance was evaluated using more than just accuracy.
* AdaBoost achieved the highest accuracy, F1-score, and sensitivity in this experiment.
* Decision Tree achieved the highest specificity and lowest FPR.
* CatBoost achieved a very high ROC-AUC score of **0.99**.
* The results show that model selection should consider the **overall evaluation profile**, not a single metric.
* Confusion matrices and correlation analysis were used to provide additional insight into model behavior.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* CatBoost
* LightGBM
* TensorFlow / Keras
* Jupyter Notebook / Kaggle

---

## Future Improvements

Some possible improvements for future versions of this project include:

* Cross-validation for more reliable model evaluation
* More extensive hyperparameter optimization
* Feature selection
* Feature importance analysis
* SHAP-based explainability
* ROC curves for individual models
* Precision-Recall curves
* Class-wise performance analysis
* Model deployment using Streamlit
* Automated prediction for new student data

---

## Conclusion

This project was developed to explore how different machine learning algorithms perform when predicting student academic performance.

The main objective was not only to build a predictive model, but also to **compare, analyze, and understand the strengths and weaknesses of different algorithms**.

By combining exploratory data analysis, multiple machine learning approaches, ensemble learning, hyperparameter tuning, and detailed evaluation metrics, the project provides a more complete view of machine learning performance on student data.
