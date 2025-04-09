![Screenshot 2025-04-08 132902](https://github.com/user-attachments/assets/39c4e0e9-b718-48c1-af8a-81be053bf363)



# Fraudulent-Claim-Detection-Case-Study 🚨📊

## Overview 🌟
Global Insure, an insurance company processing thousands of claims annually, faces significant financial losses due to fraudulent claims. The current manual fraud detection process is inefficient and often detects fraud too late. This project aims to enhance fraud detection by leveraging historical claim data and customer profiles to build a predictive model that classifies insurance claims as either **fraudulent** or **legitimate**. By identifying patterns and key indicators of fraud early in the approval process, the model helps minimize financial losses and optimize claims handling. 💼🔍

## Goal 🎯
The primary goal is to develop a data-driven solution that:
- Analyzes historical claim data to detect patterns indicative of fraudulent claims. 📈
- Identifies the most predictive features of fraudulent behavior. 🔑
- Predicts the likelihood of fraud for incoming claims based on past data. ⚡
- Provides actionable insights to improve the fraud detection process. 🛠️

Ultimately, the model uses features like claim amounts, customer profiles, claim types, and approval times to predict fraudulent claims before they are approved, enabling proactive fraud prevention. 🚀

---

## Project Objectives ❓
1. **Pattern Detection**: How can we analyze historical claim data to detect patterns that indicate fraudulent claims? 🕵️‍♂️
2. **Feature Importance**: Which features are the most predictive of fraudulent behavior? 🌟
3. **Fraud Prediction**: Based on past data, can we predict the likelihood of fraud for an incoming claim? 📅
4. **Process Improvement**: What insights can be drawn from the model to improve the fraud detection process? 💡

---

## Methodology 🛠️
The project follows the **CRISP-DM** methodology:
1. **Business Understanding**: Emphasis on recall as a key metric for fraud detection. ✅
2. **Data Preparation**: Processed and prepped data for analysis. 🧹
3. **Data Cleaning**: Handled missing values and corrected data types. 🧼
4. **Data Splitting**: Divided data into training and validation sets. ✂️
5. **Exploratory Data Analysis (EDA)**: Analyzed patterns and distributions. 📊
6. **Feature Engineering**: Created new features to enhance performance. 🛠️
7. **Model Building**: Developed **Logistic Regression** and **Random Forests**. 🤖
8. **Feature Selection**: Used RFECV and Feature Importance. 🔍
9. **Model Fine-Tuning**: Optimized cutoffs and hyperparameters with GridSearchCV. ⚙️
10. **Model Evaluation**: Assessed performance with Accuracy, Recall, and F1-Score. 📏

### Techniques Used 🧪
- **Data Preprocessing**: One-Hot Encoding, Feature Scaling (StandardScaler). 🔢
- **Model Building**: Logistic Regression, Random Forests. 🧠
- **Optimization**: Accuracy/Sensitivity/Specificity Cutoff Graph, GridSearchCV. 🎛️
- **Evaluation Metrics**: Accuracy, Confusion Matrix, Recall. 📈

---

## Results 🏆
Since the goal is to detect fraudulent claims, **Recall** is the most critical metric. Here’s a comparison of the two models:

| Model              | Accuracy (Train) | Recall (Train) | Accuracy (Validation) | Recall (Validation) |
|--------------------|------------------|----------------|-----------------------|---------------------|
| Logistic Regression| 86.6% ✅         | 87.3% 🌟       | 84% ✅                 | **90.5%** 🥇        |
| Random Forests     | 90.4% ✅         | 93.3% 🌟       | 77.7% ⚠️              | 75.7% ⚖️           |

**Logistic Regression** outperformed Random Forests with a **90.5% Recall** on the validation set, making it the preferred model for fraud detection. 🎉

### Significant Features 🌟
The Logistic Regression coefficients highlight key predictors:
- **insured_hobbies_chess**: +4.2153 (🚨 Fraud risk up!)
- **insured_hobbies_cross-fit**: +3.5445 (🚨 Fraud risk up!)
- **insured_hobbies_dancing**: -22.7954 (✅ Fraud risk down!)
- **incident_severity_Minor Damage**: -3.4093 (✅ Fraud risk down!)
- **incident_severity_Total Loss**: -3.2046 (✅ Fraud risk down!)

**Regression Equation**:  
```
1.5584 + 4.2153(insured_hobbies_chess) + 3.5445(insured_hobbies_cross-fit) - 22.7954(insured_hobbies_dancing) - 3.4093(incident_severity_Minor Damage) - 3.2046(incident_severity_Total Loss)
```

---

## Key Insights 💡
1. **Customer Tenure**: Fraudulent claims are more frequent among newer customers. ⏳
2. **Age**: Younger customers (below 30) are more prone to fraud. 👶
3. **Policy Deductible**: Lower deductibles correlate with higher fraud risk. 💸
4. **Hobbies**: Chess and CrossFit signal fraud, while dancing suggests legitimacy. 🎲🏋️‍♂️💃
5. **Claim Severity**: Minor damage and total loss claims are less likely fraudulent. 🚗

![Screenshot 2025-04-08 121921](https://github.com/user-attachments/assets/516231ad-752f-4578-b27a-ab4834445ed1) 
*The ROC curve shows an AUC of 0.88, indicating strong performance!* 📈

---

## Recommendations 📋
1. **Flag High-Risk Claims**: Scrutinize claims with chess or CrossFit hobbies. 🚩
2. **Streamline Low-Risk Claims**: Fast-track minor damage and dancing-related claims. ⚡
3. **Adjust Fraud Focus**: Prioritize claims without total loss or minor damage. 🎯

---

## How to Use This Repository 🖥️
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/fraudulent-claim-detection.git
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Model**:
   - Explore the Jupyter notebooks in `notebooks/` for EDA and modeling. 📓
   - Use pre-trained models from the `models/` folder. 🤖

---

## Repository Structure 📂
```
fraudulent-claim-detection/
├── data/                  # Dataset files  📊
├── notebooks/             # Jupyter notebooks for EDA and model building 📓
├── models/                # Pre-trained Logistic Regression and Random Forest models 🤖
├── images/                # Images used in README and notebook 🖼️
└──README.md               # Project overview and instructions 📝
 
```

---

## 🎯 **Project Overview**

This repository is part of an ongoing assignment for the **Postgraduate Certification in Data Science, Machine Learning, and AI** from **IIIT Bangalore & UpGrad**.  

📚 **Case Study:** Lead Scoring for **X Education**, an online course-selling platform. 

👥 **Team Members:** [Rohit Vashishth](https://www.linkedin.com/in/rohit-vashishth-2724a81b/) , [Rakesh Kumar Sahoo](https://www.linkedin.com/in/rakeshkumarsahoo23/) , [Saurab Singh](https://www.linkedin.com/in/saurabh-singh-778390193/) & [Sandeep Santhosh]()

🏫 **Institution:** [IIIT Bangalore](https://www.iiitb.ac.in/) in collaboration with [UpGrad](https://www.upgrad.com/).  

---

## License 📜
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Badges for Visual Appeal
![Python](https://img.shields.io/badge/Python-3.8-blue) ![License](https://img.shields.io/badge/License-MIT-green) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---
