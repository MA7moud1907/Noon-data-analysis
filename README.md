# 🛒 Noon Sales Analytics Dashboard (Power BI)

An interactive Power BI dashboard analyzing e-commerce sales performance, styled after **Noon.com**—one of the largest online retail platforms in the Middle East. This project transforms raw internet sales data into an executive-ready report covering revenue, orders, customers, and product/territory performance.

---

## 📊 Project Overview

This report simulates a real-world business intelligence use case for an e-commerce platform: consolidating sales, product, currency, and territory data into a unified data model to construct a multi-page interactive dashboard. Stakeholders can easily drill down from high-level executive KPIs to granular, transaction-level details.

* **Primary File:** `Noon_project.pbix`

---

## 🧭 Report Pages

| Page | Purpose |
| :--- | :--- |
| **Home Page** | Landing & navigation hub with brand alignment and entry points to the report sections. |
| **Overview Page** | Executive KPI summary featuring total sales, orders, active users, profit margin, target vs. actual metrics, and revenue trends over time. |
| **Sales Breakdown** | Advanced analytical view with trend lines, a decomposition tree for root-cause exploration, and category/territory performance metrics. |
| **Table of Sales** | Detailed, filterable transaction log equipped with cross-report slicers for ad-hoc data analysis. |

---

## 📈 Key Metrics & Visuals

* **KPI Cards:** Total Sales, Number of Orders, Active Users, Net Profit, Profit Margin %, Average Order Value (AOV), and Best-Performing Month.
* **Trend Analysis:** Line charts mapping sales performance over time alongside Year-to-Date (YTD) tracking.
* **Comparative Views:** Clustered bar charts and donut charts broken down by product category and geographic territory.
* **Root-Cause Analysis:** Interactive decomposition tree allowing users to isolate key sales drivers dynamically.
* **Detail Table:** Fully sortable and filterable matrix of individual transaction records.
* **Interactivity:** Integrated slicers for date ranges, territories, products, and dimensions cross-filtered across all pages.

---

## 🗂️ Data Model

The project architecture relies on a **Star Schema** data model featuring a central fact table surrounded by dimension tables:

* `fact_InternetSales`: Transaction-level sales fact table (sales amount, product cost, quantity, order info).
* `dim_Product`: Product metadata and categorization attributes.
* `dim_SalesTeritory`: Regional and geographic metadata (country, region, sales group).
* `dim_Currency`: Currency reference and conversion mapping table.
* `calendar`: Dedicated date dimension supporting time-intelligence functions.
* `measuers`: Container table holding all custom DAX calculations.

---

<img width="1335" height="767" alt="Screenshot 2026-10-02 181108" src="https://github.com/user-attachments/assets/96b64509-fb12-4ef0-9a3a-d3aa4839b7b8" />
<img width="1377" height="761" alt="noon2" src="https://github.com/user-attachments/assets/cdc8416a-14ad-4374-9c03-1ee0ef85d91a" />
<img width="1352" height="767" alt="noon3" src="https://github.com/user-attachments/assets/f784e498-6acd-40c0-b9e9-0806741dd7ec" />
<img width="1362" height="746" alt="noon 4" src="https://github.com/user-attachments/assets/b9847ce4-2e01-476b-9a9a-6f0a46522045" />



