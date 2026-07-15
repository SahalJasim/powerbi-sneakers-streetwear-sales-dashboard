# powerbi-sneakers-streetwear-sales-dashboard
Interactive Power BI dashboard analyzing Sneakers &amp; Streetwear sales performance using KPIs, geographic insights, sales trends, product categories, and customer purchasing behavior.

# 👟 Sneakers & Streetwear Sales Dashboard

An interactive Power BI dashboard analyzing global sneaker and streetwear sales data across brands, countries, product types, and time periods.

---

## 📁 Project Overview

| Detail | Info |
|---|---|
| **Tool** | Microsoft Power BI |
| **Dataset** | Sneakers & Streetwear Sales Data (Kaggle) |
| **Period** | January – August 2022 |
| **Records** | 353 transactions |
| **Countries** | 7 (UK, USA, Canada, Japan, Germany, Australia, India) |
| **Brands** | Nike, Adidas, Puma, Supreme, Off-White, New Era, Essentials |

---

## 🎯 KPIs Tracked

- 💰 **Total Amount** — Overall sales value across all transactions
- 📦 **Total Orders** — Number of transactions
- 👟 **Total Quantity** — Units sold
- 📈 **Avg Order Value** — Average revenue per order

---

## 📈 Charts & Visuals

| Visual | Chart Type | Purpose |
|---|---|---|
| Amount by Month | Line Chart | Track sales trend over time |
| Amount by Brand | Bar Chart | Compare brand performance |
| Amount by Country | Map Visual | Geographic sales distribution |
| Orders by Category | Donut Chart | Category-wise order split |
| Top Products | Table | Product-level performance breakdown |
| Revenue vs Target | Gauge | Track progress toward sales goal |

---

## 🎛️ Slicers / Filters

- 📅 Date Range
- 🏷️ Brand
- 🌍 Country
- 👤 Gender

---

## 🛠️ Data Cleaning (Power Query)

- Changed `Date` column from Text → Date type
- Extracted date parts: Year, Month Name, Month Number, Quarter
- Added Custom Column: `Amount (INR)` = Amount ($) × exchange rate
- Verified `Amount` = `Quantity × Unit Price` across all rows
- Confirmed no null values or duplicate records

---

## 📐 DAX Measures Created

```dax
Total Amount = SUM('Table'[Amount ($)])
Total Orders = COUNTROWS('Table')
Total Quantity = SUM('Table'[Quantity])
Avg Order Value = DIVIDE([Total Amount], [Total Orders])
Avg Unit Price = AVERAGE('Table'[Unit Price ($)])
```

---

## 📂 Files in This Repository

```
📁 Sneakers-Streetwear-Dashboard/
├── sneakers_streetwear_sales_data.csv   # Raw dataset
├── SneakersDashboard.pbix               # Power BI file
├── dashboard_preview.png                # Dashboard screenshot
└── README.md                            # Project documentation

---

