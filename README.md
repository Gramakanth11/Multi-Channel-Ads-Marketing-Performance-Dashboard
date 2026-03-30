# 📊 Multi-Channel Marketing Performance Dashboard

## 🚀 Project Overview

This project analyzes marketing performance across multiple advertising platforms (Google, Meta, TikTok) by integrating **Ads data, Google Analytics (GA) data, and CRM data** into a unified Power BI dashboard.

The goal was to understand:

* How much we are spending on ads
* How users interact with ads (clicks, impressions)
* How many users actually convert into customers
* Whether our marketing efforts are profitable

---

## 🎯 Business Problem

Marketing teams often rely on platform-reported metrics (like Google Ads revenue), which can be misleading.

This project answers a critical question:

> **Are our ads actually generating real business revenue, or just inflated platform numbers?**

---

## 📂 Data Sources

### 1️⃣ Ads Dataset

Contains campaign-level marketing performance:

* Impressions
* Clicks
* Ad Spend
* Estimated Revenue (platform-reported)

👉 Represents **marketing effort**

---

### 2️⃣ Google Analytics (GA) Dataset

Contains user interaction data:

* Traffic sources
* Sessions / visits
* User behavior

👉 Represents **user engagement**

---

### 3️⃣ CRM Dataset

Contains actual business outcomes:

* Leads
* Conversion status (Won / Lost)
* Revenue

👉 Represents **real revenue (source of truth)**

---

## 🔧 Data Preparation

### Key Challenge:

Each dataset used different naming conventions and levels of detail.

### What I did:

* Created a **common key (`campaign_group`)** across all datasets
* Standardized campaign names (google_search, meta_display, tiktok_video)
* Handled missing values and "unknown" traffic
* Cleaned and transformed data using Power Query

---

## 🧠 Data Model

Built a **star schema**:

* `dim_campaign` → central table
* Connected to:

  * Ads (spend data)
  * GA (traffic data)
  * CRM (conversion data)

👉 This avoids incorrect joins and ensures accurate analysis

---

## 📊 Key Metrics (KPIs)

* **Total Spend** → Total advertising cost
* **Estimated Revenue (Ads)** → Platform-reported revenue
* **Actual Revenue (CRM)** → Real business revenue
* **ROAS (Return on Ad Spend)** → Profitability
* **CTR (Click Through Rate)** → Engagement efficiency
* **CPC (Cost Per Click)** → Cost efficiency
* **Total Conversions** → Number of successful leads

---

## ⚠️ Important Insight

> Ads platforms significantly overestimate revenue compared to CRM data.

This highlights:

* Attribution gaps
* Tracking limitations
* Conversion drop-offs

---

## 📈 Dashboard Features

### 🔹 KPI Cards

Quick overview of performance:

* Spend, Revenue, ROAS, CTR, CPC

---

### 🔹 Campaign ROI Comparison

Compares:

* Spend vs Actual Revenue per campaign

👉 Helps identify underperforming campaigns

---

### 🔹 ROAS by Campaign

Shows profitability across campaigns

👉 Example insight:

* TikTok → highest ROAS
* Google → highest spend but lowest return

---

### 🔹 Campaign Efficiency (Scatter Plot)

* X-axis → Spend
* Y-axis → ROAS
* Bubble size → Conversions

👉 Helps identify high-performing campaigns visually

---

### 🔹 Revenue Distribution (Pie Chart)

Breakdown of revenue contribution by campaign

---

### 🔹 Funnel Analysis

Tracks user journey:

* Impressions → Clicks → Conversions

👉 Shows drop-offs in marketing funnel

---

### 🔹 Tabular View

Detailed comparison of:

* Spend
* Revenue
* ROAS

👉 Useful for decision-making

---

## 🧠 Key Insights

* TikTok campaigns deliver the **highest ROI** despite lower spend
* Google Search consumes the **largest budget but underperforms**
* Significant gap between **estimated vs actual revenue**
* Conversion volume is low, indicating **inefficiencies in the funnel**

---

## 🛠 Tools Used

* **Power BI** → Data modeling & visualization
* **Power Query** → Data cleaning
* **DAX** → KPI calculations

---

## 💡 What I Learned

* Importance of **data consistency across sources**
* Difference between **platform metrics vs business metrics**
* How to design **real-world dashboards using star schema**
* How to convert raw data into **actionable insights**

---

## 📌 Conclusion

This project demonstrates how combining multiple data sources can uncover hidden insights and prevent misleading conclusions.

👉 Instead of blindly trusting ad platform metrics, businesses should rely on **CRM-driven insights for real performance evaluation**.

---

## 📎 How to Use

1. Open the Power BI file
2. Use slicers to filter by campaign or date
3. Analyze KPIs and charts to derive insights

---

## ⭐ If you found this useful

Feel free to ⭐ the repo or connect with me!
