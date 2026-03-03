# Olist-Brazil-E-Commerce-Analytics-Modeling
End-to-end analytics and modeling on the Olist Brazil e-commerce dataset (2016–2018) to uncover what drives marketplace success and customer trust. 7 reproducible analyses cover delivery performance, product/listing drivers of sales, review propensity, high-rating prediction, and customer &amp; seller segmentation.


---

## Dataset Overview

- **Source:** Kaggle (Olist)
- **Format:** 9 CSV tables
- **Scale:** ~100,000 rows (raw), mixed **numerical/categorical/text/date** fields
- **Known data issues handled in this project:** missing values (~5–10%), formatting inconsistencies (e.g., dates/categories), and multi-table joins.
---
## How to Navigate

This repository is organized for fast review and reproducibility:

- **`/code/`**: 7 standalone scripts/notebooks — each file answers one research question (one analysis per question).
- **`/report/`**: final presentation/report summarizing methods, results, and recommendations.
- **`/data/`**: the Olist dataset (CSV tables). Raw tables are kept as-is; each analysis script loads and merges the required files.

> Tip: Start with the report for context, then open the corresponding analysis in `/code/`.

---
## Research Questions & Methods (7 Analyses)

### 1) Delivery Proficiency — What drives delivery time?
**Goal:** identify bottlenecks in delivery and how they impact customer experience.  
**Method:** Linear regression with engineered delivery time (days) and features like freight value, weight/volume, product count, location (seller/customer state), and time components (day/week/month + holiday dummy).

### 2) Product Attributes & Sales — What increases units sold?
**Goal:** help product managers refine listings and improve sales.  
**Method:** Linear regression with product attributes (category dummies, name/description lengths, price, photos, weight/dimensions).  
**Note:** model fit is modest, so we document limitations and next steps.

### 3) Incentivizing Reviews — What predicts whether a customer leaves a review?
**Goal:** understand review behavior to increase engagement and trust.  
**Method:** Logistic regression (binary: review given vs not), with feature selection, one-hot encoding, scaling, and evaluation using F1.

### 4) Customer Satisfaction — What predicts a high review score (>4 stars)?
**Goal:** identify drivers of high satisfaction.  
**Method:** Logistic regression + Ridge regularization + cross-validation.  
Features include delivery time, product photos quantity, product description length, and freight value relative to price.

### 5) Customer Segmentation — How can customers be clustered by purchasing behavior?
**Goal:** create actionable segments for targeted marketing and retention.  
**Method:** K-Means on aggregated customer-level metrics (total spend, freight cost, frequency, unique products, categories), scaling, and elbow method exploration.

### 6) Seller Segmentation — How can sellers be clustered by performance metrics?
**Goal:** tailor platform support and improve marketplace health.  
**Method:** Hierarchical clustering on seller-level aggregated product/price/revenue/sales and listing-quality metrics (name/description length, photos, weight/dimensions).

---

## Key Business Takeaways (high level)

- Delivery time and geographic variability are critical levers for customer experience.
- Review behavior is influenced by price and delivery outcomes; incentives and logistics improvements can increase review rates.
- Customer and seller clustering enable targeted retention and growth strategies (e.g., focus resources on loyal repeat segments; tailored support for high-performing sellers).


## Contributors

- Camila Gutierrez  
- Theresse Nilson  
- Ali Senel  
- Vera van Gansewinkel  
- Ashia Norhalim  
- Diana Vossberg
