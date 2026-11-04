[e_commerce_bi_github_readme.md](https://github.com/user-attachments/files/34361954/e_commerce_bi_github_readme.md)
# 📊 E-Commerce Strategic Business Intelligence & Decision-Making Tool

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Advanced_Modeling-blue?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)]()

> **An end-to-end Business Intelligence and Strategic Simulation solution designed to diagnose multi-year financial performance, rationalize inventory bloat, uncover micro-segment profitability drivers, and simulate forward-looking pricing scenarios.**

---

## 📁 Repository Structure

All project assets, dashboard visual snapshots, and the main Power BI report are organized within this repository as follows:

```text
📦 E-Commerce-Strategic-Business-Intelligence-Decision-Making-Tool
 ┣ 📂 E_ecommerce/              # High-resolution snapshots of all dashboard modules
 ┣ 📄 E-Commerce Dashboard.pbix # Main Power BI Desktop application file
 ┗ 📄 README.md                 # Project case study, findings, and technical documentation
```

---

## 📌 1. Executive Summary & Core KPIs

This project transforms three years of historical e-commerce transactional records (2006–2008) into an interactive decision-support system. Below is the high-level financial and operational baseline achieved across the analyzed period:

| Metric | Value | Strategic Context |
| :--- | :--- | :--- |
| **Total Revenue** | **USD 273.7M** | Cumulative gross sales across 6 global markets |
| **Total COGS** | **USD 160.8M** | Direct cost of goods sold (58.76% of revenue) |
| **Total Profit** | **USD 112.9M** | Exact net margin of **USD 112,886,951.1** |
| **Profit Margin** | **41.24%** | Strong baseline gross profitability |
| **Total Quantity Sold** | **622K Units** | Cumulative volume shipped |
| **Active Customer Base** | **18.3K Customers** | Generating an average profit of **USD 6.2K per customer** |
| **Average Customer Age** | **34 Years** | Core demographic spanning ages 15 to 54 |
| **Catalog Utilization** | **158 / 606 SKUs** | **26.07%** active revenue-generating products vs. **73.93%** dead stock |

---

## 🚨 2. The Business Problems (Why This Project Was Built)

Before developing this analytical tool, raw transactional tables masked four critical operational and strategic bottlenecks:

1. **Severe Inventory Bloat & Capital Lockup (Dead Stock):**
   Out of **606 available products** in the master catalog, only **158 products (26.07%)** generated actual sales, while **448 products (73.93%)** remained completely unsold (**UnSold Products**), tying up warehouse capacity and working capital.
2. **Extreme Price-Tier & Geographic Concentration Risk:**
   * **Price Concentration:** Products priced above USD 150 generated **94.9% (USD 107.1M)** of total company profits, while items priced below USD 150 contributed only **5.1% (USD 5.8M)**.
   * **Geographic Concentration:** Just two markets—the **United States (USD 36.2M)** and **Australia (USD 33.3M)**—accounted for **61.56%** of global profit, leaving European and Canadian operations under-leveraged.
3. **Time-Series Distortion & Misleading Seasonality:**
   High-level monthly trend lines suggested a sharp seasonal collapse starting every July (dropping from **USD 32.6M** in June to **USD 15.0M** in July). Root-cause inspection revealed this was caused by data collection ending in mid-July 2008 rather than an actual summer demand slump.
4. **Lack of Forward-Looking Pricing & Discount Visibility:**
   Executive leadership lacked a dynamic sensitivity model to test how promotional discounts, supply cost fluctuations, or price adjustments would impact net ROI and breakeven thresholds.

---

## 🛠️ 3. What Was Done (Technical Solution & Architecture)

To address these challenges, I engineered a **5-module analytical ecosystem** inside Power BI:

### Module 1: Executive Financial Overview
* Built dynamic KPI cards tracking **Total Revenue**, **Total Profit**, **Profit Margin %**, **Total COGS**, and **Total Quantity** with trend sparklines.
* Designed seasonal and calendar breakdowns comparing **Weekday performance (71.9% / USD 81.2M)** against **Weekend performance (28.1% / USD 31.7M)**, alongside day-of-week and quarterly profit distributions (**Q1: USD 32.3M, Q2: USD 39.0M, Q3: USD 18.2M, Q4: USD 23.4M**).

### Module 2: Product & Inventory Rationalization Intelligence
* Formulated dynamic DAX measures isolating **Sold Products (158)** vs. **UnSold Products (448)** across any selected timeframe or region.
* Evaluated profit distribution across **Size Groups**, **Pricing Tiers (< USD 150 vs. > USD 150)**, **Top-5 Profitable Colors**, and **Top-5 Hero Products**.

### Module 3: Root-Cause Decomposition Tree & Historical Matrix
* Implemented an AI-assisted **Decomposition Tree** drilling down across 6 hierarchical dimensions:
  $$\text{Total Profit} \rightarrow \text{Year} \rightarrow \text{Country} \rightarrow \text{Size Group} \rightarrow \text{Gender} \rightarrow \text{Color} \rightarrow \text{Product Name}$$
* Paired the tree with a **36-month granular financial matrix (2006–2008)** tracking monthly Revenue, Profit, Quantity, Sold SKUs, and Unsold SKUs side-by-side.

### Module 4: Customer Demographics & Lifecycle Segmentation
* Segmented the **18.3K customer base** by **Gender**, **Marital Status**, **Household Size (Total Children: 0 to 5)**, and **Age Brackets (15–25, 25–34, 35–44, 45–54)**.
* Ranked top high-value VIP customers by net lifetime profit contribution.

### Module 5: Dynamic What-If Strategic Simulation Engine
* Constructed 4 independent **What-If Parameters** allowing decision-makers to simulate real-time shifts in:
  1. `Quantity Change %`
  2. `Price Change %`
  3. `Cost Change %`
  4. `Discount %`
* Engineered automated financial outputs calculating **Projected Revenue**, **Projected COGS**, **Projected Profit**, **Projected ROI % (70.2% baseline)**, **Max Safe Discount % (41.2% breakeven ceiling)**, and an automated **Strategic Signal** indicator.

---

## 🔍 4. Deep-Dive Analytical Findings (Key Insights)

### A. The July 2007 Operational Inflection Point
Cross-examining the monthly matrix uncovered the single most important growth driver in the company's history:
* **Stagnant Baseline (Jan 2006 – Jun 2007):** For 18 consecutive months, active sold products hovered between **23 and 31 SKUs per month**, generating monthly volumes of only **1,810 to 3,490 units** and total 2006 profit of **USD 28.18M**.
* **The Catalog Expansion Surge (July 2007):** In July 2007, active sold SKUs tripled from **31 to 99 products** (and **102 products** by August).
* **Immediate Financial Impact:** Monthly unit sales surged by **+362.86% in a single month** (jumping from **3,258 units** in June 2007 to **15,080 units** in July 2007, and scaling to **55,082 units / USD 18.43M revenue** by December 2007).
* **Record 2008 Velocity:** Driven by this broader active catalog, H1 2008 profit reached **USD 41.87M** compared to **USD 13.04M** in H1 2007—a **+221% Year-over-Year profit expansion**. Within just 6.5 months in 2008, the company generated **USD 42.16M** in profit, nearly matching the entire 12-month profit of 2007 (**USD 42.55M**).

### B. Product, Size, and Color Pareto Dynamics
* **Hero SKUs:** **Mountain-200** is the undisputed flagship product, generating **USD 37M** in profit alone, followed by **Road-250 (USD 18M)**, **Road-150 (USD 12M)**, **Touring-1000 (USD 12M)**, and **Road-350-W (USD 6M)**.
* **Color Concentration:** The top 5 colors (**Black: USD 38M, Silver: USD 23M, Red: USD 21M, Yellow: USD 19M, Blue: USD 9M**) drive **72.0%** of total company profit, while all other colors combined contribute **28.0%**.
* **Size Group Skew:** Small (**S: USD 46.4M**) and Medium (**M: USD 41.4M**) sizes capture **77.77% (USD 87.8M)** of total profits, whereas Large (**L: USD 17.0M**) and Extra-Large (**XL: USD 3.6M**) represent niche demand.
* **Micro-Segment Nuance:** Drilling through the Decomposition Tree into **2007 (USD 42.55M)** $\rightarrow$ **United States (USD 12.70M)** $\rightarrow$ **Size L (USD 1.61M)** $\rightarrow$ **Male (USD 798.9K)** reveals that **Blue (USD 274.1K)** and **Yellow (USD 206.1K)** outperform Black (USD 141.3K), driven heavily by the **Touring-1000 (USD 187.6K)** model.

### C. Customer Behavioral Equilibrium
* **Gender Parity:** Profit contribution is virtually split 50/50 between **Male (50.61% / USD 57.1M)** and **Female (49.39% / USD 55.8M)** buyers.
* **Household Composition:** Customers with **0 children** represent the largest volume segment (**175K units**), followed by households with **2 children (125K units)** and **1 child (119K units)**, tapering down to **48K units** for families with 5 children. Married customers account for **9.9K buyers** vs. **8.4K Single buyers**.
* **Multi-Generational Stability:** Profit generation is remarkably uniform across all four age cohorts: **15–25 (USD 28.8M)**, **25–34 (USD 28.0M)**, **35–44 (USD 27.3M)**, and **45–54 (USD 28.8M)**.
* **Top VIP Accounts:** **Jordan Turner** leads individual customer profitability at **USD 78K**, followed closely by **Dawn Nath (USD 62K)**, **Ricky Vazquez (USD 62K)**, **Kate Anand (USD 62K)**, and **Ann Martinez (USD 61K)**.

---

## 💡 5. Strategic Recommendations & Action Plan

1. **Inventory Rationalization & Dead-Stock Liquidation:**
   * Immediately freeze procurement on the **448 unsold SKUs** (which remained above 504 unsold monthly SKUs throughout 2008).
   * Utilize the **What-If Simulation Engine** to structure clearance bundles on slow-moving inventory using promotional discounts strictly capped below the **41.2% Max Safe Discount threshold** to recover working capital without eroding net profitability.
2. **Production & SKU Reallocation by Size and Color:**
   * Allocate **75%+ of manufacturing capacity** to **Size S and Size M** models in **Black, Silver, Red, and Yellow**.
   * Shift **Size XL (USD 3.6M profit)** to a Make-to-Order (MTO) fulfillment model to minimize overproduction.
   * Prioritize **Blue and Yellow Touring-1000** stock specifically for the US male Large-size segment.
3. **European & Canadian Market Expansion:**
   * Replicate the July 2007 catalog expansion strategy across the **United Kingdom (USD 13.4M)**, **Germany (USD 11.4M)**, **France (USD 10.5M)**, and **Canada (USD 8.1M)** to reduce reliance on the US and Australian markets.
4. **Weekend Flash Campaigns & Demographic Bundling:**
   * Launch targeted **Weekend Promotional Campaigns** (Friday night through Sunday) to lift weekend profit share from **28.1% toward 35%+**.
   * Design tailored product bundles targeting **young professionals and small households (0–2 children)**, who collectively purchase **419K of the 622K total units (67.4%)**.

---

## 🧮 6. Core DAX Measures & Simulation Logic

```dax
// 1. Unsold Products Counter (Dynamic Catalog Diagnostic)
Sold Products = DISTINCTCOUNT(Sales[ProductKey])

Available Products = COUNTROWS(Products)

UnSold Products = [Available Products] - [Sold Products]

// 2. What-If Projected Revenue & Profit
Projected Quantity = 
[Total Quantity] * (1 + 'Quantity Change %'[Quantity Change % Value])

Projected Revenue = 
SUMX(
    Sales,
    Sales[OrderQuantity] * (1 + 'Quantity Change %'[Quantity Change % Value]) *
    Sales[UnitPrice] * (1 + 'Price Change %'[Price Change % Value]) *
    (1 - 'Discount %'[Discount % Value])
)

Projected COGS = 
SUMX(
    Sales,
    Sales[OrderQuantity] * (1 + 'Quantity Change %'[Quantity Change % Value]) *
    Sales[UnitCost] * (1 + 'Cost Change %'[Cost Change % Value])
)

Projected Profit = [Projected Revenue] - [Projected COGS]

Projected ROI % = DIVIDE([Projected Profit], [Projected COGS], 0)

// 3. Automated Strategic Decision Signal
Strategic Signal = 
VAR CurrentMargin = DIVIDE([Projected Profit], [Projected Revenue], 0)
RETURN
SWITCH(
    TRUE(),
    CurrentMargin >= 0.35, "🚀 Highly Profitable - Safe to Expand",
    CurrentMargin >= 0.15, "⚖️ Moderate Margin - Monitor Cost Structure",
    CurrentMargin > 0,     "⚠️ Thin Margin - High Promotional Risk",
    "🛑 Loss Territory - Reduce Discount / Cost Immediately"
)
```

---

## 👤 Author & Contact

**Abdallah Rady**  
*Data Analyst & Business Intelligence Specialist*  
* 📧 **Email:** [b99aas@gmail.com](mailto:b99aas@gmail.com)  
* 📱 **Phone / WhatsApp:** +20 1096043027  
