# Instacart Sales & Customer Behavior Dashboard (Power BI)
#  Project Overview
This Power BI dashboard analyzes Instacart customer purchasing behavior using real transaction data. It reveals patterns in product popularity, reorder habits, and shopping time preferences.
The project showcases skills in data modeling, DAX, interactive filtering, and visual storytelling.

#  Business Questions Addressed
What are the most frequently purchased products on Instacart?
Which products have the highest reorder rates?
When do customers place the most orders (by hour and day)?
Which departments and aisles drive the most product sales?

## Tools & Technologies
Power BI Desktop
Power Query for data cleaning
DAX for calculated metrics
GitHub for portfolio hosting
##  Dataset
orders – order ID, user ID, order time, day of week
order_products – products purchased per order, reorder flag
products – product names and IDs
aisles – aisle names
departments – department names

## Data Preparation (Power Query)
Key cleaning and transformation steps:
Removed nulls and duplicates
Converted data types (dates, integers, text)
Merged tables using keys (product_id, order_id, aisle_id, department_id)
Created a Date Table for time intelligence
Added calculated columns for:
Day name
Hour bucket
Product hierarchy

## DAX Measures
Examples of DAX used in the dashboard:
Total Orders = DISTINCTCOUNT(orders[order_id])
Total Products Sold = COUNT(order_products[product_id])
Reorder Rate = AVERAGE(order_products[reordered])
Average Basket Size = [Total Products Sold] / [Total Orders]

## Dashboard Features
### Executive Metrics
Total Orders: 3M
Total Products Sold: 34M
Reorder Rate: 0.59
Average Basket Size: 10.11
### Time-Based Behavior
Orders by Day of Week (0 = Sunday to 6 = Saturday)
Orders by Hour of Day (peak hours identified)
### Product-Level Insights
Top-selling products (e.g., Bananas, Strawberries, Avocados)
Reorder rate by product
Product filters: Department, Aisle, Product Name
### Category Breakdown
Treemap of products sold by Aisle
Bar chart of products sold by Department
Highlights top categories: Produce, Dairy & Eggs, Snacks

## Key Insights
Bananas are the most purchased item (~0.49M units)
Fresh fruits and vegetables dominate sales volume
Reorder rate of 0.59 shows strong customer loyalty
Most orders placed between 10 AM and 4 PM, peaking midday
Produce department accounts for nearly 30% of all products sold

![Instacart Dashboard](image.png)

