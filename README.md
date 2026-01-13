# 📡 Telecom Churn Prediction (Interconnect)

## 📋 Project Description
 The telecom operator **Interconnect** aims to forecast its customer churn rate to identify users planning to leave. The main goal is to offer promotional codes and special plan options to these users, thereby maximizing retention.

This project utilizes Machine Learning models to predict churn probability based on contract data, personal characteristics, and subscribed services.

## 🛠️ Tools & Technologies
* **Python** (Pandas, NumPy, Matplotlib, Seaborn)
* **Machine Learning:** Scikit-learn, LightGBM, XGBoost
* **Techniques:** Upsampling, Downsampling, GridSearchCV, Cross-Validation

## 📊 Methodology

1.  **Data Preprocessing:**
    * Cleaning missing values and type conversion.
    * Feature Engineering: Categorical variable transformation ('Yes'/'No' to 1/0) and One-Hot Encoding (OHE).
    * Scaling of numerical variables.
2.  **Exploratory Data Analysis (EDA):**
    * Identified that customers with "month-to-month" contracts and "electronic check" payments have the highest churn rates.
    * 1 or 2-year contracts show significantly higher loyalty.
3.  **Modeling:**
    * Tested: Decision Tree, Random Forest, XGBoost, and LightGBM.
    * Addressed class imbalance using **Upsampling** and Downsampling techniques.

## 📈 Final Model Results
The best performing model was **LightGBM with Upsampling**, outperforming XGBoost and baseline models.

| Metric | Result |
| :--- | :--- |
| **AUC-ROC** | **0.93** |
| Accuracy | 88.29% |
| F1 Score | 0.78 |

> **Technical Conclusion:** Upsampling consistently improved performance across all models compared to downsampling. LightGBM offered the best balance between training speed and predictive metrics.

## 💡 Business Insights & Recommendations
Based on the model findings, the following strategies are suggested to the Marketing team:

1.  **Incentivize Long-Term Contracts:** Month-to-month contracts are the biggest risk factor.
2.  **Encourage Automatic Payments:** Users paying via electronic check tend to churn more. Migrating them to automatic payments could reduce friction.
3.  **Early Retention Programs:** Most churn occurs in the first few months. Implementing aggressive onboarding programs during the first quarter is recommended.

## ⚠️ Challenges Faced
* **Class Imbalance:** The number of retained customers was much higher than those who churned. This was successfully resolved using *Upsampling* techniques, which significantly boosted the F1 Score.
* **Categorical Encoding:** Converting categorical columns without causing dimensionality explosion required careful cleaning and feature selection.

---
*Project developed by [Jefferson Torres Mangier] as part of the TripleTen Data Science Bootcamp.*
