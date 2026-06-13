# Heart Disease Classification

## Project Overview

This project aims to build a Machine Learning model capable of predicting whether a patient is likely to have heart disease based on various clinical and demographic attributes.

The project follows an end-to-end Machine Learning workflow including:

- Data Understanding
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Feature Analysis
- Model Building
- Hyperparameter Tuning
- Model Evaluation

---

## Problem Statement

Heart disease is one of the leading causes of death worldwide. Early prediction can assist healthcare professionals in identifying high-risk patients and making informed clinical decisions.

The objective of this project is to classify whether a patient has heart disease (`target = 1`) or does not have heart disease (`target = 0`) using patient health data.

---

## Dataset Information

The dataset contains patient-level clinical information such as:

| Feature | Description |
|----------|------------|
| age | Age of the patient |
| sex | Gender of the patient |
| cp | Chest pain type |
| trestbps | Resting blood pressure |
| chol | Serum cholesterol level |
| fbs | Fasting blood sugar |
| restecg | Resting ECG results |
| thalach | Maximum heart rate achieved |
| exang | Exercise induced angina |
| oldpeak | ST depression induced by exercise |
| slope | Slope of peak exercise ST segment |
| ca | Number of major vessels colored by fluoroscopy |
| thal | Thalassemia |
| target | Heart disease diagnosis (0 = No, 1 = Yes) |

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

### Data Inspection

- Dataset shape analysis
- Data types validation
- Summary statistics
- Missing value verification

### Univariate Analysis

- Target variable distribution
- Age distribution
- Clinical feature distributions

### Bivariate Analysis

- Age vs Heart Disease
- Sex vs Heart Disease
- Chest Pain Type vs Heart Disease
- Age vs Maximum Heart Rate

### Correlation Analysis

- Correlation Matrix
- Heatmap Visualization
- Feature Relationship Assessment

### Outlier Detection

Outlier detection was performed using:

- Boxplots
- Interquartile Range (IQR) Method

#### Findings

| Feature | Outliers Detected |
|----------|------------------|
| age | 0 |
| trestbps | 9 |
| chol | 5 |
| thalach | 1 |
| oldpeak | 5 |

Since this is a medical dataset, detected outliers may represent genuine patient conditions rather than data-entry errors. Therefore, they were retained for further analysis.

---

## Project Structure

```text
heart-disease-classification/
│
├── data/
│   └── heart-disease.csv
│
├── notebooks/
│   └── Heart_Disease_EDA.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

---

## Current Status

✅ Data Understanding Completed

✅ Exploratory Data Analysis Completed

✅ Correlation Analysis Completed

✅ Outlier Detection Completed

🔄 Model Building In Progress

⏳ Hyperparameter Tuning

⏳ Model Evaluation

⏳ Final Prediction Pipeline

---

## Future Improvements

- Build baseline classification models
- Perform hyperparameter tuning
- Evaluate models using ROC-AUC and cross-validation
- Analyze feature importance
- Create a prediction pipeline
- Deploy the model as a web application

---

## Author

Lalu

Machine Learning Engineer (Aspiring)