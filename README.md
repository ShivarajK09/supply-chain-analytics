# 🔗 Supply Chain Analytics — End-to-End Project

![SQL](https://img.shields.io/badge/SQL-MySQL-blue)
![Python](https://img.shields.io/badge/Python-3.13-green)
![ML](https://img.shields.io/badge/Machine%20Learning-XGBoost-orange)
![PowerBI](https://img.shields.io/badge/Dashboard-PowerBI-yellow)

## 📌 Project Overview
An end-to-end supply chain analytics project built on the **DataCo Supply Chain Dataset** containing **180,519 orders** across global markets. The project covers the full analytics pipeline — from raw data ingestion and SQL analysis to machine learning and interactive dashboards.

---

## 🗂️ Project Structure
supply-chain-analytics/

│

├── 01_Data_Exploration/

├── 02_SQL_Analysis/

│   └── supply_chain_queries.sql

├── 03_Python_Analysis/

│   └── supply_chain_eda.ipynb

├── 04_Visualizations/

│   ├── 01_late_delivery_distribution.png

│   ├── 02_delivery_status_breakdown.png

│   ├── 03_shipping_mode_late_delivery.png

│   ├── 04_profit_by_market.png

│   ├── 05_sales_by_segment.png

│   ├── 06_planned_vs_actual_shipping.png

│   ├── 07_model_comparison.png

│   ├── 08_feature_importance.png

│   └── 09_xgboost_improved_features.png

├── 05_PowerBI/

│   └── Supply_Chain_Dashboard.pbix

└── README.md

---

## 🛠️ Tech Stack
| Tool | Purpose |
|---|---|
| MySQL | Data storage and SQL analysis |
| Python (pandas, seaborn, matplotlib) | EDA and visualization |
| Scikit-learn, XGBoost | Machine learning |
| Power BI | Interactive dashboard |

---

## 📊 Dashboard Preview
![Dashboard](PowerBI%20Dashboard.png)

---

## 🔍 Phase 1 — SQL Analysis
**7 business questions answered using MySQL:**

| # | Question | Key Finding |
|---|---|---|
| 1 | Overall late delivery rate | 54.83% of 180,519 orders were late |
| 2 | Delivery status breakdown | Late delivery dominates at 54.83% |
| 3 | Late delivery by shipping mode | First Class worst at 95.32% late |
| 4 | Profit by market | Europe leads with $1.16M total profit |
| 5 | Top 10 products by sales | Field & Stream Gun Safe #1 at $6.9M |
| 6 | Sales by customer segment | Consumer segment drives $19M in sales |
| 7 | Scheduled vs actual shipping days | Second Class delays by +1.99 days |

---

## 🐍 Phase 2 — Python EDA
Exploratory data analysis using pandas, matplotlib, and seaborn:
- Late delivery risk distribution
- Delivery status breakdown
- Shipping mode vs late delivery rate
- Profit by market
- Sales by customer segment
- Planned vs actual shipping days comparison

---

## 🤖 Phase 3 — Machine Learning (Late Delivery Prediction)

### Model Progression
| Model | Features | Accuracy |
|---|---|---|
| Logistic Regression | 5 basic features | 68.75% |
| Random Forest | 5 basic features | 69.10% |
| XGBoost (basic) | 5 basic features | 69.12% |
| **XGBoost (engineered)** | **10 features + delay_gap** | **97.49% ✅** |

### Key Insight
> Engineered a new feature `delay_gap` = actual shipping days − scheduled shipping days. This single feature improved model accuracy from **69% to 97.49%**, confirming that shipment scheduling discipline is the most critical factor in predicting late deliveries.

---

## 📈 Phase 4 — Power BI Dashboard
Interactive dashboard with:
- 5 KPI cards (Total Orders, Profit, Sales, Quantity, Avg Shipping Days)
- Profit by Category (bar chart)
- Sales by Market (pie chart)
- Profit by Customer Segment (stacked bar)
- Total Orders by Shipping Mode (bar chart)
- Filters: Market, Shipping Mode, Category, Order Region

---

## 💡 Key Business Insights
1. **54.83% late delivery rate** — more than half of all orders are at risk
2. **First Class shipping has 95.32% late delivery** — premium customers get worst service
3. **Europe is the most profitable market** at $1.16M total profit
4. **Consumer segment drives 52%+ of total sales**
5. **Standard Class is the only shipping mode meeting its schedule** (0 days delay)
6. **delay_gap feature drives 99%+ of ML prediction** — scheduling is everything

---

## 🚀 How to Run
1. Import `DataCoSupplyChainDataset.csv` into MySQL
2. Run `02_SQL_Analysis/supply_chain_queries.sql`
3. Open `03_Python_Analysis/supply_chain_eda.ipynb` in VS Code
4. Open `05_PowerBI/Supply_Chain_Dashboard.pbix` in Power BI Desktop

---

## 👤 Author
**Shivaraj** — MBA (Operations & Business Analytics), PES University Bangalore  
4 years supply chain operations experience at Wilmar/Shree Renuka Sugars Ltd.
