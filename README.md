# HR Attrition Prediction – Machine Learning Model Performance Analysis

This repository contains my mini-project for the **BSc Applied AI & Data Engineering** program. The goal of this project is to analyze how different machine learning models perform in predicting **employee attrition**, identify issues like overfitting and class imbalance, and discover the major factors influencing employees to leave.

This project uses the IBM HR dataset along with visual exploration, WEKA-based modeling, and automated AI summarization.

---

## 📁 Project Structure

```
Attrition-Prediction-ML-Project/
│── README.md
│── mp.pdf
│── mp.docx
│── images/
│── data/
│── src/
│── notebooks/
```

---

# 🚀 Project Workflow

## 1️⃣ Load the Dataset  
Imported the HR dataset and inspected structure, missing values, and data types.

---

## 2️⃣ Clean & Prepare the Dataset  
- Removed irrelevant columns like `EmployeeNumber`  
- Encoded categorical values  
- Verified class imbalance  
- Checked distributions  

---

## 3️⃣ Convert CSV to ARFF (Optional for WEKA)

---

## 4️⃣ Load Dataset Into WEKA  
Used WEKA Explorer for pre-processing and model building.

---

## 5️⃣ Exploratory Analysis & Visualization  
Generated visual insights such as:

- Attrition vs Job Satisfaction  
- Attrition vs OverTime  
- Histograms & categories  
- Employee distribution patterns  

### 📊 Visual Story  
**Flourish Dashboard:** https://public.flourish.studio/story/3459871/

---

## 6️⃣ Create Visual Narratives (Flourish)

---

## 7️⃣ Train Baseline Model (J48 Decision Tree)
- Training Accuracy: **72.93%**  
- Cross-Validation Accuracy: **50.81%**  
- **Conclusion: Overfitting observed**

---

# 🤖 Model Performance Summary

### ✔ J48 Decision Tree
- Strong performance on training set  
- Poor generalization  
- Large tree size → overfitting  

---

### ✔ Naive Bayes  
- Impacted by **class imbalance**  
- Predicts majority class more often  
- Weak recall for attrition cases  

---

### ✔ Random Forest  
- Accuracy: **27.41%** (underfitting)  
- Affected by:
  - Irrelevant features  
  - Class imbalance  
  - Lack of tuning  

---

### ✔ ZeroR (Baseline)
- Predicts only majority class  
- Extreme underfitting  
- Useful only as a reference baseline  

---

# ⚠ Key Issues Identified

### 🔸 Overfitting  
J48 tree is too large and too specific.

### 🔸 Underfitting  
Random Forest & ZeroR cannot capture meaningful relationships.

### 🔸 Class Imbalance  
Majority class dominates (Attrition = No).

### 🔸 Irrelevant Features  
IDs like EmployeeNumber reduce learning quality.

---

# 📝 Summarizing Insights Using Napkin.ai

To convert technical outputs into clear English insights, I used **Napkin.ai**, which generated a high-level summary of model behavior.

### 📄 Napkin Summary Link  
https://app.napkin.ai/page/CgoiCHByb2Qtb25lEiwKBFBhZ2UaJDc5ZDE5MDc3LWMxMjUtNGEyMi1hNWZhLWY3NDQ2ODEyMmVhNA?s=1

### 🔍 Napkin Summary Highlights  
- J48 overfitted heavily.  
- Random Forest & ZeroR underfitted because of imbalance and noise.  
- Class imbalance was a major blocker.  
- Removing EmployeeNumber improves learning.  
- Recommended:
  - SMOTE / Oversampling  
  - Cost-sensitive learning  
  - Hyperparameter tuning  
  - Feature selection  
- Key attrition factors:
  - Low job satisfaction  
  - Overtime workload  
  - Salary issues  
  - Promotion scarcity  
  - Poor work-life balance  
  - Short tenure  

Napkin helped convert raw metrics into **HR-friendly insights**.

---

# 🔍 Key Factors Driving Attrition

- Low job satisfaction  
- Long overtime hours  
- Work-life imbalance  
- Short tenure  
- Limited promotions  
- Lower salary bands  

---

# 🎯 Recommendations for Model Improvement

### ✔ Fix Class Imbalance  
- SMOTE  
- Undersampling  
- Weighted classifiers  

### ✔ Remove Noise Features  
Eliminate EmployeeNumber, EmployeeCount, Over18, StandardHours, etc.

### ✔ Tune Hyperparameters  
Improve Random Forest & J48 performance.

### ✔ Use Better Evaluation Metrics  
Accuracy is misleading → use:
- F1-score  
- Recall  
- ROC-AUC  

---

# 🏢 HR Recommendations Based on Findings

- Identify high-risk employees early  
- Improve promotion and career pathways  
- Improve compensation fairness  
- Provide workload and overtime balance  
- Apply department-level retention plans  

---

# 📂 Dataset Used  
Google Sheets dataset:  
https://docs.google.com/spreadsheets/d/1FvJYP03OPrZUGc3dTIgn6uXQWM7MtOs21azyTC5QoO0/edit?usp=sharing

---

# 👨‍💻 Author  
**Abduttaiyeb Huseni Matcheswala (b24bs1015)**  
BSc Applied AI & Data Engineering  

---

# ⭐ Support  
If you like this project, consider giving the repository a ⭐!
