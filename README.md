# Nashville Housing Data Cleaning & Visualization Project

## Project Overview

This project analyzes housing sales in Nashville, Tennessee using SQL and Tableau. The project demonstrates an end-to-end analytics workflow, including data cleaning, transformation, exploratory analysis, and dashboard development.

Housing transaction data was cleaned and transformed in SQL before being visualized in an interactive Tableau dashboard to identify pricing trends, geographic patterns, and property characteristics associated with residential sale prices.

---

## Tools Used

- SQL
- Tableau
- Exploratory Data Analysis (EDA)
- Data Cleaning & Transformation
- Data Visualization

---

## Executive Summary

This project examines residential housing sales in Nashville to identify factors that influence property sale prices and evaluate how housing prices changed over time.

The dataset initially contained 56,478 records and required cleaning to address missing values, inconsistent address formatting, and duplicate records. After cleaning, the final dataset contained 56,374 records.

The analysis found that housing prices generally increased between 2013 and 2016, location played a significant role in pricing, property characteristics influenced sale values, and vacant properties tended to sell for lower prices than occupied properties.

An interactive Tableau dashboard was developed to allow users to explore housing trends through filters, maps, KPIs, and comparative visualizations.

---

## Business Problem & Objective

### Business Problem

Real estate professionals, investors, and property developers need to understand the factors that influence residential property values in order to make informed purchasing, pricing, and investment decisions.

### Business Question

**What factors influence residential sale prices in Nashville, and how has pricing changed over time?**

### Project Objectives

- Clean and prepare housing transaction data for analysis
- Identify trends in housing prices over time
- Evaluate the impact of location on sale prices
- Analyze relationships between property characteristics and property values
- Develop an interactive dashboard to communicate findings

---

## Dataset Overview

The Nashville Housing dataset contains residential property transaction records and property characteristics dated between 2013 and 2020. However, most records occur between 2013 and 2016, which serves as the primary period analyzed in this project.

### Dataset Summary

| Metric | Count |
|----------|----------|
| Original Records | 56,478 |
| Cleaned Records | 56,374 |
| Duplicate Records Removed | 104 |

### Dataset Structure 

| Column | Data Type |
|----------|----------|
| UniqueID | INTEGER |
| ParcelID | STRING |
| LandUse | STRING |
| PropertyAddress | STRING |
| SaleDate | DATE |
| SalePrice | INTEGER |
| LegalReference | STRING |
| SoldAsVacant | BOOLEAN |
| OwnerName | STRING |
| OwnerAddress | STRING |
| Acreage | FLOAT |
| TaxDistrict | STRING |
| LandValue | INTEGER |
| BuildingValue | INTEGER |
| TotalValue | INTEGER |
| YearBuilt | INTEGER |
| Bedrooms | INTEGER |
| FullBath | INTEGER |
| HalfBath | INTEGER |

### Columns Created During Data Cleaning

| Column | Purpose |
|----------|----------|
| PropertySplitAddress | Extracted street address from PropertyAddress |
| PropertySplitCity | Extracted city from PropertyAddress |
| OwnerSplitAddress | Extracted street address from OwnerAddress |
| OwnerSplitCity | Extracted city from OwnerAddress |
| OwnerSplitState | Extracted state from OwnerAddress |
| sold_as_vacant_status | Converted Boolean values into Yes/No categories |
| row_num | Used to identify duplicate records |

---

## Analytical Process

### Data Cleaning

#### 1. Missing Value Treatment
- Identified records with missing property addresses
- Populated missing values using matching Parcel IDs

#### 2. Address Standardization
Split PropertyAddress into:
- PropertySplitAddress
- PropertySplitCity

Split OwnerAddress into:
- OwnerSplitAddress
- OwnerSplitCity
- OwnerSplitState

#### 3. Data Standardization
Converted SoldAsVacant Boolean values into user-friendly Yes/No categories.

#### 4. Duplicate Removal
Used ROW_NUMBER() and a deduplicated SQL view to identify and remove duplicate records.

### SQL Techniques Demonstrated

- JOINs
- CASE Statements
- Window Functions (ROW_NUMBER)
- Common Table Expressions (CTEs)
- Aggregate Functions
- GROUP BY and HAVING Clauses
- String Manipulation
- Missing Value Imputation
- Data Deduplication

---

## Tableau Dashboard

**Interactive Dashboard:**

 [View Interactive Tableau Dashboard](https://public.tableau.com/shared/TM2JKMBP3?:display_count=n&:origin=viz_share_link)

### Dashboard Preview

Nashville Residential Housing Dashboard <img width="1696" height="794" alt="Tableau_Nashville_Residential_Housing_Dashboard" src="https://github.com/user-attachments/assets/031c1891-d572-4881-b59a-dbaed2a4cf7d" />

### Dashboard Feature

#### KPI Cards
- Average Sale Price
- Total Homes Sold
- Average Bedrooms
- Total Property Value

#### Interactive Filters
- Sale Year
- Land Use
- City

#### Visualizations
- Average Sales by Month
- Homes Sold by City Map
- Bedrooms vs Average Sale Price
- Sale Price vs Total Value Scatter Plot
- Sale Price Distribution Histogram
- Average Sale Price by Land Use
- Sold-As-Vacant Comparison

---

## Insight Deep Dive

### Pricing Trends Over Time

Average residential sale prices showed a generally upward trend between 2013 and 2016, indicating continued growth in the Nashville housing market.

### Geographic Trends

Housing activity and average sale prices varied across cities, with some locations consistently generating higher sales volumes and property values.

### Property Characteristics

Properties with more bedrooms generally achieved higher sale prices, although the relationship was not perfectly linear.

### Land Use Analysis

Different land-use classifications exhibited substantial differences in average sale prices and total property values.

### Vacancy Analysis

Properties sold as vacant generally had lower average sale prices than non-vacant properties.

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
## Business Recommendations

Based on the analysis, the following recommendations could help real estate professionals, investors, and property developers make more informed decisions:

### 1. Focus Investment in High-Value Markets
Cities with consistently higher average sale prices may present stronger opportunities for investment and development. Real estate firms should prioritize these areas when evaluating future projects.

### 2. Monitor Pricing Trends Over Time
The upward trend in housing prices suggests a growing market. Investors and developers should regularly monitor pricing trends to identify favorable buying and selling periods.

### 3. Consider Property Characteristics in Valuation
The analysis shows that property characteristics, such as the number of bedrooms, influence sale price. Property improvements that increase livable space may help maximize property value.

### 4. Evaluate Land Use Before Acquisition
Different land-use classifications show significant differences in average sale prices and total property values. Understanding land-use patterns can support more effective investment decisions.

### 5. Review Vacant Property Opportunities
Properties sold as vacant generally had lower average sale prices than occupied properties. Investors may find opportunities to purchase vacant properties at lower costs and increase value through renovation or redevelopment.

### 6. Use Geographic Trends to Guide Marketing Strategies
Areas with higher sales volume may benefit from targeted marketing campaigns, while lower-volume areas may require different sales strategies to attract buyers.

---

## Repository Contents

- `Nashville_Housing_Data_Raw.csv` — Original Nashville housing dataset prior to cleaning and transformation.
- `Nashville_Housing_Data_Cleaned.csv` — Cleaned dataset after addressing missing values, standardizing fields, and removing duplicate records.
- `Nashville_Housing_SQL.sql` — SQL queries used for data cleaning, transformation, and exploratory analysis in Google BigQuery.
- `Tableau_Screenshot_Dashboard.png` — Preview image of the interactive Tableau dashboard.

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
