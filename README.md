# 📊 Sales & Profitability Dashboard 

This project is a practical Power BI report built from a typical retail sales dataset.  
The goal is to show how a business analyst can turn raw transaction data into clear,
actionable insights about sales, profit, and profitability across regions, categories,
and products.

---

## ⭐ Project Overview

The dashboard answers questions like:

- Which regions generate the most **sales and profit**?
- Which **categories and products** drive performance?
- How do **sales trends** change over time?
- Where is **profit margin** strong or weak?

What I focused on:

- Clean, easy-to-read layout 
- Core DAX measures for Total Sales, Total Profit, and Profit Margin %
- Interactive filters for slicing by Year, Region, and Category
- Visuals that a stakeholder can understand without explanation
- A short “story” of the business built from the charts

---

## 📂 Files in this Repository

| File | Purpose |
|------|---------|
| `Sales_Profitability_Dashboard.pbix` | Main Power BI report file |
| `dataset.csv` *(optional if included)* | Source data used by the report |
| `README.md` | Project documentation (this file) |
| `dashboard_overview.png` | Screenshot of the main dashboard view |

---

## 🧱 Data Model & Measures

The model is intentionally simple so the focus stays on analysis and storytelling.

**Main table**

- `train` – transactional sales table containing:  
  `Order Date`, `Region`, `Category`, `Sub-Category`, `Product Name`, `Sales`, `Profit`, `Profit Margin %`, etc.

**Key measures (DAX)**

- `Total Sales = SUM('train'[Sales])`
- `Total Profit = SUM('train'[Profit])`
- `Profit Margin % = DIVIDE([Total Profit], [Total Sales])`

The built-in **Date hierarchy** on `Order Date` is used for Year-level analysis.

---

## 📊 Dashboard Layout & Visuals

The main page is designed as an **executive overview**:

- **KPI Cards**
  - Total Sales
  - Total Profit
  - Profit Margin %

- **Trend**
  - Line chart: **Sales by Year**

- **Comparisons**
  - Bar chart: **Profit by Region**
  - Bar chart: **Sales by Category**
  - Bar chart: **Top Products by Sales**

- **Filters / Slicers**
  - Year
  - Region
  - Category

All visuals react to the slicers so a user can quickly narrow the view to a specific
region, product category, or year.

---

## 🔍 Example Insights

A few example insights that the dashboard surfaces (will depend on the exact data):

- Sales grow steadily over the later years, with **2018** being the strongest year.
- **West** and **East** regions contribute a large share of total profit.
- The **Technology** category leads in sales, followed by **Furniture** and **Office Supplies**.
- A small set of top products accounts for a significant portion of total revenue.

These are the kinds of observations a business analyst could take into a meeting with
sales or regional managers.

---

## ▶️ How to Open & Explore

1. Download `Sales_Profitability_Dashboard.pbix`.
2. Open it with **Power BI Desktop** (free from Microsoft Store).
3. Use the slicers at the top of the report to filter by:
   - Year
   - Region
   - Category
4. Hover over charts for tooltips and more detail.
5. Use the KPIs at the top as a quick health check before digging into specific charts.

---

## 🎯 What This Project Demonstrates

From a **Business Analyst** perspective, this project shows:

- Ability to take a raw sales table and turn it into a **clear data model**.
- Use of **DAX measures** for core business metrics (Sales, Profit, Margin).
- Building a **single-page executive dashboard** that’s easy to interpret.
- Using slicers and consistent formatting to create a **professional, interactive report**.
- Communicating findings through both **visuals and written insights**.


