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

### Optimization
To efficiently label churn:
- Original method: O(n²) (too slow for 300,000+ rows)
- Improved method: O(m²) per customer group (`m` ≪ `n`), using `rowwise()` and `map()`

### Features Used:
- `payment_method`, `promo_amount`, `traffic_source`, `shipment_eta`, etc.

## ✅ Results

- Efficiently merged and cleaned multi-source behavioral data  
- Delivered meaningful visualizations for business and user insights  
- Built a reproducible pipeline for churn labeling and predictive modeling

---

📌 _This project was completed as part of the final assignment for STAT5125._
