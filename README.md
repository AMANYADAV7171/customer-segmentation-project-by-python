# 🛒 Customer Segmentation using K-Means Clustering

An end-to-end **customer segmentation project** built with Python. It cleans raw customer data, explores it visually, and uses **K-Means clustering** on RFM-style features to group customers into actionable business segments.

---

## 📌 Project Overview

Businesses can't treat all customers the same way. This project groups customers by income, spending behavior, purchase frequency, and recency, so marketing teams can design targeted strategies such as loyalty rewards, premium offers, and win-back campaigns.

---

## 🎯 Objectives

- Clean and prepare raw customer data for analysis
- Explore demographics, spending patterns, and correlations
- Create a customer value tier (High / Mid / Low)
- Find the optimal number of clusters using the Elbow Method
- Segment customers with K-Means and evaluate them with the Silhouette Score
- Translate clusters into business-friendly segments with recommendations

---

## 🔄 Workflow

### Step 1: Data Cleaning
- Loaded the dataset and inspected shape, data types, and statistics
- Filled missing numeric values with the **median** (robust to outliers)
- Removed duplicate rows
- Standardized text columns (Gender, ProductCategory, Region)
- Engineered a **ValueTier** feature based on `TotalSpent_USD`:
  - High Value: ≥ 15,000
  - Mid Value: ≥ 6,000
  - Low Value: < 6,000

### Step 2: Data Visualization
Six charts built with Matplotlib and Seaborn:
1. Customer demographics (gender split and region distribution)
2. Age and annual income distributions
3. Income vs Spending Score scatter plot (colored by total spent)
4. Value tier breakdown by product category
5. Spending Score by gender (box plot)
6. Correlation heatmap of numeric features

### Step 3: Machine Learning (K-Means Clustering)
- **Features used:** Annual Income, Spending Score, Purchase Frequency, Last Purchase Days
- Scaled features with `StandardScaler`
- Used the **Elbow Method** (K = 2 to 10) and chose **K = 4**
- Evaluated cluster quality with the **Silhouette Score**
- Visualized segments with a scatter plot, a segment size chart, and a radar chart

---

## 🎯 Customer Segments & Recommendations

| Segment | Description | Recommended Action |
|---|---|---|
| 🏆 **Champions** | Highest spending score | Reward and retain with loyalty perks |
| 💎 **High Earners – Low Spend** | High income but low spending | Target with premium product offers |
| 🌱 **Potential Loyalists** | Frequent buyers with room to grow | Nurture with personalized emails |
| 😴 **At-Risk / Dormant** | Lowest spending score | Win back with discount
