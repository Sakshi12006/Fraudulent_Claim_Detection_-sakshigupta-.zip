# Insurance Fraudulent Claim Detection 🛡️
> **A Predictive Modeling approach to identify fraudulent insurance claims for Global Insure.**

## **Project Overview**
Global Insure faces significant financial losses due to fraudulent claims. This project aims to automate the detection process using Machine Learning, replacing time-consuming manual inspections with a data-driven "first-filter" system. 



## **Problem Statement**
The goal is to classify insurance claims as **Fraudulent** or **Legitimate**. The challenge lies in the imbalanced nature of the data and the critical need for high **Recall (Sensitivity)** to ensure actual fraud is detected.

## **Project Pipeline**

### **1. Exploratory Data Analysis (EDA)**
* Analyzed categorical features like `incident_type` and `collision_type`.
* Identified **'Major Damage'** as the strongest indicator of potential fraud.
* Visualized demographic distributions and claim amounts to identify risk patterns.

### **2. Data Preprocessing & Feature Engineering**
* **Missing Value Imputation:** Handled hidden `?` values using statistical modes.
* **Feature Transformation:** Applied One-Hot Encoding and Standard Scaling.
* **Handling Multicollinearity:** Used **VIF Analysis** and **RFE** to remove redundant features.
* **Class Imbalance:** Utilized Random Over-Sampling to balance the training set.

### **3. Model Building & Evaluation**
* **Logistic Regression:** Baseline statistical model.
* **Tuned Random Forest (Final Model):** Optimized using Grid Search CV to capture non-linear interactions.

## **Results & Insights**
* **Accuracy:** 75.5%
* **Sensitivity (Recall):** 0.53 (Successfully identifying 53% of all fraud cases).
* **Specificity:** 0.83 (Maintaining high efficiency for legitimate customers).
* **Key Drivers:** `incident_severity`, `total_claim_amount`, and `age`.



## **📂 Repository Structure**
* [**data/**](./data/): Raw and processed CSV files.
* [**docs/**](./docs/): PowerPoint presentation and project summary.
* [**notebooks/**](./notebooks/): Jupyter Notebooks containing the full Python implementation.

## **Conclusions**
The **Tuned Random Forest** model doubled the detection rate of fraudulent claims compared to the baseline. This allows Global Insure to automate the audit of the vast majority of claims, focusing resources only on high-risk cases.
