# Pharmaceutical-Sales-Dashboard-Power-BI
# Pharmaceutical Sales Dashboard (Power BI)

## Overview
This project is an interactive **Power BI dashboard** for analyzing pharmaceutical sales data over the years, across clusters, products, sales representatives, and branches.  
The tool is used to track performance, compare sales against targets, calculate YoY%, and includes advanced **Drill-through** and **Tooltips** for easy data exploration.

## 🔥 Key Features

## Data Cleaning & Transformation
Before building the dashboard, a complete data cleaning process was performed using Power Query:

- Removed duplicate records.
- Handled missing and null values.
- Standardized column names and data types.
- Corrected inconsistent data entries.
- Validated relationships between fact and dimension tables.
- Optimized data structure for better performance and reporting accuracy.


### Dashboard Pages

**Overview**  
Provides a summary of the main KPIs:

- **Total Sales**  
- **Total Quantity**  
- **Total Target**  
- **Achievement %**  
- **YoY %**

**Cluster & Rep Analysis**  
Analysis includes:

- Sales by Rep  
- Sales by Cluster  
- Year-over-Year performance comparison  
- Treemap & Pie charts for sales distribution  

**Products Analysis**  

- Top 10 products  
- Average annual price  
- Sales & Quantity by product  
- Stacked bar + trend line visualizations  

**Scenario Pages (1–4)**  

- Annual performance comparison  
- Sales change YoY  
- Quantity distribution  
- Seasonal analysis  

**Cluster Drillthrough**  
Detailed page showing:

- Sales by product within each cluster  
- Target vs. Amount comparison  

**Rep Drillthrough**  
Sales analysis per Rep over the years, including products.

## 🧱 Data Model
The data model was redesigned and optimized following a Star Schema approach:

### Dimension Tables
- D_Cluster  
- D_Group  
- D_Rep  
- Date Table (Custom Calendar)  

### Fact Tables
- F_Actuals  
- F_Actuals (2)  
- F_Targets  

### Relationships
One-to-Many relationships between:

- Date Table → F_Actuals  
- D_Rep → F_Actuals  
- D_Cluster → F_Actuals  
- D_Group → F_Actuals  

Relationships include **cross-filtering** to enable Drillthrough and filter propagation.

## 📈 KPIs Used
- Total Sales  
- Total Quantity  
- Total Targets  
- **Achievement %** = Amount ÷ Target  
- **YoY%** (Year-over-Year Change)  
- Average Price  

