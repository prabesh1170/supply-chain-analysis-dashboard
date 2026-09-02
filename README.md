# Supply Chain Performance & Profitability Dashboard

## Overview
A complete Excel-based supply chain analysis project covering data cleaning, transformation,
formula-based analysis, and dashboard design using Power Query, PivotTables, PivotCharts,
and a broad range of Excel functions (lookup, conditional logic, aggregation, dynamic arrays,
text, and date functions).

## Business Problem
This project analyzes order fulfillment, delivery performance, and profitability across
transportation modes, regions, and suppliers to identify inefficiencies and support
data-driven logistics decisions.

## Dataset
- Source: Supplychain_data.csv — 1,500 orders, 24 columns
- Covers order/shipment/delivery dates, customers, products, suppliers, warehouses,
  transportation, cost, and profit

## Tools Used
- Microsoft Excel (Tables, PivotTables, PivotCharts, formulas)
- Power Query (cleaning, custom columns, conditional logic)
- Excel Functions: XLOOKUP, SUMIFS/COUNTIFS/AVERAGEIFS, IFERROR, nested IF, FILTER,
  TEXT functions, NETWORKDAYS
- GitHub (version control, documentation)

## Data Preparation
Raw CSV kept untouched in `data/raw/`. Working file built separately in `excel/`.
Discovered during import that dates displayed correctly in Excel but were stored as text —
resolved by explicitly setting types in Power Query. Full details: [power-query/documentation.md](power-query/documentation.md)

## Power Query Transformations
Cleaned and validated data, built a custom `Order to Delivery Days` column after discovering
the existing `Delivery Time Days` field was mislabeled (it actually measured shipment-to-delivery,
not order-to-delivery). Built a conditional `Delivery Performance` column, correctly excluding
undelivered orders from performance calculations. Full details: [power-query/documentation.md](power-query/documentation.md)

## Analysis
Four PivotTables covering delivery performance, profit by transport mode, delivery time by mode,
and order status by region. Full details: [documentation/analysis-notes.md](documentation/analysis-notes.md)

## Excel Formula Showcase
Built a supplier performance summary using XLOOKUP and multi-criteria aggregation, a profit
classification column with nested IF, a live dynamic watchlist of loss-making orders using FILTER,
warehouse code extraction with TEXT functions, and business-day delivery calculations with
NETWORKDAYS. Full details: [documentation/formulas-used.md](documentation/formulas-used.md)

## Dashboard
A single-page dashboard combining 5 KPI cards (Total Orders, Total Profit, Average Delivery Time,
On-Time Delivery Rate, Cancellation Rate) with 4 charts covering delivery performance, profitability,
speed, and regional patterns.
![Dashboard Screenshot](screenshots/dashboard-overview.png)

## Key Insights
- 55% of orders were delayed; only 27% were on time
- Rail is most profitable ($1.97M) despite being second-slowest; Air is fastest but least profitable
- Asia has the highest delay rate (~7%); Europe the highest cancellation rate (~4.3%)
- `Delivery Time Days` was found to be mislabeled — actually measures shipment-to-delivery time
- Business-day delivery time (9.16 days) is notably lower than calendar-day time (11.8 days)

Full details: [documentation/business-insights.md](documentation/business-insights.md)

## Project Structure
