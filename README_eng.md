# AdventureWorks BI Dashboard | SQL + Power BI

## Project Description

Interactive analytics dashboard for AdventureWorks company (2001–2004).
The project demonstrates the full analytics cycle: from loading data into the database
to visualizing financial metrics, customer segmentation, and what-if scenarios.

## Data Source

- **Database:** AdventureWorks (Microsoft), adapted for MySQL
- **Source:** [tapsey/AdventureWorksMYSQL](https://github.com/tapsey/AdventureWorksMYSQL)
- **Deployment:** local MySQL installation + DBeaver

## Data Structure

| Table | Rows | Description |
|-------|------|-------------|
| SalesOrderHeader | 31,465 | Order headers |
| SalesOrderDetail | 121,317 | Order line items |
| Product | 504 | Products |
| Customer | 19,185 | Customers |
| SalesTerritory | 10 | Sales territories |

## Technology Stack

| Component | Tool |
|-----------|------|
| Database | MySQL 8.0 |
| SQL queries | CTE, window functions, JOIN, aggregates |
| ETL / modeling | Power BI (Import mode) |
| Visualization | Power BI Desktop |
| Design | Custom theme |

## Dashboard Pages

### 1. Executive Summary
- KPIs: Revenue, Gross Profit, Operating Profit, Operating Margin %
- Revenue and profit dynamics by year (2001–2004)
- Combo chart: Revenue + Profit + Margin % with dual axes
- Insights in English

### 2. Product & Margin Analysis
- Top 20 loss-making products with conditional formatting
- Color coding: 🔴 Critical loss 🟡 Unprofitable 🟢 Profitable
- Category filters (buttons): Accessories, Bikes, Clothing, Components
- Stacked bar: margin structure by category

### 3. Territory & Sales Team
- Margin by 10 territories with target line (average margin)
- Color coding: green (positive) / red (negative)
- Sales manager table sorted by margin
- Insights in English

### 4. Customer Segments (RFM)
- RFM segmentation: Champions, Loyal, At Risk, Lost, etc.
- Combo chart: Customer Count + Avg Bill by segment
- Insights in English

### 5. P&L Financial Waterfall
- Profit waterfall: Revenue → COGS → Gross Profit → Freight → Tax → Operating Profit
- What-if scenarios:
  - Tax reduction % (0–50%)
  - Price increase % (0–20%)
- Interactive Adjusted Operating Profit calculation
- Insights in English

## Key Findings

| Metric | Value |
|--------|-------|
| Total Revenue | $109.85M |
| Gross Profit | $9.37M (8.53%) |
| **Operating Profit** | **−$4.00M (−3.64%)** |
| Online Revenue | 27% of revenue, 40% margin |
| Offline Revenue | 73% of revenue, −2.88% margin |

## Project Files

| File | Description |
|------|-------------|
| `SQL_scripts_BI.txt` | All SQL queries: fact_orders, RFM, P&L waterfall |
| `AdventureWorks.pbix` | Power BI dashboard |
| `draft_AdventureWorks_SQL.pdf` | Dashboard screenshots |
| `dax/measures.txt` | DAX measures (added later) |
| `README_eng.md` | Project description |

## Project Features

- **Dashboard language:** English (data and business terminology in English)
- **README language:** English
- **Conditional formatting:** color coding for loss-making products and territories
- **What-if analysis:** interactive scenarios for taxes and pricing
- **Target line:** average margin benchmark on territory chart