# Attrition-Prediction-ML-Project
Machine Learning Model Performance Analysis for Employee Attrition


---

## 🚀 Steps Performed

### **1️⃣ Load & Prepare Dataset**
- Cleaned missing values  
- Removed irrelevant features (e.g., EmployeeNumber)  
- Encoded categorical columns  

### **2️⃣ Visual Exploration**
Created Flourish visual narratives:
✔ Attrition vs Job Satisfaction  
✔ Attrition vs Overtime  
✔ Histograms & employee patterns  

📌 **Flourish Story Link:**  
https://public.flourish.studio/story/3459871/

---

## 🧠 Models Used & Performance Summary

### **✔ J48 (Decision Tree)**
- Training Accuracy: **72.93%**
- Cross-Validation Accuracy: **50.81%**
- **Overfitting detected** (large gap between train vs CV)

### **✔ Naive Bayes**
- Impacted by **class imbalance**
- Learned majority class more strongly

### **✔ Random Forest**
- Accuracy: **27.41%**
- **Underfitting**, mainly due to:
  - Class imbalance  
  - Presence of irrelevant attributes  
  - Lack of tuning

### **✔ ZeroR**
- Always predicts majority class  
- Baseline underfitting model

---

## ⚠ Key Issues Identified

### **1. Overfitting**
Especially in J48 (very large tree – 2247 nodes)

### **2. Underfitting**
Random Forest and ZeroR failed to capture useful patterns.

### **3. Class Imbalance**
Attrition = "Yes" is very small → models biased toward "No".

### **4. Irrelevant Features**
EmployeeNumber caused useless splits → removed in later trials.

---

## 🔍 Key Factors Behind Attrition
From visual & model-based insights:

- Low job satisfaction  
- Poor work-life balance  
- Lower salary  
- Lack of growth opportunities  
- Long overtime  
- Short tenure  

---

## 🛠 Recommendations for Model Improvement
- Apply **SMOTE / Oversampling**  
- Remove irrelevant features  
- Hyperparameter tuning  
- Use **ROC, F1-score** instead of accuracy  
- Try **XGBoost, Logistic Regression, SVM**

---

## 📈 HR Use-Case Recommendations
HR teams can:
- Identify high-risk employees early  
- Improve work-life balance  
- Increase promotion & learning opportunities  
- Adjust compensation strategies  
- Create department-specific retention plans  

---

## 📂 Final Dataset
Google Sheets:  
https://docs.google.com/spreadsheets/d/1FvJYP03OPrZUGc3dTIgn6uXQWM7MtOs21azyTC5QoO0/edit?usp=sharing

---

## 👨‍💻 Author  
**Abduttaiyeb Huseni Matcheswala**  
BSc Applied AI & Data Engineering (b24bs1015)

---

## ⭐ If you found this project useful, feel free to ⭐ star the repo!
