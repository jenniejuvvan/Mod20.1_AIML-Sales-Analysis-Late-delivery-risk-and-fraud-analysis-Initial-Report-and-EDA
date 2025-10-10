# Mod20.1_AIML-Sales-Analysis-Late-delivery-risk-and-fraud-analysis-Initial-Report-and-EDA and Baseline model

## Introduction

## 📌 Executive Summary

This project focuses on building a Sales Fraud and Late Delivery Detection Model to strengthen supply chain integrity and operational efficiency. By leveraging transactional, regional, and customer-level data from a supply chain dataset, the project applies advanced anomaly detection techniques to identify fraudulent sales activity and late delivery risk patterns. In addition to analyzing customer and sales trends, fraud and late delivery risk pattern are studied to highlight risks in specific geographies, sales channels, and customer segments.

---

## 📌 Business Objective
The outcomes will support strategic decision-making by enabling the company to:

- Detect and mitigate fraudulent sales transactions before they impact revenue.
- Identify late delivery patterns and reduce operational inefficiencies.
- Enhance customer trust and satisfaction by proactively addressing anomalies.
- Reduce financial losses and reputational risks associated with fraud and delivery failures.

---
## 📌 Rationale

Understanding customer behavior is critical for businesses in a competitive marketplace. Fraudulent sales activities and late deliveries present significant challenges to businesses operating in competitive markets. Fraud directly leads to financial losses and inaccurate reporting, while delivery failures damage customer trust and loyalty. Detecting anomalies early allows organizations to implement corrective actions, strengthen internal controls, and optimize logistics strategies.

A fraud and late delivery detection framework helps address these challenges by:

- Pinpointing suspicious transactions through anomaly detection techniques.
- Predicting high-risk deliveries based on order, product, and regional attributes.
- Enhancing monitoring of geographic or product-specific vulnerabilities.
- Improving allocation of resources to fraud prevention and logistics optimization.

By solving this problem, the company can safeguard revenue, protect brand reputation, and improve customer experiences while minimizing risks in sales and delivery operations.

---

## 📌 Research Question

The central research question for this project is: “How can we detect and classify anomalies in sales transactions and delivery records to prevent fraud and reduce late deliveries across regions?”

**Supporting sub-questions:**

Which transaction, product, and delivery attributes most strongly signal fraud or anomalies? How do geographic and regional patterns influence fraud detection and late deliveries? What machine learning models are most effective at detecting fraud and delivery risks? How do preprocessing, feature engineering, and anomaly detection techniques impact model accuracy and interpretability?

## 📊 Dataset Overview
What data will you use to answer your question? The analysis uses the DataCo Supply Chain dataset, which includes detailed records of customer demographics, transactions, product sales, supply chain operations, and regional information.

**Specifically:**

- Customer Data: Demographics and segmentation details.
- Transaction Data: Sales amounts, order quantities, payment methods, and timestamps.
- Product Data: Categories, pricing, and supply chain attributes.
- Supply Chain Data: Order processing, shipping, delivery status, and lead times.
- Regional Data: Customer location and regional logistics performance.

The dataset used in this project is maintained transparently with the Creative Commons 4.0 license by Fabian Constante, Fernando Silva, and António Pereira through the Mendeley data repository. The dataset consists of roughly 180k transactions from supply chains used by the company DataCo Global for 3 years. This dataset provides a holistic view of customer interactions across regions, enabling robust classification modeling that considers both individual and regional behaviors.

The dataset can be downloaded from:

[DataCo SMART SUPPLY CHAIN FOR BIG DATA ANALYSIS](https://www.google.com/url?q=https%3A%2F%2Fdata.mendeley.com%2Fdatasets%2F8gx2fvg2k6%2F5)

---

## 🔍 Steps Performed (High-level)

### 1. Data Checks
- Checked for missing values and duplicates
- Inspected incorrect or impossible values
- Identified outliers in numeric columns 
- Converted columns to correct datatypes

### 2. Exploratory Data Analysis (EDA)
- **Univariate**: Histograms, density plots, summary stats.  
- **Bivariate**: Correlation heatmaps, scatterplots, boxplots.  
- **Multivariate**: Combined feature visualizations.  

### 3. Preprocessing
- **Encoding**: One-Hot Encoding for categorical, Label Encoding for target.  
- **Scaling**: StandardScaler for Logistic Regression/Decision Tree; MinMaxScaler for KNN/SVM.  
- **Feature Selection**: Used correlation and `SelectKBest` to retain most informative features.  
- **Outlier Handling**: Capped extreme values 

### 4. Modeling
Built baseline and advanced models:  
- Logistic Regression  
- KNN (K-Nearest Neighbors)  
- Decision Tree  
- SVM (Support Vector Machine)  
- Dummy Classifier (baseline)

### 5. Model Comparison
Each model was compared on:  
- Train time  
- Train accuracy  
- Test accuracy  
- Precision, Recall, F1-score  
- ROC-AUC

### 6. Hyperparameter Tuning
- Used **GridSearchCV** to tune hyperparameters:
  - Logistic Regression (regularization)  
  - KNN (n_neighbors, weights)  
  - Decision Tree (max_depth, min_samples_split)  
  - SVM (kernel, C, gamma)

---

## 📈 Modeling Approach

This project aims to compare multiple machine learning classification models to determine which algorithm best classifies customer sales behavior and supports the business objective of improving segmentation, targeting, and revenue growth.

Since the dataset comes from a supply chain context, important parameters related to customers, transactions, and products are identified and used to train the models. The goal is to classify customer sales patterns (e.g., likelihood to purchase, high-value customers, late delivery risks) and provide insights that help in predicting behavior and optimizing decision-making.

The classification models evaluated in this project include:

  - Logistic Regression
  - Gaussian Naive Bayes
  - Support Vector Machines (SVM)
  - k-Nearest Neighbors (KNN)
  - Decision Tree Classification
  - Random Forest Classification
  - Extra Trees Classification
  - Extreme Gradient Boosting (XGBoost)

Each model is compared using Accuracy, Precision, Recall, F1-score, and ROC-AUC, ensuring both balanced performance and business interpretability.

By benchmarking these models, the project will determine the most effective approach for answering the research question: “How can organizations detect and classify anomalies in sales and delivery data to proactively address fraud and late delivery risks?”

---

## 🛠️ How to Run
1. Open the Jupyter Notebook (`Mod24_AIML_Capstone - Sales Analysis - Late delivery risk and fraud analysis.ipynb`).
2. Upload dataset files  
3. Run the preprocessing cells to clean and encode the dataset.  
4. Execute modeling cells to train and evaluate classifiers.  
5. Review outputs and plots for model performance.  

---

## 📂 Project Structure
```
├── Module_17_Practical_Application_3.ipynb   # Main notebook
├── bank+marketing.csv                        # Dataset
├── README.md                                 # Project documentation
└── images/                                   # Plots & visualizations




