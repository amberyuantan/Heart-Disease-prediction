# 🩺 Heart Disease Prediction with Random Forest

This project aims to predict the likelihood of heart disease based on health indicators using machine learning techniques. The dataset originates from the **CDC**, which collects annual health-related data. The primary focus is on using **Random Forest** for classification, complemented by data preprocessing, visualization, and performance evaluation.

---

## 🚀 Project Overview

### Goals
-  Predict whether an individual has heart disease based on various health indicators.
-  Handle class imbalance issues in the dataset.
-  Evaluate model performance using robust metrics such as ROC-AUC, accuracy, and classification reports.

### Dataset
- **Source**: CDC Behavioral Risk Factor Surveillance System (BRFSS)
- **Size**: 
  - Rows: 246,022
  - Columns: 40
- **Features**: Includes demographic information, health behaviors, and medical history.
- **Target Variable**: `HeartDisease` (Binary: 1 = Yes, 0 = No)

---

## 🔨 Workflow

### Data Preparation 
- Dropped unnecessary columns (`State`, `Sex`).
- Transformed target variable (`HeartDisease`) based on conditions.
- Encoded categorical features using `OneHotEncoder`.
- Balanced data using **SMOTE** and **Random Under-Sampling**.

### Data Visualization
- Explored the distribution of the target variable with a pie chart.
- Analyzed correlations between numerical features using a heatmap.

### Model Development
- **Baseline Model**: Used `DummyClassifier` for a simple performance benchmark.
- **Random Forest Classifier**: Built a pipeline that integrates preprocessing and model training:
  - Preprocessing: One-hot encoding for categorical features and MinMax scaling for numerical features.
  - Model: Random Forest with 10 estimators.

### Model Evaluation
- Metrics:
  - Accuracy
  - Cross Validation Score

---

## 📈 Results

### Baseline Model
- **Accuracy**: 91%
- **Strategy**: Predicted the majority class for all samples.

### Random Forest Model
#### Resampled Data
- **Cross-Validation ROC-AUC**: ~0.98
- **Key Metrics**:
  - Balanced precision and recall


