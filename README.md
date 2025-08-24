# 🩺 Heart Disease Data Analysis

## 📌 Project Overview
This project analyzes patient health records to identify factors associated with **heart disease**.  
The dataset includes demographic, clinical, and lifestyle features, and the goal is to understand patterns and correlations that influence the presence of heart disease.

---

## 1️⃣ Dataset Overview
- **File:** `heart.csv`  
- **Shape:** (rows × columns) → Contains patient health records.  
- **Features:**
  - Age
  - Sex
  - Chest Pain Type (cp)
  - Resting Blood Pressure (RestingBP)
  - Cholesterol
  - Fasting Blood Sugar (FBS)
  - ECG Results (RestECG)
  - Max Heart Rate (MaxHR / thalach)
  - Exercise-induced Angina (exang)
  - Oldpeak (ST depression)
  - Slope of ST segment
  - Major Vessels (ca)
  - Thalassemia (thal)
  - **Target** → Heart disease presence (1 = Yes, 0 = No)

---

## 2️⃣ Data Quality Check
✔ No missing values found  
✔ No duplicate rows after cleaning  
✔ Data types are consistent (`int`, `float`, and categorical)  

---

## 3️⃣ Exploratory Data Analysis (EDA)
- **Age Distribution:** Most patients are between **40–60 years old**.  
- **Gender:** Higher proportion of **male patients** in the dataset.  
- **Chest Pain Type:** Certain pain types strongly linked to heart disease.  
- **Resting BP & Cholesterol:** Wide variation; extreme outliers handled.  
- **Max Heart Rate (thalach):** Patients with heart disease tend to have **lower max HR**.  
- **Oldpeak:** Higher ST depression correlates with higher chance of heart disease.  

---

## 4️⃣ Correlation Analysis
Target (heart disease) is most correlated with:  
- Chest Pain Type (`cp`)  
- Exercise-induced Angina (`exang`)  
- ST Depression (`oldpeak`)  
- Slope of ST Segment (`slope`)  
- Maximum Heart Rate (`thalach`)  

📊 Heatmaps & pairplots confirm relationships between numeric features and target.  

---

## 5️⃣ Data Preprocessing
- **Categorical encoding:** `pd.get_dummies()` used for categorical variables.  
- **Boolean conversion:** Converted to `0/1`.  
- **Scaling:** Applied `StandardScaler` to numeric features (`Age`, `RestingBP`, `Cholesterol`, `MaxHR`, `Oldpeak`).  

---

## 6️⃣ Key Insights
- Patients with **typical angina** and **higher MaxHR** are **less likely** to have heart disease.  
- Patients with **exercise-induced angina**, **high oldpeak**, and **abnormal ECG results** are **more likely** to have heart disease.  
- **Lifestyle factors** such as cholesterol and resting BP influence risk, but weaker predictors compared to ECG, angina, and oldpeak.  

---

## 📂 Repository Structure
