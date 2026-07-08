<div align="center">

# 🛒 Blinkit Sales Analysis Dashboard

### Interactive Power BI Dashboard for Sales, Inventory & Outlet Performance Insights

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-6D28D9?style=flat-square&logo=powerbi&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-Data%20Cleaning-217346?style=flat-square&logo=microsoftexcel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-8B5CF6?style=flat-square&logo=powerbi&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-4C1D95?style=flat-square)

</div>

---

## 📌 Overview

The **Blinkit Sales Analysis Dashboard** is an interactive Power BI project built to analyze sales performance across product categories, outlet types, and geographic locations for a quick-commerce grocery business. The dashboard transforms raw, unstructured sales data into a clean, drill-down-capable analytical tool that surfaces revenue trends, underperforming segments, and inventory-relevant patterns to support faster, data-backed business decisions.

This project simulates a real-world business intelligence engagement — from raw data ingestion to a stakeholder-ready reporting layer.

---

## 🎯 Business Problem

Retail and quick-commerce businesses generate large volumes of transactional data across categories, outlets, and regions, but that data is rarely useful in raw form. Decision-makers need:

- A clear view of **which categories and outlets drive the most revenue**
- Visibility into **underperforming segments** that need attention
- The ability to **filter and drill down** without waiting on manual reports

This dashboard was built to solve exactly that.

---

## 🏗️ Project Workflow

```
Raw Sales Data (CSV/Excel)
        │
        ▼
Data Cleaning & Transformation (Power Query)
        │
        ▼
Data Modeling (Relationships, Star Schema)
        │
        ▼
DAX Measures (KPIs, Aggregations, Ratios)
        │
        ▼
Interactive Power BI Report (Drill-down, Filters, Visuals)
```

---

## ⚙️ Tech Stack

| Component | Tool |
|-----------|------|
| **Data Cleaning & Transformation** | Power Query |
| **Data Modeling & KPI Logic** | DAX (Data Analysis Expressions) |
| **Reporting & Visualization** | Power BI Desktop |
| **Pre-processing** | Microsoft Excel |

---

## 📊 Dataset

| Detail | Description |
|--------|-------------|
| **Size** | 10,000+ sales records |
| **Granularity** | Category-level, outlet-level, and geo-based records |
| **Key Fields** | Product category, outlet type, outlet location, sales amount, item visibility, item weight, outlet establishment year |

> Note: Dataset used is a publicly available Blinkit/BigMart-style retail sales dataset, used here purely for analytical demonstration purposes.

---

## ✨ Key Features

- 📈 **8+ DAX-based KPI measures** covering total sales, average sales per outlet, category contribution %, and more
- 🔍 **Dynamic drill-down filtering** across category, outlet type, and location
- 🧹 **Fully cleansed and modeled dataset** ensuring consistency across every reporting view
- 🗂️ **Multi-dimensional analysis** — category-level, outlet-level, and geographic-level insights in a single report
- ⚡ **Real-time interactive filtering** with no report reload required

---

## 🖼️ Dashboard Preview

<div align="center">

*(Add a screenshot of your dashboard here once exported)*

```
![Dashboard Preview](assets/dashboard_preview.png)
```

</div>

To add this yourself: export a screenshot of your Power BI report (File → Export → Export to Image, or a simple screen capture), upload it to an `assets/` folder in this repo, and reference it with the markdown above.

---

## 📐 Key DAX Measures (Examples)

```dax
Total Sales = SUM(Sales[Sales_Amount])

Average Sales per Outlet =
DIVIDE([Total Sales], DISTINCTCOUNT(Sales[Outlet_ID]))

Category Contribution % =
DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Sales[Category])))

YoY Sales Growth =
VAR CurrentYearSales = [Total Sales]
VAR PreviousYearSales =
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
RETURN
    DIVIDE(CurrentYearSales - PreviousYearSales, PreviousYearSales)
```

*(Replace with your actual DAX formulas from the .pbix file for full accuracy.)*

---

## 📂 Project Structure

```
Blinkit-PowerBI-Dashboard/
├── data/
│   └── blinkit_sales_data.csv       # Raw dataset (or link if too large for repo)
├── Blinkit_Sales_Dashboard.pbix     # Main Power BI report file
├── assets/
│   └── dashboard_preview.png        # Dashboard screenshot(s)
├── docs/
│   └── dax_measures.md              # Full list of DAX measures used
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop) (free, Windows only)

### Steps to Run

```bash
git clone https://github.com/Praveen071909/Blinkit-PowerBI-Dashboard.git
```

1. Open **Power BI Desktop**
2. Go to **File → Open Report**
3. Select `Blinkit_Sales_Dashboard.pbix` from the cloned folder
4. Use the slicers/filters on the report to explore category, outlet, and location-level insights

---

## 📈 Key Insights Uncovered

- Identified top-performing product categories driving majority of overall revenue
- Surfaced underperforming outlet types requiring inventory or pricing strategy review
- Highlighted regional performance gaps to guide geographic expansion or resource allocation decisions

*(Update this section with your specific, real findings from the dashboard for maximum impact.)*

---

## 🔮 Future Improvements

- [ ] Add time-based trend analysis (monthly/quarterly sales seasonality)
- [ ] Integrate a live data source connection instead of static CSV
- [ ] Publish report to Power BI Service for web-based sharing
- [ ] Add predictive sales forecasting using Power BI's built-in forecasting or Python integration

---

## 🤝 Contributing

Suggestions and improvements are welcome. Feel free to open an [issue](https://github.com/Praveen071909/Blinkit-PowerBI-Dashboard/issues) or submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👤 Author

**Praveen D**
[GitHub](https://github.com/Praveen071909) · [LinkedIn](https://www.linkedin.com/in/praveen-d-707884281) · praveend@karunya.edu.in

