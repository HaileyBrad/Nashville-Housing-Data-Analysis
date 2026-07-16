# Nashville Housing Data Cleaning & Visualization Project

## Project Overview

This project analyzes residential housing sales in Nashville, Tennessee using SQL and Tableau. The dataset was cleaned and transformed in Google BigQuery before being visualized in an interactive Tableau dashboard.

### Business Question

**What factors influence residential sale prices in Nashville, and how has pricing changed over time?**

To answer this question, I cleaned housing transaction data, explored pricing trends, analyzed property characteristics, and built an interactive dashboard to identify patterns in residential property sales.

---

## Tools Used

- Google BigQuery (SQL)
- Tableau Public
- Data Cleaning & Transformation
- Data Visualization

---

## Tableau Dashboard

**Interactive Dashboard:**

https://public.tableau.com/shared/TM2JKMBP3?:display_count=n&:origin=viz_share_link

### Dashboard Preview

![Nashville Housing Dashboard] <img width="1696" height="794" alt="Tableau_Nashville_Residential_Housing_Dashboard" src="https://github.com/user-attachments/assets/031c1891-d572-4881-b59a-dbaed2a4cf7d" />


---

## Data Cleaning Process

The raw housing dataset contained missing values, inconsistent formatting, and duplicate records. SQL was used to prepare the data for analysis.

### Cleaning Tasks Completed

#### 1. Populated Missing Property Addresses
- Identified records with missing property addresses
- Used matching Parcel IDs to populate missing address values

#### 2. Split Address Fields
Created separate columns for:

**Property Address**
- Street Address
- City

**Owner Address**
- Street Address
- City
- State

#### 3. Standardized Sold-As-Vacant Values
Converted boolean values into user-friendly categories:
- Yes
- No

#### 4. Removed Duplicate Records
Used:

```sql
ROW_NUMBER()
PARTITION BY
```

to identify and remove duplicate transactions while preserving unique records.

---

## SQL Analysis Performed

### Pricing Trends Over Time
- Average sale price by year
- Number of home sales by year

### Geographic Analysis
- Average sale price by city
- Total homes sold by city

### Property Characteristics
- Bedrooms vs. average sale price
- Land use vs. average sale price
- Total property value vs. sale price

### Vacancy Analysis
- Comparison of sale prices for vacant and non-vacant properties

### Ownership Analysis
- Identification of top property owners
- Average sale price by owner

---

## Dashboard Features

The Tableau dashboard includes:

### KPI Metrics
- Average Sale Price
- Total Homes Sold
- Average Bedrooms
- Total Property Value

### Interactive Filters
- Sale Year
- Land Use
- City

### Visualizations
- Average Sales by Month
- Homes Sold by City Map
- Bedrooms vs. Average Sale Price
- Sale Price vs. Total Value Scatter Plot
- Sale Price Distribution Histogram
- Average Sale Price by Land Use
- Sold-As-Vacant Comparison

---

## Key Insights

### Home Prices Increased Over Time
Average residential sale prices generally trended upward between 2013 and 2016.

### Location Influences Sale Price
Certain cities and neighborhoods consistently showed higher average sale prices and greater sales activity.

### Property Characteristics Matter
Properties with more bedrooms generally sold for higher prices, although the relationship was not perfectly linear.

### Land Use Impacts Property Value
Different land-use classifications exhibited notable differences in average sale prices and total property values.

### Vacant Properties Sold for Less
Properties sold as vacant generally had lower average sale prices than non-vacant properties.

---

## Repository Contents

- `Nashville_Housing_Cleaning.sql` — SQL data cleaning and analysis queries
- `dashboard_screenshot.png` — Dashboard preview image
- `README.md` — Project documentation

---

## Skills Demonstrated

- SQL Data Cleaning
- Data Transformation
- Data Quality Validation
- Window Functions
- Data Analysis
- Tableau Dashboard Development
- Data Storytelling
- Business Intelligence Reporting
