# 📦 Inventory Analysis Dashboard
**Power BI Business Intelligence Project | Power BI · Power Query · DAX · Data Analytics**

---

## 📌 Project Overview

Most businesses lose money not because they sell too little, but because they manage inventory too poorly.

This project presents an end-to-end **Inventory Analysis Dashboard** built in Microsoft Power BI, designed to help businesses make faster, smarter decisions on stock management. Using raw stock and sales data, I transformed numbers into an interactive dashboard that tracks revenue performance, inventory health, stock movement, and regional sales — giving decision-makers real-time visibility at a glance.

> **The goal was simple:** Turn raw stock and sales data into a dashboard that drives action — not just reports numbers.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard development, DAX measures, interactive visuals |
| Power Query (M) | Data cleaning, transformation and structuring |
| DAX | KPI calculations and dynamic measures |
| PowerPoint | Custom layout wireframing before Power BI build |
| Power BI Service | Dashboard publishing and sharing |

---

## 📂 Repository Structure

```
inventory-analysis-dashboard/
│
├── dashboard/
│   └── Inventory_Analysis_Dashboard.pbix     # Power BI file
│
├── data/
│   └── inventory_sales_data.csv              # Raw dataset
│
├── assets/
│   ├── dashboard_screenshot.png              # Dashboard preview
│   └── wireframe_layout.png                  # PowerPoint wireframe
│
└── README.md
```

---

## 📊 Key Performance Indicators

| KPI | Value |
|-----|-------|
| 💰 Total Revenue | $495M |
| 📦 Inventory Value | $997M |
| 🗃️ Stocks Available | 20M units |
| 📅 Days of Inventory on Hand (DOH) | 59 days |
| 🔄 Inventory Turnover Rate | 12.43 |


![My Image](https://github.com/R887645/-Inventory-Analysis-Dashboard/blob/main/Inventory%20Analysis%20Dashboard.png?raw=true)
---

## ⚙️ Project Pipeline

```
Phase 1 → Data Loading & Understanding
Phase 2 → Data Cleaning & Transformation (Power Query)
Phase 3 → Data Modelling
Phase 4 → DAX Measures & KPI Calculations
Phase 5 → Dashboard Design & Layout (PowerPoint Wireframe)
Phase 6 → Dashboard Build (Power BI)
Phase 7 → Insights & Recommendations
```

---

## 🧹 Phase 1–2: Data Loading & Transformation

### Power Query Transformation Steps

All data cleaning and structuring was done entirely in **Power Query (M language)** before loading into the Power BI data model. Key transformation steps included:

- Removed duplicate rows and null values
- Standardised column data types (dates, currency, integers)
- Created calculated columns for inventory value and days on hand
- Merged stock and sales tables on product and region keys
- Filtered out inactive or discontinued product records
- Renamed columns for dashboard-ready labelling

---

## 🔄 Phase 3: Data Modelling

The data model connects stock, sales, product, and region tables through a clean star schema — ensuring fast, accurate filtering across all dashboard visuals.

```
Sales Table (Fact)
    ↓
Date Table (Dimension)
```
![My Image](https://github.com/R887645/-Inventory-Analysis-Dashboard/blob/main/Screenshot%202026-06-28%20031410.png?raw=true)
---

## 💻 Phase 4: DAX Measures

Key DAX measures built to power the dashboard KPIs and dynamic visuals:

```dax
-- Total Revenue
Total Revenue = SUMX(Sales, Sales[Units Sold] * Sales[Unit Price])

-- Inventory Value
Inventory Value = SUMX(Inventory, Inventory[Stock Available] * Inventory[Unit Cost])

-- Days of Inventory on Hand (DOH)
DOH = 
DIVIDE(
    [Inventory Value],
    DIVIDE([Total Revenue], 365),
    0
)

-- Inventory Turnover Rate
Inventory Turnover = 
DIVIDE(
    [Total Revenue],
    [Inventory Value],
    0
)

-- Units Sold by Region
Units Sold = SUM(Sales[Units Sold])
```

---

## 🎨 Phase 5: Dashboard Design

Before opening Power BI, a **custom layout was designed in PowerPoint** — mapping out the position of every KPI card, chart, button, and slicer. This wireframing step prevented rework and ensured a professional, structured final output.

Design decisions included:
- Clean, minimal colour palette for executive readability
- KPI cards at the top — most important numbers at first glance
- Charts positioned following the **F-pattern layout** (left-to-right, top-to-bottom)
- Custom SVG icons and bookmarks for smoother navigation between views
- Interactive buttons for a polished, app-like user experience

---

## 📈 Phase 6: Dashboard Features

### KPI Cards
Four headline KPI cards display the most critical business metrics at a glance — Total Revenue, Inventory Value, Stocks Available, and Inventory Turnover Rate.

### Inventory Value by Category
Furniture and Groceries lead inventory value, almost evenly matched at approximately **$201M each** — signalling that these two categories carry the highest stock risk and require the closest monitoring.

### Regional Sales Performance
| Region | Units Sold |
|--------|-----------|
| East | 2,511K units |
| South | Second highest |
| West | Lowest — opportunity for targeted action |

The East region leads in unit sales, followed closely by South — showing relatively balanced regional performance across most of the business.

### Monthly Stock Movement
Stock movement across months is **stable with no major spikes or crashes** — a positive signal of healthy demand planning and consistent supply chain management.

### Interactive Elements
- **Bookmarks** for switching between dashboard views
- **Navigation buttons** for smooth page transitions
- **Slicers** for filtering by region, category, and date
- **Custom SVG icons** for a professional, branded look

---

## 🔍 Phase 7: Key Insights & Recommendations

### Key Insights

| # | Insight |
|---|---------|
| 1 | Furniture and Groceries dominate inventory value at ~$201M each — highest stock exposure |
| 2 | East region leads unit sales at 2,511K — closely followed by South |
| 3 | Monthly stock movement is stable — no demand spikes signal healthy planning |
| 4 | Turnover rate of 12.43 means stock is moving fast — stockout risk needs monitoring |
| 5 | Electronics is a slow-moving category — even a small percentage drop has large value impact |

### Recommendations

| # | Recommendation | Business Impact |
|---|---------------|----------------|
| 1 | Monitor slow-moving categories like Electronics closely | Prevent capital being tied up in unsold stock |
| 2 | Run targeted promotions or improve stock allocation in the West region | Close the unit sales gap between East and West |
| 3 | Track Days of Inventory on Hand (DOH) monthly, not just annually | Catch overstocking or understocking before it becomes costly |
| 4 | Automate this dashboard for real-time visibility | Eliminates hours of manual reporting for decision-makers |
| 5 | Set reorder alerts for high-turnover categories | Prevent stockouts in fast-moving product lines |

---

## 🎯 What I Focused On

| Focus Area | Approach |
|------------|---------|
| Data transformation | Clean, well-structured Power Query pipeline |
| KPI design | Cards designed to tell a story, not just display numbers |
| User experience | Bookmarks, buttons, and SVGs for smoother navigation |
| Layout | Custom layout wireframed in PowerPoint before building |
| Storytelling | Every visual positioned to guide the viewer to an insight |

---

## 🔗 Live Dashboard

> 🌐 **[View Live Dashboard on Power BI Service](#)** *(link coming soon)*

---

## 📄 Deliverables

| Deliverable | Description |
|-------------|-------------|
| `Inventory_Analysis_Dashboard.pbix` | Full interactive Power BI dashboard |
| `inventory_sales_data.csv` | Raw dataset used for analysis |
| `README.md` | Full project documentation |

---

## 🙌 Acknowledgements

Special shoutout to **Chiamaka Igwe** for the tutorial inspiration behind this build. 🙏

---

## 👩‍💻 Author

**Abdul-Azeez Rofiah Kehinde**
Business Intelligence Analyst · Data Analyst · Power Platform Enthusiast

Helping businesses turn data into clear, actionable insights. If you're looking to make smarter, data-driven decisions — let's connect.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/rofiah-abdul-azeez/)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-navy)](https://rofiahportfolio.mystrikingly.com/)

---

## 🏷️ Tags

`#PowerBI` `#DataAnalytics` `#DataVisualization` `#InventoryManagement` `#BusinessIntelligence` `#DataAnalyst` `#PowerBIDashboard` `#DataDrivenDecisions` `#RetailAnalytics`

---

*Data is powerful — but only when it's visualised in a way people can actually act on. That's the part of this work I find most fulfilling.*
