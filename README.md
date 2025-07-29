# ICU Length of Stay Prediction for Spinal Cord Injury Patients

This project focuses on predicting **ICU Length of Stay (LOS)** for patients with **acute traumatic spinal cord injury (SCI)**, with a specific focus on **cervical spinal cord injuries** (ICD-9 codes: 806.0–806.09). Using the **MIMIC-III dataset**, which contains de-identified ICU patient records, the project explores the relationship between patient demographics, diagnostic codes, treatments, and ICU stays. The goal is to achieve more accurate predictions compared to the **traditional APACHE-IV model**, which has shown limited predictive power (R² = 0.05–0.28) for trauma patients.

---

## **Features**
- **Data Preparation & Cleaning**
  - Integrated data from multiple MIMIC-III tables (e.g., ICU stays, diagnoses, procedures).
  - Handled missing values, duplicates, and standardized date formats.
  - Performed feature engineering, including calculating ventilator duration and encoding categorical variables.

- **Exploratory Data Analysis (EDA)**
  - Visualized distributions of ICU LOS and diagnostic code frequencies.
  - Explored ICU LOS by admission type, location, and primary vs. secondary diagnosis roles.
  - Analyzed trends by age group and diagnosis severity.

- **Model Development**
  - **Linear Regression Model**: Achieved an R² of 0.472 and MAE of 5.4 days on log-transformed LOS data.
  - **Neural Network Baseline**: Built a 3-layer sequential model (R² ≈ 0.21, MAE ≈ 7.3 days).
  - Compared both models against the APACHE-IV baseline and analyzed key predictors (e.g., LOS_ADM_DAYS, age, ICU type).

---

## **Key Findings**
- **Linear Regression** explained ~47% of LOS variance, outperforming the APACHE-IV model.
- **Significant predictors** included:
  - LOS_ADM_DAYS (hospital stay duration)
  - Age (older patients tend to have longer ICU stays)
  - Cervical SCI diagnosis codes (806.0–806.09)
- **Neural Networks** provided a baseline but need more data and feature engineering for better performance.
- Emergency admissions correlated with longer ICU stays compared to elective admissions.

---

## **Applications**
- **Healthcare Resource Planning**: More accurate LOS prediction allows for better ICU bed and staff allocation.
- **Clinical Decision Support**: Identifies high-risk patients requiring extended care.
- **Model Benchmarking**: Offers a foundation for improving LOS prediction models using structured and unstructured EHR data.

---
