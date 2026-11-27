# Nassau Candy Distributor – Factory-to-Customer Shipping Route Efficiency Analysis

An end-to-end data analytics portfolio project focused on analyzing sales performance, factory distribution, geographic demand, shipping modes, factory-to-customer combinations, and estimated distance patterns using Microsoft Excel.

---

## Project Overview

This project analyzes the sales and distribution data of Nassau Candy Distributor to understand how business performance varies across factories, products, customers, geographical locations, and shipping modes.

The main objective is to transform raw transaction data into meaningful business information through data preparation, data modelling, analytical calculations, PivotTables, PivotCharts, and an interactive Excel dashboard.

The project also identifies important business patterns, highlights data-quality concerns, and presents evidence-based recommendations to support further investigation and business planning.

Rather than focusing only on sales reporting, this project connects sales performance with factory distribution and customer geography to provide a broader view of the distributor's recorded business activity.

## Business Problem

A distributor needs a clear understanding of its sales performance and distribution network.

Without structured analysis, it can be difficult to answer questions such as:

- Which factories contribute the most to total sales and gross profit?
- Which products and divisions generate the highest sales?
- Which geographical regions, states, and cities contribute most to business activity?
- Which shipping modes are most frequently used?
- Which factory-to-customer combinations have the highest order volume and sales?
- How are sales and orders distributed across different periods?
- What data-quality issues should be investigated before making operational decisions?

This project addresses these questions by organizing the available data into a structured analytical model and developing a dashboard for business reporting.

## Project Objectives

1. Understand and inspect the available datasets.
2. Clean and prepare the data using Power Query.
3. Organize the datasets into a relational Data Model.
4. Validate primary keys, foreign keys, relationships, and data types.
5. Develop business KPIs using Power Pivot and DAX.
6. Analyze factory, product, customer, geographic, shipping, and route-combination performance.
7. Explore estimated geographic distance patterns.
8. Build an interactive Excel dashboard using PivotTables and PivotCharts.
9. Identify meaningful business insights.
10. Prepare practical recommendations supported by the available data.

## Dataset Overview

The project uses six related datasets organized into one fact table and five dimension tables.

| Dataset | Rows | Columns | Purpose |
|---|---:|---:|---|
| FactSales | 10,194 | 13 | Transaction-level sales records |
| DimCustomer | 5,044 | 2 | Customer reference information |
| DimDate | 2,370 | 9 | Calendar and date attributes |
| DimFactory | 5 | 2 | Factory reference information |
| DimGeography | 655 | 6 | Customer geographical information |
| DimProduct | 15 | 4 | Product and division information |
| **Total** | **18,283** | **36** | **Six source datasets** |

The FactSales table contains transaction-line records. One order may contain multiple transaction rows, so transaction count and distinct order count are treated as different measures.

### Fact Table

**FactSales**

Contains measurable transaction information and foreign keys connecting the fact records to the dimension tables.

Important fields include:

- Row ID
- Order ID
- OrderDateKey
- ShipDateKey
- CustomerKey
- GeographyKey
- ProductKey
- FactoryKey
- Ship Mode
- Sales
- Units
- Gross Profit
- Cost

### Dimension Tables

**DimCustomer**
- CustomerKey
- Customer ID

**DimDate**
- DateKey
- Date
- Day
- Month
- Month Name
- Quarter
- Year
- Week Number
- Day Name

**DimFactory**
- FactoryKey
- Factory

**DimGeography**
- GeographyKey
- Country/Region
- State/Province
- City
- Postal Code
- Region

**DimProduct**
- ProductKey
- Product ID
- Product Name
- Division

## Tools and Technologies

| Tool | Application |
|---|---|
| Microsoft Excel 365 | Data analysis and dashboard development |
| Power Query | Data cleaning and transformation |
| Excel Data Model | Relational data modelling |
| Power Pivot | Data Model management and calculations |
| DAX | KPI and business measure development |
| PivotTables | Data summarization and analysis |
| PivotCharts | Visual analysis and comparisons |
| Excel Dashboard | Business reporting and visualization |
| GitHub | Project version control and portfolio presentation |

## Project Methodology

The project follows a structured data analytics workflow.

### 1. Data Understanding and Inspection

- Examined the six source datasets.
- Reviewed the number of rows and columns.
- Identified the fact table and dimension tables.
- Understood the transaction-level grain.
- Reviewed the available fields and their business meaning.

### 2. Data Cleaning and Transformation

Used Power Query to prepare the datasets for analysis.

Key activities included:

- Checking column names and data types.
- Inspecting missing values and duplicate records.
- Validating identifiers and key columns.
- Standardizing data where required.
- Preparing cleaned fact and dimension tables.
- Creating additional analytical fields where appropriate.

### 3. Data Modelling

Organized the datasets into a relational model using FactSales as the central fact table and five dimension tables.

The model supports analysis across:

- Customers
- Dates
- Factories
- Geography
- Products

Relationships were established using the corresponding primary and foreign keys.

### 4. KPI Development

Created DAX measures for important business metrics, including:

- Total Sales
- Total Gross Profit
- Total Cost
- Total Units
- Distinct Orders
- Distinct Customers
- Average Order Value
- Revenue per Unit
- Gross Profit Margin
- Unique Routes
- Active Factories
- Distinct Customer Cities

Measures were designed to support analysis under different filters and categories.

### 5. Exploratory Data Analysis

Analyzed the data across multiple business dimensions to identify patterns, concentration, differences, and potential areas for further investigation.

### 6. Dashboard Development

Developed a structured Excel dashboard using PivotTables, PivotCharts, KPI summaries, and visual comparisons.

### 7. Business Insights and Recommendations

Prepared separate business insights and business recommendations reports to communicate the findings, potential actions, monitoring requirements, and analytical limitations.

## Dashboard Overview

The final Excel dashboard is organized into the following analytical sections.

### 1. Network Overview

Provides a high-level summary of the distribution network.

Key indicators include:

- Total Sales
- Distinct Orders
- Unique Routes
- Active Factories
- Customer Cities

### 2. Route Performance Analysis

Examines factory-to-customer geographical combinations.

Visualizations include:

- Top 10 Factory-to-Customer Combinations by Distinct Orders
- Top 10 Factory-to-Customer Combinations by Sales

The analysis identifies combinations with high recorded sales and order activity.

### 3. Factory Distribution Analysis

Compares the contribution of individual factories.

Visualizations include:

- Factory-wise Distinct Orders
- Factory-wise Sales

This section helps identify factories with higher recorded business contribution.

### 4. Geographic Distribution Analysis

Examines sales and order distribution across customer locations.

Visualizations include:

- Top 10 States by Sales
- Top 10 Customer Cities by Distinct Orders

This analysis helps identify geographical areas with higher recorded business activity.

### 5. Shipping Mode Analysis

Compares the distribution of sales and orders across the four shipping modes.

Shipping modes covered:

- Standard Class
- Second Class
- First Class
- Same Day

Visualizations include:

- Shipping Mode-wise Distinct Orders
- Shipping Mode-wise Sales

### 6. Route Efficiency and Distance Analysis

Explores estimated geographical distance patterns and their relationship with distribution categories.

The analysis includes:

- Sales by Distance Band
- Average Estimated Distance by Region
- Average Estimated Distance by Shipping Mode
- Estimated Distance by Factory

**Important:** These distance calculations should be interpreted as estimates based on the available geographical inputs, not verified road distances or actual shipment journeys.

## Key Business Insights

The following observations are based on the workbook's reported analytical results and should be revalidated after any data refresh or change in calculations.

### Factory Performance

- Lot's O' Nuts is the leading factory by recorded sales and gross profit.
- Wicked Choccy's is another major contributor.
- The two leading factories account for a substantial share of recorded sales.
- The Other Factory shows a comparatively low gross profit margin and may deserve further investigation.

### Product Performance

- Recorded sales are concentrated among a small number of products.
- The top five products contribute approximately 92.88% of sales in the project study benchmark.
- Product availability and product-level profitability are useful areas for further investigation.

### Geographic Performance

- The Pacific and Atlantic regions together contribute approximately 61.72% of recorded sales in the project study benchmark.
- California and New York are among the leading states by sales.
- New York City and Los Angeles are among the leading customer cities by order activity.

### Shipping Mode Performance

- Standard Class is the dominant recorded shipping mode.
- Second Class and First Class also contribute to recorded shipping activity.
- Same Day has comparatively lower recorded usage.

This distribution describes usage patterns; it does not establish which mode is faster, cheaper, or more efficient.

### Route Performance

- The analysis identifies factory-to-city combinations with comparatively high sales and order activity.
- Lot's O' Nuts to New York City is a leading combination in the project study benchmark.
- High-volume combinations can be prioritized for more detailed distribution analysis.

These are factory-to-customer combinations, not verified physical road routes.

## Business Recommendations

The analysis suggests several areas for management review.

### 1. Review Factory Concentration

Monitor the contribution of the leading factories and evaluate production capacity, inventory availability, and contingency planning before changing factory allocations.

### 2. Monitor Product Concentration

Track the leading products and investigate inventory availability, product-level margins, demand patterns, and replenishment requirements.

### 3. Review Regional Demand

Use state-wise and city-wise sales patterns to support regional demand planning. Additional inventory and operational information is required before making distribution changes.

### 4. Investigate High-Volume Factory-to-City Combinations

Prioritize combinations with high recorded order activity for further investigation using actual distances, transport costs, carrier information, and delivery performance.

### 5. Evaluate Shipping Modes

Investigate the reasons behind the dominance of Standard Class. Compare actual delivery times, service levels, and transportation costs before recommending changes.

### 6. Improve Data Quality

Validate the unusual relationship between recorded order dates and ship dates before using calculated lead time in operational reporting.

## Important Data Limitations

Responsible interpretation is an important part of this project.

### 1. Order Date and Ship Date Anomaly

The workbook reports Order Dates from 2 January 2024 to 31 December 2025, while Ship Dates range from 30 June 2026 to 28 June 2030.

This produces exceptionally large calculated lead-time values.

Therefore, calculated lead time is treated as a provisional data-quality finding, not verified delivery performance. The original date values and date-key mapping require validation.

### 2. No Verified Physical Route Information

The available data does not provide verified road paths, GPS coordinates for actual journeys, carrier routes, or confirmed transport distances.

Therefore, this project does not claim to have optimized physical transportation routes.

### 3. No Confirmed Shipping Cost Data

The Cost field should not automatically be interpreted as freight or transportation cost. Its business definition must be confirmed before using it for cost-to-serve analysis.

Similarly, Gross Profit should not be described as net profit.

### 4. Limited Operational Data

The available datasets do not provide verified information about:

- Actual delivery timestamps
- Promised delivery dates
- Carrier performance
- Freight charges
- Vehicle capacity
- Shipment weight and volume
- Warehouse capacity
- Failed delivery attempts

Consequently, on-time delivery rates, cost per kilometre, vehicle utilization, and physical route optimization cannot be established from the current data.

### 5. Distinct Order Aggregation

The fact table contains multiple transaction lines per order. Distinct order counts grouped by different categories may overlap when an order contains multiple values of a category.

Grouped order totals should therefore be interpreted carefully.

## Project Deliverables

The repository contains the project workbook, documentation, dashboard screenshots, and supporting reports.

| Deliverable | Description |
|---|---|
| Excel Analysis Workbook | Data preparation, calculations, analysis, PivotTables and dashboard |
| Excel Documentation PDF | Detailed project workflow and learning documentation |
| Dashboard Images | Screenshots of the completed dashboard and analytical sections |
| Business Insights PDF | Key analytical observations and findings |
| Business Recommendations PDF | Suggested actions, priorities and monitoring considerations |
| README.md | Project overview, methodology, findings and limitations |
| LICENSE | Repository licensing information |

## Repository Structure

```text
shipping-route-efficiency-analysis/
│
├── images/
│   └── Dashboard and analysis screenshots
│
├── reports/
│   ├── README.md
│   ├── Nassau_Candy_Business_Insights.pdf
│   └── Nassau_Candy_Business_Recommendations.pdf
│
├── Documentation_Excel.pdf
│
├── Nassau_Candy_Shipping_Route_Analysis.xlsx
│
├── LICENSE
│
└── README.md
```

The exact workbook filename may differ slightly from the example above. The repository's actual uploaded filename should be used.

## How to Explore the Project

1. Start by reading this README to understand the business problem and project scope.
2. Open the Excel workbook to explore the prepared datasets and analytical worksheets.
3. Review the KPI calculations and supporting PivotTables.
4. Explore the FinalDashboard worksheet to understand the visual analysis.
5. Open the Business Insights PDF to review the findings.
6. Open the Business Recommendations PDF to understand the proposed next steps.
7. Refer to the Excel documentation PDF for a detailed explanation of the analytical workflow.

## Future Scope

The project can be extended with additional verified operational data.

Potential improvements include:

- Integrating actual shipment and delivery timestamps.
- Adding verified road distances and route information.
- Incorporating carrier and transportation costs.
- Comparing planned and actual delivery performance.
- Developing cost-per-shipment and cost-per-distance metrics.
- Evaluating factory capacity and inventory availability.
- Building predictive demand and replenishment models.
- Developing a more detailed logistics performance dashboard.

These improvements would make it possible to move from descriptive distribution analysis towards a more complete logistics performance study.

## Conclusion

This project demonstrates an end-to-end Excel-based data analytics workflow, starting with raw datasets and progressing through data preparation, relational modelling, KPI development, exploratory analysis, dashboard creation, and business reporting.

It provides a structured understanding of sales contribution, factory distribution, customer geography, shipping mode usage, and factory-to-customer activity.

An important outcome of the project is the identification of data limitations that must be resolved before making operational logistics decisions.

The project demonstrates not only the ability to analyze data and build dashboards, but also the importance of validating results, interpreting findings responsibly, and translating analytical observations into practical business recommendations.

---

**Project Category:** Data Analytics | Business Analysis | Distribution Network Analysis

**Primary Tool:** Microsoft Excel 

**Author:** Ravindra Pal

**GitHub Repository:** [Nassau Candy Shipping Route Efficiency Analysis](https://github.com/ravindrapal001/shipping-route-efficiency-analysis)
