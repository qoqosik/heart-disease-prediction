# Heart Disease Prediction Using Machine Learning

This project was developed as part of the **Veri Analizi** course.  
The objective is to apply data analysis and machine learning techniques to predict the presence of heart disease based on patient medical data.

---

## 📊 Dataset

- **Source:** Kaggle – Heart Disease Dataset  
- **Observations:** 1025  
- **Features:** 13 input features + 1 target variable  
- **Target:** Binary classification  
  - `1` — Presence of heart disease  
  - `0` — No heart disease  
- **Missing values:** None  
- **Class balance:** Nearly balanced  

---

## 🎯 Problem Definition

The task is formulated as a **binary classification problem**, where the goal is to predict whether a patient has heart disease based on clinical and demographic attributes.

This is a medically important problem, as minimizing false negatives (undetected disease cases) is critical in healthcare applications.

---

## 🧪 Exploratory Data Analysis (EDA)

During EDA, the dataset was analyzed using:
- Descriptive statistics
- Target variable distribution
- Correlation analysis
- Data visualizations (heatmaps and plots)

Key insights:
- Features such as `cp`, `thalach`, and `slope` show positive correlation with heart disease.
- Features like `exang`, `oldpeak`, `ca`, and `thal` show negative correlation with the target variable.

---

## ⚙️ Data Preprocessing

- Feature and target separation
- Train-test split
- Feature scaling where appropriate
- No missing value handling or encoding was required, as the dataset was already clean and numerical

---

## 🤖 Machine Learning Models

The following models were implemented and evaluated:

### 1. Logistic Regression
- Used as a baseline model
- Interpretable and effective for structured medical data

### 2. Random Forest
- Ensemble learning method
- Capable of capturing non-linear relationships

---

## 📈 Model Evaluation

Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Special emphasis was placed on **recall for class 1**, as detecting patients with heart disease is more important than avoiding false positives.

---

## 🏆 Results & Comparison

- **Logistic Regression** achieved higher overall accuracy and significantly better recall for heart disease cases.
- **Random Forest** showed higher precision but lower recall.

Based on these results, **Logistic Regression** was selected as the most suitable model for this task.

---

## 🧾 Project Structure

