# Power_BI_Final_Project
 Sales & Customer Intelligence Dashboard (Power BI)
 Project Overview

This project is an end-to-end Power BI dashboard designed to analyze sales performance, customer behavior, and profitability across regions, products, and customer segments.
The dashboard helps business users and management make data-driven decisions using interactive visuals, KPIs, and advanced DAX calculations.

 Business Objectives

Analyze overall sales and profit performance

Identify top customers and customer segments

Track profit margin and profitability categories

Monitor sales trends over time

Enable drillthrough analysis for detailed insights

Implement Row-Level Security (RLS) for data access control

 Dataset Description

The project uses a star schema model with the following tables:

Dimension Tables

Date_Dim – Date, Month, Year, Year-Month

Customer_Dim – Customer details, segment

Product_Dim – Product and category details

Region_Dim – Regional information

Fact Tables

Sales_Fact – Sales transactions, quantity, cost, profit

Returns_Fact – Returned sales data

 Data Model

Star schema design

One-to-many relationships

Single-direction filtering

Date table marked for time intelligence

 Key DAX Measures

Some important measures used in the project:

Total Sales = SUM(Sales_Fact[SalesAmount])
Total Profit = SUM(Sales_Fact[Profit])
Net Sales = [Total Sales] - [Total Returns]
Profit Margin = DIVIDE([Total Profit], [Total Sales])
Total Customers = DISTINCTCOUNT(Customer_Dim[CustomerID])

Profit Margin Category
Profit Margin Category =
SWITCH(
    TRUE(),
    [Profit Margin] < 0, "Loss",
    [Profit Margin] < 0.20, "Low",
    [Profit Margin] < 0.40, "Medium",
    "High"
)

 Dashboard Pages
 Page 1: Executive Overview

KPI Cards: Total Sales, Net Sales, Total Profit, Profit Margin

Sales trend over time

Sales by region

Sales by product category

Interactive slicers (Date, Region, Product, Segment)

 Page 2: Sales & Customer Analysis

KPI Cards for sales and customer metrics

Sales by customer segment

Top 10 customers by sales

Profit Margin Category distribution

Sales trend analysis

 Page 3: Customer Intelligence

Customer segmentation analysis

Top customers by profit

Average Order Value (AOV)

Customer-level insights

 Page 4: Drillthrough Detail Page

Drillthrough by Customer, Product, and Region

Detailed sales, profit, and margin analysis

 Row-Level Security (RLS)

Implemented to restrict data access by region

Role-based security using DAX filters

Tested using View As Role feature

 Mobile Optimization

Mobile layout designed for Executive Overview

Optimized for KPI monitoring and quick insights

 Tools & Technologies

Power BI Desktop

DAX (Data Analysis Expressions)

Power Query

Excel (Data Source)

 Key Features

Interactive dashboards

Advanced DAX calculations

Time intelligence (YTD, YoY, MoM)

Profitability analysis

Drillthrough and slicers

Professional UI/UX design

 How to Use

Open the .pbix file in Power BI Desktop

Refresh data (if required)

Use slicers to filter insights

Drillthrough for detailed analysis

View mobile layout for executive summary



This Power BI project demonstrates real-world business intelligence skills, including data modeling, DAX, dashboard design, and security implementation.
It is suitable for portfolio presentation, interviews, and enterprise reporting scenarios.
