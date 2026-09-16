Noon Sales Analytics Dashboard (Power BI)
An interactive Power BI dashboard analyzing e-commerce sales performance, styled after Noon.com, one of the largest online retail platforms in the Middle East. The project transforms raw internet sales data into an executive-ready report covering revenue, orders, customers, and product/territory performance.
   
________________________________________
📊 Project Overview
This report simulates a real-world business intelligence use case for an e-commerce company: consolidating sales, product, currency, and territory data into a single data model, then building a multi-page report that lets stakeholders drill from a high-level overview down to transaction-level detail.
File: Noon_project.pbix
🧭 Report Pages
Page	Purpose
Home Page	Landing/navigation page with branding and entry points into the report
Overview Page	Executive KPI summary — total sales, orders, users, profit margin, target vs. actual, and sales trend over time
Sales Breakdown	Deeper analysis with trend lines, a decomposition tree for root-cause exploration, and category/territory breakdowns
Table of Sales	Detailed, filterable transaction-level table with slicers for ad-hoc exploration
📈 Key Metrics & Visuals
•	KPI Cards: Total Sales, Number of Orders, Number of Users/Active Users, Net Profit, Profit Margin %, Average Order Value (AOV), Best-Performing Month
•	Trend Analysis: Line charts for sales over time with Year-to-Date (YTD) tracking
•	Comparative Views: Clustered bar charts and donut charts by product/territory
•	Root-Cause Analysis: Decomposition tree to break down sales drivers interactively
•	Detail Table: Sortable/filterable table of individual transactions
•	Interactivity: Slicers for date, territory, product, and other dimensions across all pages
🗂️ Data Model
The report is built on a star schema with one fact table and supporting dimensions:
•	fact_InternetSales — transaction-level sales fact table (sales amount, product cost, quantity, order info)
•	dim_Product — product attributes (e.g., product name)
•	dim_SalesTeritory — geography/territory attributes (country, region/group)
•	dim_Currency — currency reference data
•	calendar — date dimension used for time intelligence
•	measuers — dedicated measures table holding all DAX calculations
🧮 Sample DAX Measures
Profit Margin % =
VAR Sales = SUM(fact_InternetSales[SalesAmount])
VAR Cost = SUM(fact_InternetSales[TotalProductCost])
RETURN DIVIDE(Sales - Cost, Sales)

YTD Sales =
CALCULATE(
    SUM(fact_InternetSales[SalesAmount]),
    DATESYTD(calendar[Date])
)
Other measures in the model include Total Sales, AOV, Net Profit, Number of Orders, Number of Users / Active Users, and Target vs. actual comparisons.
🎨 Design
The report uses a custom Power BI theme aligned to Noon's brand palette (yellow/black), along with custom icons and logo imagery for a polished, product-like feel.
🛠️ Tools & Skills Demonstrated
•	Power BI Desktop (data modeling, report design)
•	DAX (time intelligence, ratio/margin calculations, custom measures)
•	Star-schema data modeling
•	Interactive dashboard design (slicers, drill-through, decomposition tree)
•	KPI and executive reporting design
🚀 How to View
1.	Download Noon_project.pbix
2.	Open it in Power BI Desktop (free download from Microsoft)
3.	Explore the report pages using the tabs at the bottom and the slicers on each page
📌 Notes
This is a portfolio/practice project intended to demonstrate Power BI and DAX skills using an e-commerce sales dataset styled with Noon branding for presentation purposes.
