

# 📊 Telco Customer Churn Prediction (Big Data ML Project)

## 🚀 Project Overview

This project builds an end-to-end **Customer Churn Prediction system** using:

- Apache Spark (Distributed ML)
- PySpark MLlib
- SHAP (Model Explainability)
- Hybrid Spark + Scikit-learn workflow

The objective is to identify customers likely to churn and explain *why* they are at risk.

---

## 🏗 Architecture

Spark is used for:
- Data preprocessing
- Feature engineering
- Model training
- Distributed scalability

Scikit-learn + SHAP is used for:
- Model interpretability
- Global and local feature impact analysis

Spark (Distributed Training) ↓ Sample Dataset ↓ Sklearn Model ↓ SHAP Explainability

---

## 📂 Dataset

**Telco Customer Churn Dataset**

Features include:
- Demographics
- Contract type
- Internet services
- Payment methods
- Monthly & total charges

Target variable:
- `Churn` (Yes/No)

---

## 🔎 Data Preprocessing

- Converted `TotalCharges` from string → double
- Handled missing values
- Created numeric label (0/1)
- One-hot encoded categorical features
- Assembled feature vector

---

## 🤖 Model Training (Spark)

Model used:
- Logistic Regression
- Random Forest (for better performance)

Train/Test split:
- 80/20 random split

Evaluation Metric:
- AUC (Area Under ROC Curve)

---

## 📊 Explainability (SHAP)

Two levels of explanation:

### 1️⃣ Global Explanation
- SHAP Summary Plot
- Identifies top churn drivers

Key Drivers Identified:
- Short tenure
- Electronic check payment method
- Fiber optic internet
- Month-to-month contracts

---

### 2️⃣ Local Explanation
- SHAP Waterfall Plot
- Explains individual customer churn probability

Example:
Baseline churn probability: 25.8%  
Predicted churn probability: 61.7%

Main contributing factors:
- Tenure = 1 month
- Electronic check payment
- Low total charges

---

## 📈 Key Business Insights

- Customers with short tenure are high risk
- Long-term contracts reduce churn
- Electronic check payments correlate with churn
- High monthly charges increase churn risk

These insights can drive:
- Retention campaigns
- Contract upgrades
- Payment method incentives

---

## 💾 Model Persistence

Spark model saved to:

hdfs:///models/churn_model

or locally:

/home/user/churn_model

---

## 🛠 Technologies Used

- Apache Spark 3.x
- PySpark MLlib
- Python 3.10
- Scikit-learn
- SHAP
- Pandas
- Matplotlib
- Hadoop (YARN)

---

## 📊 Sample Results

- AUC Score: ~0.80 (varies slightly)
- Clear separation between high-risk and low-risk customers
- Explainable predictions at customer level

---

## 🔥 Production Considerations

- Model scalable on YARN cluster
- Explainability performed on sampled data
- SHAP values can be stored in Hive for dashboards
- Can integrate with batch scoring pipelines

---

## 📌 Future Enhancements

- Cost-sensitive churn optimization
- Lift and gain chart analysis
- Real-time scoring pipeline
- Model monitoring & drift detection
- Deployment via REST API

---

## 👨‍💻 Author

Big Data ML Engineer  
Specialized in Spark-based distributed machine learning pipelines

---

## ⭐ Why This Project Matters

This project demonstrates:

✔ Distributed ML at scale  
✔ Real-world business problem solving  
✔ Model interpretability  
✔ Production-aware architecture  



<img width="1840" height="592" alt="image" src="https://github.com/user-attachments/assets/57c3b2ae-885b-49e7-8900-ec658dca6821" />
<img width="1840" height="592" alt="image" src="https://github.com/user-attachments/assets/2267b9ec-79be-4d6a-b7e5-ffcc459a481c" />
