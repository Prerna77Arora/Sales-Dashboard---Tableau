# Sales-Dashboard---Tableau
"This Tableau project brings together sales, customer, product, and geographic data to deliver a 360‑degree view of business performance. Interactive dashboards surface key performance indicators (KPIs) and drill‑downs so analysts and executives can quickly spot trends and outliers."

## Table of Contents

Data Sources

KPIs & Metrics

Dashboards

Getting Started

Project Structure

License

## Project Goals
Consolidate disparate sales data into a single Tableau workbook

Track critical KPIs for quantity, customers, orders, and revenue‐per‑customer

Provide fast visual answers through purpose‑built dashboards (sales, customer, weekly trend, etc.)

Enable non‑technical stakeholders to self‑serve insights

#### Data Sources
| File            | Description                              | Key Columns* |
|-----------------|------------------------------------------|--------------|
| `customer.csv`  | Customer master list                     | `CustomerID`, `CustomerName`, `Segment` |
| `products.csv`  | Product and sub‑category reference       | `ProductID`, `ProductName`, `SubCategory`, `Category` |
| `location.csv`  | Geographic lookup table                  | `LocationID`, `City`, `State`, `Region`, `Country` |
| `orders.csv`    | Line‑level order facts                   | `OrderID`, `OrderDate`, `CustomerID`, `ProductID`, `Quantity`, `Sales` |

> *Exact column names may differ; adjust the data model accordingly in Tableau.

## KPIs & Metrics
| KPI | Definition |
|-----|------------|
| **Quantity** | Sum of items sold (`Quantity`) |
| **Customers** | Count of distinct `CustomerID` with at least one order |
| **Orders** | Count of distinct `OrderID` |
| **Sales per Customer** | `SUM(Sales) / COUNTD(CustomerID)` |
| **Legend KPI** | Color‑encoded status bands for any KPI (e.g., *Good*, *Average*, *Poor*) |
| **Legend Sub‑Category** | Color legend used in sub‑category visualizations |

## Dashboards
| # | Dashboard | Purpose |
|---|-----------|---------|
| 1 | **Sales Dashboard** | High‑level revenue and KPI snapshot with time filters |
| 2 | **Customer Dashboard** | Customer segmentation, LTV, and churn risk insights |
| 3 | **Weekly Trends** | Week‑over‑week movements for quantity, orders, and sales |
| 4 | **Sub‑Category Comparison** | Performance matrix of sub‑categories vs. KPIs |
| 5 | **Customer Distribution** | Geographic density map of customers and sales |
| 6 | **Legend KPI / Legend Sub‑Category** | Re‑usable legends for consistent color semantics |

All dashboards share global filters for **Date Range**, **Product Category**, and **Region** to streamline cross‑analysis.

## Getting Started
1. **Clone or download** this repository and ensure the `/data` folder contains the four CSV files.
2. Open `workbooks/SalesAnalytics.twbx` (built with *Tableau Desktop 2023.3*; earlier versions may prompt for upgrade).
3. Tableau will prompt you to locate each data source; point it to the matching CSV in `/data`.
4. Click **Refresh** to verify row counts, then **Save** the workbook.
5. Explore the dashboards using the filter pane; hover for tooltips and click any mark to drill down.


## Data Refresh
- **Manual**: Replace the CSVs in `/data` with updated extracts (same schema), open the workbook, and click **Refresh**.
- **Automated** (optional): Publish the workbook and data sources to Tableau Server or Tableau Cloud, then schedule an extract refresh.

## Contributing
Pull requests are welcome! When adding a new feature:
- **Do not modify existing dashboards**—create a *new* dashboard or worksheet.
- Include detailed comments in calculated fields for clarity.
- Keep visual design consistent with the existing style guide (colors, fonts, borders).

## License
Distributed under the MIT License. See `LICENSE` for details.

---



