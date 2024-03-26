# Coffee_DataSet
## Table of Contents
1. [Introduction](#introduction)
4. [Data Description](#data-description)
5. [Methodology](#methodology)
6. [Results](#results)
7. [Discussion](#discussion)
15. [Conclusion](#conclusion)

## Introduction
In this analysis, I delved into a dataset containing sales information for various coffee types. The dataset comprised order details including order ID, order date, customer ID, product ID, quantity, customer name, email, country, coffee type, roast type, size, unit price, sales, coffee type name, roast type name, and loyalty card status.
The objective of this analysis was to clean the data, extract relevant information, and visualize the overall sales of different coffee types. By examining the sales performance of each coffee type, I aimed to gain insights into consumer preferences and trends.
This analysis provided valuable insights for coffee businesses to understand their market demand, optimize inventory management, and strategize marketing efforts effectively. Let's dive into the data-cleaning process and explore the sales patterns of various coffee types.

## Data Description
| Column Name      | Description                                                                                           | Significance                                                               |
|------------------|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Order ID         | Unique identifier for each order.                                                                     | Helps track individual orders and identify patterns in purchasing behavior. |
| Order Date       | Date when the order was placed.                                                                       | Allows analysis of sales trends over time and seasonality.                 |
| Customer ID      | Unique identifier for each customer.                                                                  | Enables tracking of individual customer's purchasing history and loyalty.   |
| Product ID       | Unique identifier for each coffee product.                                                            | Identifies the specific coffee product purchased in each order.            |
| Quantity         | Number of units of the coffee product purchased.                                                       | Indicates the volume of sales for each product in each order.             |
| Customer Name    | Name of the customer who placed the order.                                                             | Helps identify individual customers and analyze their purchasing behavior. |
| Email            | Email address of the customer.                                                                        | Additional contact information for customers and potential data point for customer segmentation. |
| Country          | Country where the order was placed.                                                                   | Allows analysis of sales performance in different geographic regions.     |
| Coffee Type      | Code representing the type of coffee (e.g., Robusta, Arabica).                                         | Identifies the variety of coffee purchased, crucial for analyzing sales by coffee type. |
| Roast Type       | Code representing the roast level of the coffee (e.g., Light, Medium, Dark).                          | Indicates the roast preference of customers and its impact on sales.      |
| Size             | Size of the coffee product purchased (e.g., 1.0 kg, 0.5 kg).                                           | Allows analysis of sales based on product size and pricing strategy.      |
| Unit Price       | Price per unit of the coffee product.                                                                 | Essential for calculating total sales and analyzing pricing strategies.   |
| Sales            | Total sales amount for each order.                                                                    | Key metric for analyzing revenue and sales performance.                   |
| Coffee Type Name | Name of the coffee type (e.g., Robusta, Arabica).                                                     | Provides a readable format of the coffee type for analysis and visualization. |
| Roast Type Name  | Name of the roast type (e.g., Light, Medium, Dark).                                                   | Provides a readable format of the roast type for analysis and visualization. |
| Loyalty Card     | Indicator of whether the customer has a loyalty card (Yes/No).                                         | Helps analyze the impact of loyalty programs on sales and customer retention. |


## Methodology

### Data Cleaning:

1. **Review the Data:** Initially, I examined the provided datasets, including the customer and product tables, to understand their structure and contents.

2. **Identify Data Issues:** I looked for any anomalies or irregularities in the data that may require attention, such as missing values, incorrect data types, outliers, or formatting inconsistencies.

3. **Handle Missing Data:** Before proceeding with data extraction and aggregation, I ensured that missing data was appropriately handled. This may have involved imputation, removal of records with missing values, or other suitable strategies.

4. **Remove Duplicates:** Duplicates were identified and removed from the dataset to ensure each observation was unique, preventing skewing of results during analysis.
  
### Data Extraction and Aggregation:

1. **Customer Information Extraction:** Using functions like XLOOKUP, I extracted customer information such as name, email, country, and loyalty card status from the customer table and integrated it into the main dataset.

2. **Product Information Extraction:** Similarly, information related to coffee type, roast type, size, unit price, and other product details were extracted from the product table using INDEX and MATCH functions and merged into the main dataset.

3. **Creating Descriptive Columns:** I used IF statements to convert codes into readable formats for columns like Coffee Type Name and Roast Type Name, facilitating better understanding and analysis.

4. **Visualizing Overall Sales:** With the dataset now enriched with relevant information, I aggregated the data to visualize overall sales. This involved grouping the data by coffee type, roast type, or other relevant factors and calculating total sales amounts.

## Results

![Capture](https://github.com/Ariel70/Coffee_DataSet/assets/60137528/3b85d911-82c6-4a2a-a785-9e021ff676a3)

# Sales Analysis
In this section, we analyze the aggregated sales data derived from the line chart, focusing primarily on coffee sales. The analysis includes visualizations and key performance indicators (KPIs).

## Sum of Sales by Year and Coffee Type
The line chart displays the annual sum of sales for four types of coffee: Arabica, Excelsa, Liberica, and Robusta, spanning from 2019 to 2022. 

### Arabica
- Sales started at approximately 3,500 in 2019, peaked at around 4,000 in 2020, decreased to roughly 3,500 in 2021, and ended near 3,000 in 2022. 
- Total sum of Arabica sales over the four years: approximately 14,000.

### Excelsa
- Showed a consistent increase from just under 2,500 in 2019 to about 3,000 in 2021, before plummeting to around 1,500 in 2022. 
- Cumulative sum of Excelsa sales: approximately 10,000.

### Liberica
- Presented lower figures, starting near 2,500 in 2019 and descending to approximately 1,500 by 2022. 
- Total sum for Liberica: around 8,500.

### Robusta
- Displayed the highest volatility, soaring to nearly 4,500 in 2020 from about 2,500 in 2019, then falling to approximately 3,000 in 2021, and sharply declining to just over 1,000 in 2022. 
- Total sum of Robusta sales: roughly 11,000.

The aggregated sum of sales for all coffee types from 2019 to 2022 is approximately 43,500.

## Sum of Sales by Country and Roast Type Name
The bar graph differentiates the sum of sales by country and roast type (Dark, Light, and Medium).

### United States
- Leads with the highest sales across all roast types, with Dark roast approaching 14,000, Medium roast around 8,000, and Light roast near 2,000.

### Ireland
- Significantly lower sales, favoring Medium roast with sales just over 2,000, followed by Dark roast at about 1,000, and negligible sales for Light roast.

### United Kingdom
- Reflects moderate sales for Dark roast, approaching 4,000, and very limited sales for Medium and Light roasts.

## Key Performance Indicators
Two KPIs provide additional insights:

### Sum of Quantity
- The quantity stands at 3551 units, though the specific parameters of this measurement remain unclear.

### Average of Sales
- The average sales value is 45.13, a metric that averages sales data across the dataset but lacks detailed denomination.
