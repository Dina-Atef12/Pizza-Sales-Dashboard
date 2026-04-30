# Pizza-Sales-Dashboard
Designed to help restaurant managers make data-driven decisions by analyzing 48,620 pizza sales transactions, uncovering revenue trends, peak ordering patterns, and product performance insights.


## 🚀 Quick Highlights

- 💰 Revenue: $817K across 21K orders  
- 📈 Peak sales on Fridays (+27% vs Sunday)  
- 🍕 Top product: Thai Chicken Pizza ($43K)  
- 📊 Built with Power BI + DAX  
- 💡 Includes revenue simulator for business decisions  

📈 Key Metrics

Metric              Value

Total Revenue           $817,860

Total Orders            21,350

Avg Order Value         $38.31

Pizzas Sold             49,574

✨ Features

5-page dashboard with bookmark-based tab navigation
KPI cards — Revenue, Orders, AOV, Pizzas Sold
Revenue trend — monthly with anomaly annotations
Pizza performance board — card grid, color-coded by category
Peak hours analysis — hourly heatmap + day-of-week breakdown
Revenue simulator — what-if sliders projecting up to +14.9% uplift
Drill-through pages — click any pizza for a detailed breakdown
Dynamic titles — update based on active slicer selections

💡 Top Insights

🏆 Thai Chicken is the #1 pizza at $43.4K — 3.7× the bottom performer
📅 Friday drives 27% more orders than Sunday (7,723 vs 6,063)
⏰ 12–1 PM is peak hour with ~12,700 orders — critical staffing window
📉 September & December dip 8–9% below average — seasonal promo opportunity
📐 Large size alone generates 45.9% of total revenue


🛠️ Built With
Power BI Desktop   DAX   Power Query   Bookmarks   Drill-through   Conditional Formatting

📐 DAX Highlights
dax-- Average Order Value
Avg Order Value = DIVIDE([Total Revenue], DISTINCTCOUNT(pizza_sales[order_id]))

-- Revenue formatted as $43.4K
Revenue Label =
"$" & FORMAT([Total Revenue] / 1000, "#.#") & "K"

-- Auto-detect top seller
Top Seller =
IF(RANKX(ALL(pizza_sales[pizza_name]), [Total Revenue],, DESC, Dense) = 1,
   "Top seller", "")

   📂 Files
├── PizzaSalesDashboard.pbix     ← Power BI report
├── pizza_sales.xlsx             ← Source dataset
├── FornoAnalytics_Theme.json    ← Custom dark theme
└── screenshots/
    ├── overview.png
    ├── menu_board.png
    ├── timeline.png
    └── simulator.png

    
