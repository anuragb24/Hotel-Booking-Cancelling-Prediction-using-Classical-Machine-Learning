 

# Hotel Booking Cancellation Prediction

## 📌 Project Overview

This project analyzes a large hotel booking dataset (\~119K records, 32 features) to understand customer behavior, identify key drivers of booking cancellations, and build machine learning models to predict cancellation risk. The goal is to support hotels in **inventory management, overbooking strategy, and revenue optimization**.

---

## 🎯 Objectives

* Perform **Exploratory Data Analysis (EDA)** to uncover patterns in hotel bookings and cancellations.
* Engineer and preprocess features for robust predictive modeling.
* Compare multiple **machine learning classifiers** to select the best model for cancellation prediction.
* Provide **business insights** into customer segments, booking trends, and risk factors.

---

## ⚙️ Methodology

1. **Data Cleaning & Preprocessing**

   * Removed duplicates, imputed missing values (`agent`, `children`, `country`, `adr`), dropped high-NA columns (`company`).
   * Applied log transformations to skewed variables (`lead_time`, `adr`, etc.) and decomposed dates into **year, month, day**.
   * Encoded categorical variables (hotel type, meal plan, deposit type, etc.).

2. **Exploratory Data Analysis (EDA)**

   * Checked cancellation trends by **hotel type**, **lead time**, **arrival month**, **customer type**, and **market segment**.
   * Found that **city hotels, long lead times, transient customers, and low special requests** strongly correlate with cancellations.

3. **Model Development**

   * Implemented **Logistic Regression, Decision Tree, K-Nearest Neighbors, and Random Forest** classifiers.
   * Evaluated models with **K-Fold Cross Validation (CV mean = 0.82)**, **F1 score**, **accuracy**, and **confusion matrix**.
   * Tuned Random Forest with **GridSearchCV** for optimal hyperparameters.

---

## 📊 Results & Insights

* **Random Forest** emerged as the best classifier with:

  * **Accuracy:** \~95%
  * **F1 Score:** 0.93
  * **CV Mean Score:** 0.82
* Key predictors: **lead time, hotel type, market segment, special requests**.
* Discovered actionable insights:

  * **Transient customers** are more likely to cancel.
  * **City hotels** face higher cancellation rates than resort hotels.
  * **Cancellations peak around 60–70 days lead time**.
  * **Repeat guests cancel less frequently** than new customers.

---

## 🛠️ Tech Stack

* **Languages & Libraries:** Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn
* **Techniques:** Data Cleaning, Feature Engineering, Label Encoding, Log Transformation, Hyperparameter Tuning, Cross Validation
* **ML Models:** Logistic Regression, Decision Tree, KNN, Random Forest

---

## 🚀 Key Deliverables

* Cleaned and preprocessed hotel booking dataset.
* EDA visualizations of cancellation drivers.
* ML model comparison with metrics and confusion matrices.
* Final **Random Forest model** with tuned hyperparameters and feature importance insights. 
