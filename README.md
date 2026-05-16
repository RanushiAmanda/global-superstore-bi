# 🏬 Global Superstore Retail Analytics
### Business Intelligence & Data Warehouse Solution

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![SSIS](https://img.shields.io/badge/SSIS-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual%20Studio-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)

---

## 📌 Project Overview

An end-to-end **Business Intelligence and Data Warehouse solution** built on 51,000+ global retail transactions from the Global Superstore dataset. This project covers the full BI lifecycle — from raw data ingestion through ETL pipelines to interactive Power BI dashboards that support strategic business decision-making.

---

## 🎯 Objectives

- Design and implement a scalable **Star Schema** data warehouse
- Build **ETL pipelines** to integrate data from multiple sources
- Enable **multidimensional OLAP analysis** with drill-down capabilities
- Deliver **interactive Power BI dashboards** for KPI-driven insights
- Support business decisions around **sales, profit, discounts, shipping, and regional performance**

---

## 🏗️ Architecture

```
Raw Data Sources          ETL Layer            Data Warehouse         Analytics Layer
─────────────────    ─────────────────    ──────────────────    ─────────────────────
SQL Server       →                    →                      →
CSV Files        →   SSIS Pipelines   →   Star Schema (DW)   →   SSAS Cube + Power BI
Excel Files      →                    →                      →
```

---

## 🗄️ Data Warehouse Design

### Star Schema
- **Fact Table** — Sales transactions with accumulating metrics
- **Dimension Tables** — Customer, Product, Geography, Date, Shipping
- **SCD Type 2** — Customer history tracking for segmentation analysis

### Key Design Decisions
- Accumulating fact tables for process lifecycle analysis
- Slowly Changing Dimensions (SCD Type 2) for customer history
- Conformed dimensions for cross-functional reporting

---

## ⚙️ ETL Pipeline (SSIS)

| Component | Description |
|-----------|-------------|
| **Data Sources** | SQL Server, CSV, Excel |
| **Transformations** | Data cleansing, type conversions, lookups, derived columns |
| **SCD Handling** | Type 2 for customer dimension |
| **Error Handling** | Redirect rows, logging |
| **Load Strategy** | Incremental load with staging tables |

---

## 📦 SSAS Multidimensional Cube

- **Hierarchies** — Product (Category → Sub-Category → Product), Geography (Region → Country → City)
- **OLAP Operations** — Roll-up, Drill-down, Slice, Dice, Pivot
- **Measures** — Sales, Profit, Discount, Quantity, Shipping Cost
- **KPIs** — Profit Margin, Sales Growth, Discount Rate

---

## 📊 Power BI Dashboards

### Dashboard 1 — Sales Performance
- Revenue trends with drill-down by year, quarter, month
- Top 10 products by sales and profit
- Cascading slicers for dynamic filtering

### Dashboard 2 — Regional Analysis
- Geographic heat map of sales distribution
- Country and city level drill-through
- Comparative regional performance

### Dashboard 3 — Customer Segmentation
- Customer segments by profitability
- Purchase frequency analysis
- SCD-based customer history trends

### Dashboard 4 — Operational KPIs
- Shipping mode analysis and cost breakdown
- Discount impact on profit margins
- Matrix reporting with conditional formatting

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **SQL Server** | Data warehouse storage |
| **SSIS** | ETL pipeline development |
| **SSAS** | Multidimensional cube |
| **Power BI** | Interactive dashboards |
| **T-SQL** | Stored procedures & queries |
| **Excel** | Source data & PivotTables |
| **Visual Studio** | SSIS & SSAS development |

---

## 📁 Repository Structure

```
global-superstore-bi/
├── README.md
├── GlobalSuperstore.pbix          # Power BI project file
├── reports/
│   ├── sales-report.pdf
│   ├── regional-analysis.pdf
│   └── kpi-summary.pdf
├── screenshots/
│   ├── dashboard1-sales.png
│   ├── dashboard2-regional.png
│   ├── dashboard3-customers.png
│   └── dashboard4-kpis.png
└── sql/
    └── schema.sql                 # DW schema scripts
```

---

## 🚀 How to Run

1. **Restore the database** using SQL Server Management Studio (SSMS)
2. **Run SSIS packages** in Visual Studio to load data
3. **Process the SSAS cube** in Visual Studio
4. **Open `GlobalSuperstore.pbix`** in Power BI Desktop
5. **Connect to your local SSAS cube** or SQL Server instance

---

## 📈 Key Insights Delivered

- Identified top-performing regions contributing 60%+ of total revenue
- Revealed discount strategies negatively impacting profit margins by up to 30%
- Tracked customer lifetime value trends using SCD Type 2 history
- Highlighted shipping mode inefficiencies affecting operational costs

---

## 👩‍💻 Author

**Ranushi Amanda**
BSc (Hons) Information Technology — Data Science | SLIIT

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ranushi-amanda-b135572ba)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/RanushiAmanda)
[![Blog](https://img.shields.io/badge/Blog-FF5722?style=flat&logo=blogger&logoColor=white)](https://ranu001coding.blogspot.com)

---

> *"Turning 51,000+ transactions into strategic insights — one dashboard at a time."*
