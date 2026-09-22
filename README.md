<div align="center">

# Pizza Sales Report

### Power BI Business Intelligence Dashboard for Pizza Sales Analysis

<p>
  An interactive Power BI dashboard designed to analyze revenue, orders, pizza quantity, product performance, sales trends, pizza categories, and pizza sizes.
</p>

<p>
  <a href="#project-overview">Overview</a> &nbsp;•&nbsp;
  <a href="#dashboard-preview">Dashboard</a> &nbsp;•&nbsp;
  <a href="#key-performance-indicators">KPIs</a> &nbsp;•&nbsp;
  <a href="#business-analysis">Analysis</a> &nbsp;•&nbsp;
  <a href="#sql-analysis">SQL</a> &nbsp;•&nbsp;
  <a href="#project-structure">Structure</a> &nbsp;•&nbsp;
</p>

</div>

---

## Table of Contents

<details>
<summary><strong>Click to expand</strong></summary>

* [Project Overview](#project-overview)
* [Project Objectives](#project-objectives)
* [Dashboard Preview](#dashboard-preview)
* [Key Performance Indicators](#key-performance-indicators)
* [Dashboard Pages](#dashboard-pages)
* [Business Analysis](#business-analysis)
* [Top 5 Pizza Analysis](#top-5-pizza-analysis)
* [Bottom 5 Pizza Analysis](#bottom-5-pizza-analysis)
* [SQL Analysis](#sql-analysis)
* [Technology Stack](#technology-stack)
* [Data Source](#data-source)
* [Project Structure](#project-structure)
* [How the Project Works](#how-the-project-works)
* [Project Requirements](#project-requirements)
* [Future Improvements](#future-improvements)
* [Project Files](#project-files)

</details>

---

<a name="project-overview"></a>

## Project Overview

The **Pizza Sales Report** is an interactive Business Intelligence project developed using **Microsoft Power BI**.

The purpose of the project is to transform pizza sales transaction data into a visual analytics solution that helps understand overall sales performance and product-level performance.

The dashboard focuses on:

* Revenue performance
* Average order value
* Total orders
* Total pizzas sold
* Average pizzas per order
* Daily order trends
* Monthly order trends
* Pizza category performance
* Pizza size performance
* Top-selling pizzas
* Lowest-performing pizzas

The project combines **Power BI, SQL, structured sales data, and GitHub version control** into a complete analytics workflow.

---

<a name="project-objectives"></a>

## Project Objectives

| Objective             | Description                                                    |
| --------------------- | -------------------------------------------------------------- |
| Revenue Analysis      | Measure total revenue generated from pizza sales               |
| Order Analysis        | Analyze total orders and average order value                   |
| Quantity Analysis     | Measure total pizzas sold and average pizzas per order         |
| Trend Analysis        | Analyze order patterns across days and months                  |
| Category Analysis     | Compare sales contribution across pizza categories             |
| Size Analysis         | Understand revenue contribution by pizza size                  |
| Product Analysis      | Identify high- and low-performing pizzas                       |
| Dashboard Development | Convert analytical results into an interactive Power BI report |
| SQL Validation        | Use SQL queries to calculate and validate business metrics     |
| Version Control       | Maintain the Power BI project using Git and GitHub             |

---

<a name="dashboard-preview"></a>

## Dashboard Preview

### Home Dashboard

The Home page provides a consolidated view of the main business KPIs and sales trends.

<div align="center">

<img src="./Pizza%20sales%20Report%20image/Home%20sales%20report.png" alt="Pizza Sales Home Dashboard" width="100%">

</div>

<br>

### Best / Worst Sellers Dashboard

The Best/Worst Sellers page focuses on product-level performance across revenue, quantity sold, and total orders.

<div align="center">

<img src="./Pizza%20sales%20Report%20image/BestWorst%20sales%20report.png" alt="Pizza Sales Best and Worst Sellers Dashboard" width="100%">

</div>

---

<a name="key-performance-indicators"></a>

## Key Performance Indicators

The dashboard contains five primary KPIs.

| KPI                      |       Value | Description                                   |
| ------------------------ | ----------: | --------------------------------------------- |
| Total Revenue            | **817.86K** | Total revenue generated from pizza sales      |
| Average Order Value      |   **38.31** | Average revenue generated per order           |
| Total Pizzas Sold        |  **49,574** | Total quantity of pizzas sold                 |
| Total Orders             |  **21,350** | Total number of orders                        |
| Average Pizzas Per Order |    **2.32** | Average number of pizzas included in an order |

### KPI Calculation Logic

```text
Total Revenue
    = SUM(total_price)

Average Order Value
    = Total Revenue / Total Orders

Total Pizzas Sold
    = SUM(quantity)

Total Orders
    = COUNT(DISTINCT order_id)

Average Pizzas Per Order
    = Total Pizzas Sold / Total Orders
```

---

<a name="dashboard-pages"></a>

## Dashboard Pages

### Page 1 — Home

The Home dashboard provides a high-level overview of business performance.

| Section           | Analysis                                                                                |
| ----------------- | --------------------------------------------------------------------------------------- |
| KPI Cards         | Revenue, Average Order Value, Total Pizzas Sold, Total Orders, Average Pizzas Per Order |
| Daily Trend       | Total orders by day of week                                                             |
| Monthly Trend     | Total orders by month                                                                   |
| Category Sales    | Revenue contribution by pizza category                                                  |
| Size Sales        | Revenue contribution by pizza size                                                      |
| Category Quantity | Total pizzas sold by category                                                           |
| Filters           | Pizza category and date filters                                                         |

### Page 2 — Best / Worst Sellers

The Best/Worst Sellers dashboard provides detailed product-level analysis.

| Section              | Analysis                                         |
| -------------------- | ------------------------------------------------ |
| Top 5 by Revenue     | Highest revenue-generating pizzas                |
| Top 5 by Quantity    | Highest quantity-selling pizzas                  |
| Top 5 by Orders      | Pizzas appearing in the highest number of orders |
| Bottom 5 by Revenue  | Lowest revenue-generating pizzas                 |
| Bottom 5 by Quantity | Lowest quantity-selling pizzas                   |
| Bottom 5 by Orders   | Pizzas appearing in the lowest number of orders  |

---

<a name="business-analysis"></a>

## Business Analysis

### Daily Order Trend

The project analyzes total orders across the days of the week.

| Day       | Total Orders |
| --------- | -----------: |
| Friday    |        3,538 |
| Thursday  |        3,239 |
| Saturday  |        3,158 |
| Wednesday |        3,024 |
| Tuesday   |        2,973 |
| Monday    |        2,794 |
| Sunday    |        2,624 |

This analysis helps identify differences in order activity across the week.

---

### Monthly Order Trend

The dashboard also analyzes order activity by month.

| Month     | Total Orders |
| --------- | -----------: |
| January   |        1,845 |
| February  |        1,685 |
| March     |        1,840 |
| April     |        1,799 |
| May       |        1,853 |
| June      |        1,773 |
| July      |        1,935 |
| August    |        1,841 |
| September |        1,661 |
| October   |        1,646 |
| November  |        1,792 |
| December  |        1,680 |

---

### Sales by Pizza Category

| Pizza Category |    Revenue | Contribution |
| -------------- | ---------: | -----------: |
| Classic        | 220,053.10 |       26.91% |
| Supreme        | 208,197.00 |       25.46% |
| Chicken        | 195,919.50 |       23.96% |
| Veggie         | 193,690.45 |       23.68% |

The category analysis measures each category's revenue contribution to overall pizza sales.

---

### Sales by Pizza Size

| Pizza Size |    Revenue | Contribution |
| ---------- | ---------: | -----------: |
| Large      | 375,318.70 |       45.89% |
| Medium     | 249,382.25 |       30.49% |
| Small      | 178,076.50 |       21.77% |
| X-Large    |  14,076.00 |        1.72% |
| XX-Large   |   1,006.60 |        0.12% |

The size analysis helps visualize how different pizza sizes contribute to total revenue.

---

### Total Pizzas Sold by Category

| Category | Pizzas Sold |
| -------- | ----------: |
| Classic  |      14,888 |
| Supreme  |      11,987 |
| Veggie   |      11,649 |
| Chicken  |      11,050 |

---

<a name="top-5-pizza-analysis"></a>

## Top 5 Pizza Analysis

### Top 5 by Revenue

| Rank | Pizza                        |   Revenue |
| ---: | ---------------------------- | --------: |
|    1 | The Thai Chicken Pizza       | 43,434.25 |
|    2 | The Barbecue Chicken Pizza   | 42,768.00 |
|    3 | The California Chicken Pizza | 41,409.50 |
|    4 | The Classic Deluxe Pizza     | 38,180.50 |
|    5 | The Spicy Italian Pizza      | 34,831.25 |

### Top 5 by Quantity

| Rank | Pizza                      | Quantity Sold |
| ---: | -------------------------- | ------------: |
|    1 | The Classic Deluxe Pizza   |         2,453 |
|    2 | The Barbecue Chicken Pizza |         2,432 |
|    3 | The Hawaiian Pizza         |         2,422 |
|    4 | The Pepperoni Pizza        |         2,418 |
|    5 | The Thai Chicken Pizza     |         2,371 |

### Top 5 by Total Orders

| Rank | Pizza                      | Total Orders |
| ---: | -------------------------- | -----------: |
|    1 | The Classic Deluxe Pizza   |        2,329 |
|    2 | The Hawaiian Pizza         |        2,280 |
|    3 | The Pepperoni Pizza        |        2,278 |
|    4 | The Barbecue Chicken Pizza |        2,273 |
|    5 | The Thai Chicken Pizza     |        2,225 |

---

<a name="bottom-5-pizza-analysis"></a>

## Bottom 5 Pizza Analysis

### Bottom 5 by Revenue

| Rank | Pizza                     |   Revenue |
| ---: | ------------------------- | --------: |
|    1 | The Brie Carre Pizza      | 11,589.99 |
|    2 | The Green Garden Pizza    | 13,955.75 |
|    3 | The Spinach Supreme Pizza | 15,277.75 |
|    4 | The Mediterranean Pizza   | 15,360.50 |
|    5 | The Spinach Pesto Pizza   | 15,596.00 |

### Bottom 5 by Quantity

| Rank | Pizza                     | Quantity Sold |
| ---: | ------------------------- | ------------: |
|    1 | The Brie Carre Pizza      |           490 |
|    2 | The Mediterranean Pizza   |           934 |
|    3 | The Calabrese Pizza       |           937 |
|    4 | The Spinach Supreme Pizza |           950 |
|    5 | The Soppressata Pizza     |           961 |

### Bottom 5 by Total Orders

| Rank | Pizza                     | Total Orders |
| ---: | ------------------------- | -----------: |
|    1 | The Brie Carre Pizza      |          480 |
|    2 | The Mediterranean Pizza   |          912 |
|    3 | The Spinach Supreme Pizza |          918 |
|    4 | The Calabrese Pizza       |          918 |
|    5 | The Chicken Pesto Pizza   |          938 |

---

<a name="sql-analysis"></a>

## SQL Analysis

SQL was used to calculate and validate the core analytical metrics used in the project.

### SQL Analysis Areas

```text
KPI Analysis
│
├── Total Revenue
├── Average Order Value
├── Total Pizzas Sold
├── Total Orders
└── Average Pizzas Per Order

Trend Analysis
│
├── Daily Order Trend
└── Monthly Order Trend

Sales Distribution
│
├── Sales by Pizza Category
└── Sales by Pizza Size

Product Performance
│
├── Top 5 by Revenue
├── Bottom 5 by Revenue
├── Top 5 by Quantity
├── Bottom 5 by Quantity
├── Top 5 by Total Orders
└── Bottom 5 by Total Orders
```

### Example SQL

#### Total Revenue

```sql
SELECT
    SUM(total_price) AS Total_Revenue
FROM pizza_sales;
```

#### Average Order Value

```sql
SELECT
    SUM(total_price) / COUNT(DISTINCT order_id) AS Avg_Order_Value
FROM pizza_sales;
```

#### Total Pizzas Sold

```sql
SELECT
    SUM(quantity) AS Total_Pizza_Sold
FROM pizza_sales;
```

#### Total Orders

```sql
SELECT
    COUNT(DISTINCT order_id) AS Total_Orders
FROM pizza_sales;
```

#### Average Pizzas Per Order

```sql
SELECT
    CAST(
        CAST(SUM(quantity) AS DECIMAL(10,2)) /
        CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2))
        AS DECIMAL(10,2)
    ) AS Avg_Pizzas_Per_Order
FROM pizza_sales;
```

For the complete SQL analysis, see:

<a href="./PIZZA%20SALES%20SQL%20QUERIES.docx">PIZZA SALES SQL QUERIES.docx</a>

---

<a name="technology-stack"></a>

## Technology Stack

| Technology                   | Purpose                                       |
| ---------------------------- | --------------------------------------------- |
| **Microsoft Power BI**       | Dashboard development and data visualization  |
| **Power BI Project (.pbip)** | Source-controlled Power BI development format |
| **SQL**                      | KPI calculation and analytical validation     |
| **CSV**                      | Sales transaction data                        |
| **Microsoft Excel**          | Data reference and analysis                   |
| **Git**                      | Version control                               |
| **GitHub**                   | Repository management and collaboration       |

---

<a name="data-source"></a>

## Data Source

The project uses a pizza sales transaction dataset.

### Main Dataset

<a href="./pizza_sales.csv">pizza_sales.csv</a>

### Excel Dataset

<a href="./pizza_sales_excel_file.xlsx">pizza_sales_excel_file.xlsx</a>

### Main Fields Used

```text
order_id
order_date
quantity
total_price
pizza_name
pizza_category
pizza_size
```

These fields support the KPI, trend, category, size, and product-level analysis included in the dashboard.

---

<a name="project-structure"></a>

## Project Structure

```text
Pizza-Sales-Report/
│
├── .gitignore
│
├── PIZZA SALES REPORT.pbip
├── PIZZA SALES REPORT.pbix
│
├── PIZZA SALES REPORT.Report/
│   │
│   ├── .platform
│   │
│   ├── definition/
│   │   ├── report.json
│   │   ├── pages.json
│   │   ├── version.json
│   │   │
│   │   └── pages/
│   │       ├── page definitions
│   │       └── visual definitions
│   │
│   └── StaticResources/
│       └── RegisteredResources/
│           ├── Dashboard Images
│           └── Base Theme
│
├── PIZZA SALES REPORT.SemanticModel/
│   │
│   ├── .platform
│   ├── definition.pbism
│   │
│   └── definition/
│       ├── database.tmdl
│       ├── model.tmdl
│       ├── relationships.tmdl
│       ├── cultures/
│       └── tables/
│
├── Pizza Sales Images/
│
├── Pizza sales Report image/
│   ├── Home sales report.png
│   └── BestWorst sales report.png
│
├── pizza_sales.csv
├── pizza_sales_excel_file.xlsx
├── PIZZA SALES SQL QUERIES.docx
└── PROBLEM STATEMENT.pdf
```

---

<a name="how-the-project-works"></a>

## How the Project Works

```text
                  Pizza Sales Data
                         │
                         ▼
                  Data Preparation
                         │
                         ▼
                   SQL Analysis
                         │
                         ▼
                  KPI Calculations
                         │
                         ▼
                  Power BI Dashboard
                         │
             ┌───────────┴───────────┐
             ▼                       ▼
        Home Dashboard       Best/Worst Sellers
             │                       │
             └───────────┬───────────┘
                         ▼
                  Business Analysis
```

---

<a name="usage"></a>


### 4. Explore the Dashboard

Navigate between:

```text
Home
Best/Worst Sellers
```

Use the available dashboard filters to explore the sales data.

---

<a name="collaboration"></a>


## Repository Status

<div align="center">

<table>
<tr>
<td align="center">

<strong>Power BI</strong><br>
Dashboard

</td>
<td align="center">

<strong>PBIP</strong><br>
Source Controlled

</td>
<td align="center">

<strong>SQL</strong><br>
Analysis

</td>
<td align="center">

<strong>GitHub</strong><br>
Version Control

</td>
</tr>
</table>

</div>

---

<a name="project-requirements"></a>

## Project Requirements

### KPI Requirements

| Requirement             |   Status  |
| ----------------------- | :-------: |
| Total Revenue           | Completed |
| Average Order Value     | Completed |
| Total Pizza Sold        | Completed |
| Total Orders            | Completed |
| Average Pizza Per Order | Completed |

### Visualization Requirements

| Visualization                         |   Status  |
| ------------------------------------- | :-------: |
| Daily Trend for Total Orders          | Completed |
| Monthly Trend for Total Orders        | Completed |
| Percentage of Sales by Pizza Category | Completed |
| Percentage of Sales by Pizza Size     | Completed |
| Total Pizzas Sold by Pizza Category   | Completed |
| Top 5 by Revenue                      | Completed |
| Top 5 by Quantity                     | Completed |
| Top 5 by Total Orders                 | Completed |
| Bottom 5 by Revenue                   | Completed |
| Bottom 5 by Quantity                  | Completed |
| Bottom 5 by Total Orders              | Completed |

---

<a name="project-files"></a>

## Project Files

| File / Folder                                                                          | Purpose                                       |
| -------------------------------------------------------------------------------------- | --------------------------------------------- |
| <a href="./PIZZA%20SALES%20REPORT.pbip">PIZZA SALES REPORT.pbip</a>                    | Main Power BI project entry point             |
| <a href="./PIZZA%20SALES%20REPORT.pbix">PIZZA SALES REPORT.pbix</a>                    | Power BI report file                          |
| <a href="./PIZZA%20SALES%20REPORT.Report/">PIZZA SALES REPORT.Report</a>               | Report definition and visuals                 |
| <a href="./PIZZA%20SALES%20REPORT.SemanticModel/">PIZZA SALES REPORT.SemanticModel</a> | Semantic model definition                     |
| <a href="./pizza_sales.csv">pizza_sales.csv</a>                                        | Main sales dataset                            |
| <a href="./pizza_sales_excel_file.xlsx">pizza_sales_excel_file.xlsx</a>                | Excel version of sales data                   |
| <a href="./PIZZA%20SALES%20SQL%20QUERIES.docx">PIZZA SALES SQL QUERIES.docx</a>        | SQL queries and analysis                      |
| <a href="./PROBLEM%20STATEMENT.pdf">PROBLEM STATEMENT.pdf</a>                          | Project requirements                          |
| <a href="./Pizza%20Sales%20Images/">Pizza Sales Images</a>                             | Project image resources                       |
| <a href="./Pizza%20sales%20Report%20image/">Pizza sales Report image</a>               | Dashboard screenshots                         |
| `.gitignore`                                                                           | Git ignored files and local Power BI settings |

---

<a name="future-improvements"></a>

## Future Improvements

Potential extensions for the project include:

* Automated data refresh
* Power BI Service deployment
* Sales forecasting
* Profit and margin analysis
* Geographic sales analysis
* Customer segmentation
* Product-level drill-through pages
* Additional time-intelligence analysis
* Automated reporting
* Advanced sales trend analysis

---

## Project Documentation

The following project documentation is included in the repository:

* <a href="./PROBLEM%20STATEMENT.pdf">Project Problem Statement</a>
* <a href="./PIZZA%20SALES%20SQL%20QUERIES.docx">SQL Query Documentation</a>
* <a href="./pizza_sales.csv">CSV Dataset</a>
* <a href="./pizza_sales_excel_file.xlsx">Excel Dataset</a>
* <a href="./PIZZA%20SALES%20REPORT.pbip">Power BI Project</a>

---

<div align="center">

### Pizza Sales Report

**From transactional sales data to interactive business intelligence.**

</div>
