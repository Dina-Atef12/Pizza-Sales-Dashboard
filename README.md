# 🍕 Pizza Sales Dashboard — Power BI

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Data%20Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/DAX-Advanced-0078D4?style=for-the-badge&logo=microsoft&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20Query-ETL-512BD4?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>
</p>

---

## 📊 Overview

A **business intelligence dashboard** built using Power BI to analyze **48,620 pizza sales transactions**, uncovering revenue patterns, customer behavior, and product performance insights.

This project simulates real-world restaurant analytics to support **data-driven decision making**.

---

## 🚀 Key Highlights

* 💰 **Total Revenue:** $817K across 21K orders
* 🍕 **Top Product:** Thai Chicken Pizza ($43K)
* 📈 **Best Day:** Friday (+27% vs Sunday)
* ⏰ **Peak Hour:** 12–1 PM (~12.7K orders)
* 📊 Built with **Power BI + Advanced DAX**

---

## 📈 Business KPIs

| Metric             | Value    |
| ------------------ | -------- |
| 💰 Total Revenue   | $817,860 |
| 🧾 Total Orders    | 21,350   |
| 📦 Pizzas Sold     | 49,574   |
| 💵 Avg Order Value | $38.31   |

---

## 🧠 Key Insights

* 🏆 Thai Chicken Pizza dominates sales with **$43.4K revenue**
* 📅 Friday drives **+27% more orders** than Sunday
* ⏰ Peak demand occurs during **lunch hours (12–1 PM)**
* 📉 Seasonal dips in **September & December (-8% to -9%)**
* 📐 Large size pizzas contribute **45.9% of total revenue**

---

## ✨ Dashboard Features

* 📊 Multi-page interactive dashboard (5 pages)
* 🔘 Bookmark-based navigation system
* 💰 KPI Cards (Revenue, Orders, AOV, Units Sold)
* 📈 Revenue trend analysis with anomaly detection
* 🍕 Product performance matrix (color-coded categories)
* ⏰ Hourly + weekly heatmap analysis
* 🎯 Revenue simulator (What-if analysis up to +14.9%)
* 🔍 Drill-through product insights
* 🧠 Dynamic titles based on slicer context

---

## 🛠️ Tech Stack

<p align="center">

<img src="https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=flat-square&logo=powerbi"/>
<img src="https://img.shields.io/badge/DAX-Formulas-0078D4?style=flat-square"/>
<img src="https://img.shields.io/badge/Power%20Query-ETL-512BD4?style=flat-square"/>
<img src="https://img.shields.io/badge/Excel-Data%20Source-217346?style=flat-square&logo=microsoft-excel"/>

</p>

---

## 📐 Sample DAX Measures

```DAX
-- Average Order Value
Avg Order Value =
DIVIDE([Total Revenue], DISTINCTCOUNT(pizza_sales[order_id]))

-- Revenue Formatting
Revenue Label =
"$" & FORMAT([Total Revenue] / 1000, "#.#") & "K"

-- Top Seller Flag
Top Seller =
IF(
    RANKX(ALL(pizza_sales[pizza_name]), [Total Revenue],, DESC, Dense) = 1,
    "Top Seller",
    BLANK()
)
```

---

## 📂 Project Structure

```
Pizza-Sales-Dashboard/
│
├── PizzaSalesDashboard.pbix
├── pizza_sales.xlsx
├── FornoAnalytics_Theme.json
│
└── screenshots/
    ├── overview.png
    ├── menu_board.png
    ├── timeline.png
    └── simulator.png
```

---
## 🎯 Business Value

This dashboard helps restaurant managers to:

* Optimize **staff scheduling**
* Improve **menu profitability**
* Identify **best-selling products**
* Track **seasonal demand changes**
* Simulate **revenue growth scenarios**

---

## 👩‍💻 Author

**Dina Atef Ramadan Ali**
📊 Data & BI Enthusiast | Power BI Developer

