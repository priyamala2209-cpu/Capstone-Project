# E-Commerce Sales Analysis using Microsoft Excel

## Project Overview

This project presents an end-to-end **E-Commerce Sales Data Analysis conducted using Microsoft Excel**. The objective was to clean, transform, and analyze raw sales data to derive actionable business insights. Using descriptive statistics, Pivot Tables, charts, and an interactive dashboard, the analysis focused on customer behavior, sales performance, product trends, payment methods, and store-level profitability to support data-driven decision making.

The complete workflow includes the following stages:

* **Data Cleaning:** Handled missing values, duplicates, and inconsistencies to ensure data integrity
* **Data Transformation:** Structured and formatted raw data for analysis using formulas and Excel functions
* **Descriptive Statistics:** Summarized key metrics including revenue, profit, and sales volume
* **Pivot Table Analysis:** Aggregated and cross-tabulated data to uncover trends across regions, categories, and time
* **Data Visualization:** Created charts and graphs to represent insights clearly and intuitively
* **Interactive Dashboard** Creation: Built a dynamic dashboard with slicers and KPIs for decision-making

This project was developed as a hands-on learning experience to strengthen practical knowledge in **Microsoft Excel for data analysis** and business intelligence.

---

## Project Objectives

This project aims to transform raw e-commerce data into strategic business insights using Microsoft Excel. 

**The core goals are:**

* **Ensure Data Quality:** Clean, standardize, and validate raw datasets by handling missing values, removing duplicates, and fixing inconsistencies
* **Uncover Business Drivers:** Analyze sales performance, product trends, customer behavior, and store metrics using pivot tables and descriptive statistics
* **Visualize for Decisions:** Build dynamic charts and graphs that highlight key patterns and performance indicators
* **Enable Self-Service Reporting:** Design an interactive Excel dashboard with slicers and KPIs for real-time business monitoring

---

## Dataset Description

This project utilizes multiple structured datasets representing key dimensions of an e-commerce business. The datasets were integrated to enable comprehensive analysis across customers, products, transactions, and stores.

### 1. Customer Dataset

Contains demographic and profile information for all registered customers.

**Key attributes include:**

* **Customer ID:** Unique identifier for each customer
* **Name: First:** Name, Last Name
* **Demographics:** Age, Gender
* **Location:** City, State, Country
* **Loyalty Level:** Customer tier based on purchase history and engagement

---

### 2. Product Dataset

This dataset forms the product master table for the analysis. It contains 7 key attributes used to evaluate product performance, profitability, and inventory health:

* **Product ID:** Unique identifier for each SKU
* **Product Name:** Descriptive title of the item
* **Category / Sub Category:** Hierarchical classification for trend analysis
* **Brand:** Manufacturer or label, used for brand performance comparison
* **Cost:** Unit procurement cost, critical for margin calculations
* **Stock:** Current inventory level, used to flag stockouts and overstock

---

### 3. Store Dataset

Contains store-level information used to analyze sales performance by location and format. 

**Key attributes include:**

* **Store ID:** Unique identifier for each retail outlet
* **Store Name:** Official name of the store
* **Region:** Geographic region where the store operates
* **City:** City in which the store is located
* **Store Type:** Format classification such as Flagship, Mall Outlet, or Online

---

### 4. Sales Dataset

Contains transactional records capturing all sales activity across stores and products. This dataset serves as the fact table for revenue, profit, and performance analysis. 

**Key attributes include:**

* **Sales ID:** Unique identifier for each transaction
* **Order Date:** Date when the order was placed
* **Customer ID:** Foreign key linking to the Customer Dataset
* **Product ID:** Foreign key linking to the Product Dataset
* **Store ID:** Foreign key linking to the Store Dataset
* **Quantity:** Number of units sold in the transaction
* **Unit Price:** Selling price per unit before discount
* **Discount:** Discount applied to the transaction
* **Payment Type:** Mode of payment used such as Credit Card, UPI, Cash
* **Total Amount:** Final billed amount after discount

These datasets were cleaned and transformed to resolve inconsistencies, handle missing values, and standardize formats, ensuring data integrity and readiness for analysis.

---

## Data Cleaning and Transformation

The following data cleaning and preprocessing techniques were applied to ensure data accuracy and consistency:

### Handling Missing Values

Missing values were identified and treated using appropriate methods to preserve dataset integrity and analytical accuracy.

**Tasks Performed:**

* **Identification:** Detected blank and null values across all datasets using filters and conditional formatting
* **Imputation:** Replaced missing values with suitable methods such as mode for categorical fields and median for numerical fields
* **Loyalty Level Correction:** Populated missing loyalty levels based on customer purchase history and engagement metrics
* **Data Validation:** Reviewed and flagged incomplete records to prevent skewing of analysis results

---

### Removing Duplicate Records

Duplicate entries were identified and eliminated to maintain data accuracy and prevent inflated metrics during analysis.

**Tasks Performed:**

* **Detection:** Scanned all datasets for duplicate rows using Customer ID, Sales ID, and composite keys
* **Deletion:** Removed exact duplicate transactions and customer records while retaining the first occurrence
* **Integrity Check:** Verified that removal of duplicates did not compromise relationships across Customer, Store, and Sales tables
* **Result:** Ensured each record represented a unique entity, improving reliability of aggregations and KPIs
---

### Data Standardization

Inconsistencies in data formatting were identified and corrected to ensure uniformity across all datasets, enabling accurate grouping and filtering.

**Tasks Performed:**

* **Text Formatting:** Standardized capitalization and casing for fields like City, State, Store Type, and Payment Type
* **Whitespace Correction:** Removed leading, trailing, and extra spaces using TRIM to prevent mismatched categories
* **Find and Replace:** Resolved naming inconsistencies in City, Store Type, and Payment Type to enable accurate segmentation
* **Category Alignment:** Fixed inconsistent naming conventions in LoyaltyLevel and StoreType to maintain clean, consolidated values
---

### Data Transformation

Applied structural and format changes to optimize datasets for analysis and visualization.

**Key Actions:**

* **Column Restructuring:** Split composite fields such as Full Name into First Name and Last Name for granular analysis
* **Date Formatting:** Standardized all OrderDate entries to consistent date format using DATEVALUE to support time-based analysis
* **Value Formatting:** Applied currency formatting to Unit Price and Total Amount, and percentage formatting to Discount for clear financial reporting
* **Table Structuring:** Converted data ranges into Excel Tables to enable dynamic named references, structured formulas, and efficient Pivot Table creation

---

### Formatting Techniques

Formatting improvements were applied across all datasets to enhance readability, visual clarity, and user interpretation during analysis.

**Tasks Performed:**

* **Currency Formatting:** Applied to Unit Price, Total Amount, and Profit fields for clear financial representation
* **Percentage Formatting:** Standardized Discount values to percentage format to improve comparability
* **Date Formatting:** Converted OrderDate to consistent DD-MM-YYYY format for accurate time-based analysis
* **Table Formatting:** Structured raw data into Excel Tables with banded rows and headers to improve navigation and enable structured references
* **Conditional Formatting:** Used data bars and color scales to highlight high/low sales, profit margins, and outlier values for quick visual insights
---

## Descriptive Statistics Analysis

Descriptive statistical analysis was conducted on each dataset individually to summarize central tendency, dispersion, and distribution of key variables.

**Statistical Measures Analyzed:**

* **Mean:** Calculated average values for numerical fields such as Age, Unit Price, Quantity, and Total Amount
* **Median:** Determined the middle value to assess data symmetry and reduce skew impact
* **Mode:** Identified most frequently occurring values in categorical and discrete fields like Loyalty Level and Store Type
* **Standard Deviation:** Measured variability and spread of data around the mean for sales and pricing metrics
* **Minimum & Maximum Value:** Established the range of data to identify boundaries and potential outliers
* **Range:** Computed the difference between maximum and minimum values to understand data span
* **Count:** Recorded total number of observations to validate dataset completeness

## Purpose:
To derive actionable insights from raw data by summarizing its core characteristics.

**Key Goals:**

* Identify patterns and seasonality in sales data
* Understand customer segmentation and product category distribution
* Establish baseline metrics for KPIs like revenue, profit, and order size

---

## Pivot Table Analysis

Multiple Pivot Tables were constructed to perform multidimensional analysis across key business areas, enabling dynamic data summarization and insight generation.

**Purpose of Analysis:**

* Aggregate large datasets into meaningful summaries without altering raw data
* Enable cross-tabulation of variables such as Sales by Region, Product, and Customer Segment
* Support interactive exploration of trends, comparisons, and performance metrics for decision-making

### Customer Analysis
Used Pivot Tables to segment the customer base across key demographic and behavioral dimensions.

**Key Insights Generated:**

* **Geographic Spread:** Count of customers by State to highlight top-performing regions
* **Loyalty Segmentation:** Breakdown of customers by Loyalty Level for targeted marketing strategies
* **Demographic Split:** Analysis of customer distribution by Gender to support personalized campaigns

### Product Analysis
Used Pivot Tables to break down product metrics across category, stock, and brand dimensions.

**Key Insights Generated:**

* **Category Performance:** Total Revenue and Units Sold by Product Category for portfolio optimization
* **Inventory Health:** Stock levels vs. sales trends to identify reorder points and dead stock
* **Brand Contribution:** Revenue and product distribution by Brand to assess brand-wise market share

### Sales Analysis
Pivot Tables were utilized to examine transactional data and uncover patterns in revenue, volume, and payment behavior.

**Analyses Performed:**

* **Payment Type Analysis:** Aggregated sales and transaction count by Payment Type to identify customer payment preferences and channel performance
* **Sales Performance by Date:** Analyzed daily, monthly, and quarterly sales to detect seasonality, trends, and peak periods
* **Revenue Trends:** Tracked Total Amount over time to evaluate growth patterns and business trajectory
* **Quantity Sold Analysis:** Summarized units sold across products and time frames to assess demand and sales velocity

### Store Analysis
Pivot Tables were constructed to evaluate store performance across different operational and geographic dimensions.

**Analyses Performed:**

* **Store Type Analysis:** Compared revenue, profit, and customer footfall across Store Types to identify high-performing formats
* **Region-wise Performance:** Aggregated sales and profitability metrics by Region to assess market penetration and regional contribution
* **City-based Store Analysis:** Evaluated store-level performance by City to pinpoint top-performing locations and growth opportunities

### Purpose:

To consolidate large datasets into interactive summaries that reveal key business patterns.
  Uncover sales trends and demand fluctuations across business dimensions
  Profile customer behavior by segment, region, and loyalty status
  Benchmark performance across products, stores, and payment channels for strategic planning

---

## Data Visualization and Charts

Charts were generated from Pivot Tables to visually represent key business metrics and enable quick interpretation of trends and patterns.

**Charts Created:**

* Bar Charts: Compared sales performance across Product Categories, Store Types, and Regions for side-by-side analysis
* Column Charts: Displayed revenue and quantity sold over time to highlight monthly and quarterly trends
* Pie Charts: For composition analysis of customer segments and brand contribution
* Line Charts: For time-series analysis of revenue, orders, and demand trends

### Purpose:
To make data-driven insights accessible and actionable through visual storytelling.

**Key Goals:**

* Reduce cognitive load by presenting KPIs and trends graphically
* Enable at-a-glance comparison of performance across business dimensions
* Deliver professional, insight-rich reports for management review

---

## Dashboard Creation

An interactive dashboard was developed in Microsoft Excel to consolidate key business metrics into a single, user-friendly interface for real-time analysis.

**Components Implemented:**

* **Pivot Charts:** Integrated dynamic bar, line, and pie charts linked to Pivot Tables for visualizing revenue, sales trends, and segment distribution
* **Slicers:** Added interactive slicers for Region, Product Category, Store Type, and Date to enable instant data filtering
* **KPI Visualizations:** Designed KPI cards to display critical metrics like Total Revenue, Units Sold, Average Order Value, and Customer Count
* **Filters:** Incorporated report filters and timeline controls to allow drill-down analysis by specific periods or dimensions

**Dashboard Features:**
Built for self-service analytics, the dashboard provides interactive views across all key business dimensions.

**Key Capabilities:**

* **Dynamic Filtering:** One-click slicers for instant drill-down by date, region, category, and store
* **Category & Payment Insights:** Track top-performing segments and preferred payment methods
* **Customer & Store Analytics:** Visualize customer segments and benchmark store performance geographically
* **Executive Summary:** At-a-glance KPIs and trends for quick performance assessment
  
The dashboard delivers an intuitive, consolidated view of business performance for stakeholders and management.

---

## Tools and Features Used

The analysis and dashboard were developed entirely in Microsoft Excel, leveraging the following built-in tools and features:

## Data Preparation & Formatting:

* **Data Cleaning Techniques:** Handled missing values, corrected data types, and standardized text entries
* **Remove Duplicates:** Ensured data integrity by eliminating duplicate transaction records
* **Find and Replace:** Standardized inconsistent naming conventions across categories and brands
* **Text to Columns:** Split composite fields for better granularity and analysis
* **Sorting and Filtering:** Organized data and isolated specific subsets for validation

## Analysis & Visualization:

* **Conditional Formatting:** Highlighted top/bottom performers, outliers, and data thresholds
* **Percentage & Currency Formatting:** Standardized metric display for professional reporting
* **Pivot Tables:** Aggregated data across multiple dimensions for customer, product, sales, and store analysis
* **Pivot Charts:** Created bar, column, line, and pie charts directly from Pivot Tables
* **Slicers:** Enabled interactive filtering in the dashboard for dynamic analysis
* **Descriptive Statistics ToolPak:** Generated summary statistics including mean, median, mode, and standard deviation

## Reporting:
  
* **Dashboard Design:** Combined all elements into an interactive, executive-level dashboard

---

## Requirements

To access, execute, and interact with this Excel-based analysis and dashboard, the following prerequisites are recommended:
## System Requirements:

* **Operating System:** Windows 10 or later / macOS with Excel support
* **Software:** Microsoft Excel 2016 or above, Microsoft 365, or Excel for Web
* **Compatibility:** Full functionality requires desktop Excel; limited interactivity on Excel for Web

## User Requirements:

* **Technical Skills:** Basic proficiency in Microsoft Excel, including navigation and data filtering*
* **Domain Knowledge:** Foundational understanding of data analysis concepts and business metrics

---

## Key Business Insights

The analysis of transactional and customer data revealed several actionable insights to support strategic decision-making:
**Major Findings:**

* **Top-Performing Product Categories:** Identified 3 key categories contributing to over 60% of total revenue, highlighting opportunities for inventory focus and promotions
* **Customer Loyalty Distribution:** Analysis of Loyalty Level showed majority of revenue from Gold and Platinum tiers, indicating strong retention value in premium segments
* **Payment Method Preferences:** Digital payment methods accounted for majority of transactions, with UPI/Card leading in volume and value
* **Region-wise Store Performance:** South and West regions emerged as top revenue contributors, while North showed highest growth potential
* **Sales and Revenue Trends:** Monthly analysis revealed clear seasonality with Q4 peaks; consistent month-over-month growth observed
* **Customer Demographic Patterns:** Age group 25-40 and urban customers drove highest order values; gender distribution showed balanced purchasing behavior
---

## Author

### Priyadharshini Naresh D

## Project Learning Outcome

This project was developed as part of a practical learning journey to enhance proficiency in end-to-end business analytics using Microsoft Excel.

**Skills Developed:**

* **Microsoft Excel:** Advanced functions, formulas, and feature utilization for business analysis
* **Data Cleaning:** Handling missing values, duplicates, and data standardization for analysis readiness
* **Data Analysis:** Applying descriptive statistics and trend analysis to interpret business performance
* **Pivot Tables:** Aggregating and summarizing multi-dimensional data for customer, product, and sales insights
* **Dashboard Creation:** Building interactive dashboards with slicers, KPI cards, and dynamic visuals
* **Business Reporting:** Translating data findings into clear, stakeholder-ready reports and presentations

---

## Version History

### Version 1.0

**Completed:**

* Data cleaning & preprocessing
* Data transformation & feature engineering
* Descriptive statistical analysis
* Pivot Table analysis across 5 business dimensions
* Visualization suite: 6+ chart types implemented
* Interactive Excel dashboard with slicers & KPIs

## Future Improvements
The following enhancements are proposed for subsequent versions to expand analytical capabilities and automation:

**Planned Enhancements:**

* **BI Migration:** Power BI dashboard with real-time data connectivity
* **Automation:** Power Query + VBA for automated ETL and reporting
* **Advanced Analytics:** Predictive modeling for sales forecasting and demand planning
---

## Acknowledgments

This project was made possible with the support of the following tools, platforms, and resources:

* **Microsoft Excel:** For providing a comprehensive suite of data analysis, visualization, and dashboarding capabilities essential to this project
* **GitHub:** For enabling project hosting, version control, and portfolio development to showcase analytical work
* **Learning Resources:** Online courses, documentation, and community forums that contributed to strengthening Excel and data analysis skills

---
