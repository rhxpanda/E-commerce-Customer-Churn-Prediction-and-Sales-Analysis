# E-commerce-Customer-Churn-Prediction-and-Sales-Analysis
# 📊 STAT5125 Final Project

## 🔍 Overview

This project analyzes customer behavior in an Indonesian fashion e-commerce dataset. It covers:

- ✅ **Data Tidying**: Transforming messy raw tables into clean, tidy formats  
- 📈 **Exploratory Analysis**: Visualizing trends in sales, promotion usage, and user activity  
- 🧠 **Churn Prediction**: Building a model to identify users likely to churn based on behavior patterns

## 📂 Dataset

Source: [Kaggle – Fashion E-Commerce Products Indonesia](https://www.kaggle.com/datasets/safrizalardanaa/produk-ecommerce-indonesia)

**Data sources used:**

- `transaction.csv`: Transaction-level records (payments, shipping, promos)
- `click_stream.csv`: Session-level logs (traffic source, interaction)
- `customer.csv`: Customer demographics and device info
- `product.csv`: Product category and attributes

## 🛠 Tech Stack

- **Language:** R  
- **Packages:** `tidyverse`, `tidymodels`, `lubridate`, `ggplot2`, `dplyr`, `purrr`

## 📊 Key Insights

- Time-based sales and promo usage trends
- Customer signup behavior across years
- Purchase breakdowns by category and channel

## 🔍 Churn Definition & Modeling

Churn is defined as:  
> A customer is considered churned if they made **no purchases within 30 days** after a transaction.

To generate churn labels efficiently, we created a custom labeling function that groups by user and compares session timestamps — reducing time complexity from **O(n²)** to **O(m²)** per user.

### ⚙️ Modeling Workflow

We used the [`tidymodels`](https://www.tidymodels.org/) framework in R, with the following setup:

- **Preprocessing:** `recipe()` for dummy encoding and normalization  
- **Split:** `initial_split()` to divide training and testing sets  
- **Model:** `logistic_reg()` from `parsnip` with `glm` engine  
- **Evaluation:** `metrics = metric_set(accuracy, roc_auc)`  
- **Final Fit:** `last_fit()` for performance on unseen test data

### 📌 Features used in modeling

- `promo_amount`  
- `payment_method`  
- `traffic_source`  
- `shipment_eta`  
- Session timing & frequency 

## ✅ Results

- Efficiently merged and cleaned multi-source behavioral data  
- Delivered meaningful visualizations for business and user insights  
- Built a reproducible pipeline for churn labeling and predictive modeling

---

📌 _This project was completed as part of the final assignment for STAT5125._
