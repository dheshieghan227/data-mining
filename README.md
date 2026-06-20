# Obesity Level Classification & Prediction
## Data Mining & Predictive Modeling Project

This repository contains a comprehensive data mining project aimed at classifying and predicting obesity levels based on individual eating habits, physical conditions, demographics, and lifestyle factors.

---

## 📊 Project Overview
Obesity is a major public health challenge globally. This project leverages machine learning classification models to predict a person's obesity level based on key lifestyle indicators.

The dataset contains **2,111 records** of individuals with **45 initial attributes** (including one-hot encoded variables), which are cleaned, restructured, and mapped into a single nominal target attribute with 7 classification levels:
1. **Insufficient Weight**
2. **Normal Weight**
3. **Overweight Level I**
4. **Overweight Level II**
5. **Obesity Type I**
6. **Obesity Type II**
7. **Obesity Type III**

---

## 🛠️ Data Mining Pipeline & Source Code
The Jupyter Notebook (`/notebooks/project.ipynb`) walks through the entire pipeline:

### 1. Data Cleaning & Restructuring
- Strip whitespace and sanitize column headers.
- Consolidate one-hot encoded target columns (`Obesity_...`) into a single nominal column (`ObesityLevel_nominal`).
- Transform nominal classes into integer encodings (`ObesityLevel_encoded`) for modeling.

### 2. Feature Engineering & Scaling
- Feature columns include numerical values (Height, Weight, Age) and lifestyle indicators.
- Standardized scaling using `StandardScaler` is applied for algorithms sensitive to variance (like KNN).

### 3. Classification Models
Three machine learning classification models are implemented, tested, and evaluated:
- **K-Nearest Neighbors (KNN)** ($K=5$): Evaluated using standardized scaling.
- **Naïve Bayes (GaussianNB)**: Fast probabilistic model, achieving **53.94% overall accuracy**.
- **Decision Tree (DecisionTreeClassifier)**: Powerful non-linear classifier, achieving a high **92.43% overall accuracy** on unscaled features.

---

## 📂 Repository Structure
The project files are structured as follows:
```text
├───data
│       obesity.xls                                    # Original raw dataset
│       obesity_cleaned_and_restructured.xls           # Preprocessed and cleaned dataset
│
├───notebooks
│       project.ipynb                                  # Jupyter Notebook containing ETL & ML models
│
└───reports
        DATA_MINING_Project_1.pdf                      # Phase 1 Project Report (EDA & Preprocessing)
        DATA_MINING_Project_2.pdf                      # Phase 2 Project Report (Modeling & Evaluation)
```

---

## 📈 Evaluation Metrics
For each classifier, the project outputs:
- **Overall Classification Accuracy**
- **Transposed Confusion Matrix** (True vs. Predicted classes)
- **Class-Specific Precision**
- **Class-Specific Recall**
