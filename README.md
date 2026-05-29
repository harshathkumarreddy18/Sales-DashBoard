# 📊 Sales Overview Dashboard — Power BI

An interactive Power BI sales dashboard built to analyze net sales performance across countries, customers, product categories, and time periods. The dashboard enables data-driven decision-making through dynamic filtering and rich visual storytelling.
## 📌 Overview

This dashboard delivers a comprehensive view of sales performance using a relational dataset spanning **Customers**, **Order Details**, **Categories**, and a **Date Table**. It allows users to monitor key sales KPIs, explore top-performing markets and customers, and identify seasonal revenue trends — all through interactive slicers.

The objective of the dashboard is to surface insights related to:

- Net sales performance across geographies
- Top customers and product categories by revenue
- Monthly sales seasonality and trends
- Year-to-date (YTD) performance tracking
- Per-order and per-customer sales efficiency

---

## 🗄️ Data Model

**Tables Used:**

| Table | Description |
|---|---|
| `Customers` | Customer master data including Country, City, CompanyName |
| `Order_Details` | Transactional sales data; source of all revenue measures |
| `Categories` | Product category reference table |
| `Date Table` | Calendar table supporting time intelligence (YTD, Month, Quarter, Year) |

**Key Measures / Fields:**

| Measure | Description |
|---|---|
| `Net Sales` | Total net revenue from orders |
| `Total_Orders` | Count of all orders placed |
| `Total Customers` | Count of distinct customers |
| `YTD Sales` | Year-to-date cumulative net sales |
| `Sales Per Order` | Average revenue per order |
| `Sales Per Customer` | Average revenue per customer |

---

## 📈 Key Metrics (KPIs)

| Metric | Value |
|---|---|
| **Net Sales** | 1.27M |
| **Total Orders** | 830 |
| **Total Customers** | 89 |
| **YTD Sales** | 440.62K |
| **Sales Per Order** | 1.53K |
| **Sales Per Customer** | 14.22K |

---

## 🔍 Filters & Slicers

| Slicer | Field | Type |
|---|---|---|
| **Country** | `Customers.Country` | Dropdown |
| **City** | `Customers.City` | Dropdown |
| **Category Name** | `Categories.CategoryName` | Dropdown |
| **Date** | `Date Table.Date` | Date Range Picker |

All slicers cross-filter every visual on the page simultaneously.

---

## 📊 Visuals Included

### 1. KPI Cards *(6 Cards)*
Prominent headline metrics displayed at the top of the report:
`Net Sales` · `Total Orders` · `Total Customers` · `YTD Sales` · `Sales Per Order` · `Sales Per Customer`

### 2. Net Sales by Country *(Treemap)*
Visualizes revenue contribution sized proportionally by country.

Top markets: 🇺🇸 USA · 🇩🇪 Germany · 🇦🇹 Austria · 🇫🇷 France · 🇸🇪 Sweden · 🇧🇷 Brazil · 🇬🇧 UK · 🇨🇦 Canada · 🇮🇪 Ireland · Belgium · Denmark · Switzerland · Venezuela · Italy

### 3. Net Sales by Month *(Line Chart)*
Plots `Net Sales` against a drill-down Date Hierarchy (Year → Quarter → **Month** → Day).

- Peak performance around **May**
- Mid-year dip through **June–August**
- Recovery and upward trend heading into **December**

### 4. Net Sales by Customer *(Clustered Bar Chart)*
Ranks customers by `Net Sales`.

Top customers: QUICK-Stop · Ernst Handel · Save-a-lot Markets · Rattlesnake Canyon Grocery · Hungry Owl All-Night Grocers · Hanari Carnes · Königlich Essen · Folk och fä HB · Mère Paillarde · White Clover Markets

### 5. Net Sales by Category *(Clustered Bar Chart)*
Ranks product categories by `Net Sales`.

🥤 Beverages · 🧀 Dairy Products · 🍬 Confections · 🥩 Meat/Poultry · 🐟 Seafood · 🧂 Condiments · 🥦 Produce · 🌾 Grains/Cereals

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — Report authoring and publishing
- **DAX** — Calculated measures (Net Sales, YTD Sales, Sales Per Order, Sales Per Customer, Total Customers, Total Orders)
- **Power Query (M)** — Data transformation, table relationships, and Date Table construction
