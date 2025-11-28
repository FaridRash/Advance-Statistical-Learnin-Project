# ALS Clinical Stage Prediction using Ordinal Regression

## 📌 Project Overview
This project focuses on predicting the clinical stage of Amyotrophic Lateral Sclerosis (ALS) patients based on King's Staging system. By analyzing clinical biomarkers and patient history (such as FVC), we aim to classify disease progression accurately. Given the ranked nature of the target variable (King's Stages 1-4), an **Ordinal Logistic Regression** approach was utilized instead of traditional classification methods to better capture disease severity.

## 🛠 Tech Stack & Libraries
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (StandardScaler, Metrics), Statsmodels (OrderedModel)
* **Data Augmentation:** Imbalanced-learn (SMOTE)

## ⚙️ Methodology
1.  **Data Preprocessing:**
    * Cleaning clinical data and handling missing values (e.g., in FVC).
    * Feature selection: Excluding identifiers and utilizing date-independent features.
    * Normalization using `StandardScaler` to standardize feature distributions.
2.  **Handling Imbalance:**
    * Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset, ensuring simpler clinical stages (Classes 1 & 2) are represented equally to advanced stages.
3.  **Modeling:**
    * Implemented **Ordinal Logistic Regression (GLM)** using `statsmodels`. This model is specifically chosen to respect the ordinal nature of disease stages (Stage 1 < Stage 2 < ...).
4.  **Evaluation:**
    * Assessed performance using **Accuracy**, **Mean Absolute Error (MAE)**, and **Confusion Matrix** to verify the model's ability to distinguish between adjacent stages.

## 📊 Results
The model demonstrates the capability to classify patient stages with consideration for the ordinal relationship between classes, providing a more medically interpretable result than standard multi-class classification.
