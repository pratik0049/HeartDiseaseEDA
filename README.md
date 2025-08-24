🩺 Heart Disease Data Analysis
1. Dataset Overview

Dataset loaded: heart.csv

Shape: (rows × columns) → The dataset contains patient health records.

Features include Age, Sex, Chest Pain Type, Resting Blood Pressure, Cholesterol, Fasting Blood Sugar, ECG Results, Max Heart Rate, Exercise-induced Angina, Oldpeak (ST depression), Slope, Major Vessels, Thalassemia, and Target (heart disease presence).

2. Data Quality Check

No missing values were found.

No duplicates remain after cleaning.

Data types are consistent (int, float, and categorical).

3. Exploratory Data Analysis (EDA)

Age Distribution: Most patients are in the range of 40–60 years.

Gender: Higher proportion of male patients in the dataset.

Chest Pain Type (cp): Certain pain types are strongly associated with heart disease.

Resting BP & Cholesterol: Wide variation observed, but extreme outliers were removed/handled.

Max Heart Rate (thalach): Patients with heart disease tend to have lower max HR compared to healthy individuals.

Oldpeak: Higher ST depression values (Oldpeak) correlate with higher chance of heart disease.

4. Correlation Analysis

Target variable (Heart Disease) is most correlated with:

Chest pain type (cp)

Exercise-induced angina (exang)

ST depression (oldpeak)

Slope of ST segment (slope)

Maximum heart rate (thalach)

Heatmap & pairplots confirm relationships between numeric features and target.

5. Data Preprocessing

Categorical variables encoded with pd.get_dummies.

Booleans converted into 0/1.

Scaling applied to numeric variables (Age, RestingBP, Cholesterol, MaxHR, Oldpeak) using StandardScaler.

6. Key Insights

Patients with typical angina and higher max HR are less likely to have heart disease.

Patients with exercise-induced angina, high oldpeak, and abnormal ECG results show a higher chance of heart disease.

Lifestyle factors such as cholesterol and resting BP play a role but are weaker predictors compared to ECG, angina, and oldpeak.
