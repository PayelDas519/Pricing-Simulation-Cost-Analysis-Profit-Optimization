# E-Commerce Analytics — Pricing Simulation, Cost Analysis & Profit Optimization

## Project Overview
An end-to-end e-commerce analytics project analyzing 10,000 transactions 
across 4 product categories to identify pricing inefficiencies, cost 
drivers, and profit optimization opportunities.

The business was found to be **loss-making at -₹5,41,184 total profit** 
despite generating **₹28.7 Cr in revenue**. A pricing simulation showed 
a potential uplift of **₹1.43 Cr (+2,648%)** through optimized repricing.

---

## Dataset
- **Transactions:** 10,000
- **Categories:** Beauty, Electronics, Fashion, Home
- **Period:** January 2023 – June 2023
- **Source:** Internal e-commerce transaction records
- **Features:** 41 engineered columns including Revenue, Profit, 
  Simulated Profit, Conversion Rate, ROI, Break-even Flag, 
  Aging Risk, Price Category, Discount Bucket

---

## Key Findings

### 1. Pricing
- 57% of SKUs (5,711 products) are priced below break-even
- Home is the only profitable category (+₹3.67L)
- Beauty and Electronics are the biggest loss drivers

### 2. Simulation Opportunity
- A +5% price increase converts -₹5.4L loss into +₹1.38 Cr profit
- ₹1,500–₹1,700 price bucket delivers peak profit concentration

### 3. Discount Strategy
- All discount tiers are loss-making
- Expensive SKUs (above competitor price) generate +₹3,424 avg profit
- Cheaper SKUs generate -₹2,089 avg profit — discounting is backfiring

### 4. Cost Structure
- High Cost SKUs average -₹2,145 profit per unit
- Normal Cost SKUs average +₹12,854 profit per unit
- Freight and storage are the primary margin destroyers

### 5. Channel & Traffic
- Mobile and Desktop perform almost identically
- All traffic sources (Ads, Direct, Organic) show no significant difference
- Budget should be redirected to pricing improvements

---

## Dashboard Pages
| Page | Focus |
|------|-------|
| Page 1 | Executive Summary |
| Page 2 | Pricing Simulation |
| Page 3 | Cost & Margin Analysis |
| Page 4 | Discount Strategy |
| Page 5 | Channel & Traffic Performance |
| Page 6 | Inventory & Aging Analysis |
| Page 7 | Executive Recommendations |

---

## Screenshots
### Page 1 — Executive Summary
![Executive Summary](screenshots/page1_executive_summary.png)

### Page 2 — Pricing Simulation
![Pricing Simulation](screenshots/page2_pricing_simulation.png)

### Page 3 — Cost & Margin
![Cost and Margin](screenshots/page3_cost_margin.png)

### Page 4 — Discount Strategy
![Discount Strategy](screenshots/page4_discount_strategy.png)

### Page 5 — Channel & Traffic
![Channel Traffic](screenshots/page5_channel_traffic.png)

### Page 6 — Inventory & Aging
![Inventory Aging](screenshots/page6_inventory_aging.png)

### Page 7 — Executive Recommendations
![Recommendations](screenshots/page7_recommendations.png)

---

## Tools Used
- **Microsoft Excel** — Data cleaning, feature engineering, pivot analysis
- **Power BI Desktop** — Interactive dashboard (7 pages)
- **DAX** — Custom measures for profit, simulation, ROI, conversion rate
- **Power Query** — Data transformation and column type validation

---

## Excel Sheet Structure
| Sheet | Purpose |
|-------|---------|
| Raw Data | Original 10,000 transaction records |
| Data Cleaning | Cleaned version used as source |
| Feature Engineering | 41 engineered columns — main analytics table |
| Business Questions | Pre-answered analytical questions |
| Analysis-Pivot Table | Cross-tab pivot summaries |

---

## DAX Measures Used
```dax
Total Revenue = SUM('Feature Engineering'[Revenue])

Total Profit = SUM('Feature Engineering'[Profit])

Simulated Profit = SUM('Feature Engineering'[Simulated Profit])

Profit Uplift = [Simulated Profit] - [Total Profit]

Loss SKU % = DIVIDE(
    COUNTROWS(FILTER('Feature Engineering',
    'Feature Engineering'[Break-even Flag] = "Loss")),
    COUNTROWS('Feature Engineering')
)

Avg Conversion Rate = AVERAGE('Feature Engineering'[Conversion Rate])

Avg ROI = AVERAGE('Feature Engineering'[ROI])
```

---

## How to Use
1. Clone or download this repository
2. Open `data/ecommerce_pricing_analysis.xlsx` to explore the raw 
   analysis and feature engineering
3. Open `dashboard/ecommerce_dashboard.pbix` in Power BI Desktop
4. If data connection breaks, go to **Home → Transform Data → 
   Data Source Settings** and repoint to the xlsx file location
5. Open `dashboard/dashboard_preview.html` in any browser for 
   a quick static preview without Power BI

---

## Recommended Actions
1. **Immediate** — Reprice Beauty and Electronics SKUs upward
2. **Immediate** — Cap all discounts at 20% maximum
3. **Short Term** — Clear 90+ day aging inventory to reduce storage costs
4. **Short Term** — Replicate Home category pricing strategy across others
5. **Long Term** — Renegotiate freight and storage cost contracts

---

## Author
**Your Name**
[LinkedIn](https://linkedin.com/in/yourprofile) | 
[GitHub](https://github.com/yourusername)
