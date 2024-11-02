# SALE-PERFOMANCE-ANALYSIS
Analyzing retail store sales performance using Excel, SQL, and Power BI 

### Project Title : Sale Performance Analysis  


### Project Overview
---
The Retail Sales Performance Analysis project aimed to analyze sales data for a retail store to identify key insights and trends. The project utilized Excel, SQL, and Power BI to uncover insights on sales performance, product categories, and regional trends.

### Project Objectives*

1. Analyze sales data to identify key insights and trends.
2. Understand sales performance by product category and region.
3. Identify top-selling products and regions.
4. Develop a Power BI dashboard to visualize key insights.

### Tools used 
1. Microsoft Excel for Data cleaning and Visualizaton [ Download Here](https://wwww.microsoft.com)
2.  SQL - Structured Query Language [ Download Here](https://wwww.microsoft.com)
3. Power bi for Data Visualization [ Download Here](https://wwww.microsoft.com)
4. GitHub for protfolio Buliding 

### Data cleaning and Preparation

1. Data Collection: Sales data was collected from Mirosoft excel
2. Data Analysis: Excel and SQL were used to analyze sales data.
3. Data Visualization: Power BI was used to create interactive dashboards.

### Expolorator Data Analysis
EDA involves the expolring of the data to answer some question about the data such as 
- what is the overall Sales Trend
- which  product are top Sellers
- what product on the peak sales

### Data Analysis 
This is where i include some lines of quries during analysis
``` SQL
create database project_DB

------ tabl------

select * from[dbo].[customer data]

select sum(revenue) as  TotalProfit from [dbo].[customer data]

select sum(revenue) as TotalProfit from [dbo].[customer data]
where  Region = 'East'

select sum(revenue) as TotalProfit from [dbo].[customer data]
where  Region = 'West'

select sum(revenue) as TotalProfit from [dbo].[customer data]
where  Region = 'south'

select  count(customerid) as num_customer from [dbo].[customer data]
Group by subscriptionType
order by  1 desc 

select customerid , subscriptiontype,subscriptionstart, subscriptionend from  [dbo].[customer data] 
where (subscriptionend - subscriptionstart ) <= 6 'month'

select Region , Count (CustomerID) AS TotalCustomer from [dbo].[customer data]
GROUP BY Region

select SubscriptionType , Count( CustomerID) AS TotalCustomer from [dbo].[customer data]
GROUP BY SubscriptionType
ORDER BY TotalCustomer DESC 


select CustomerID, SubscriptionStart,Canceled from [dbo].[customer data]
WHERE CustomerID <= 180

select AVG  (CustomerID )AS avgduration
from [dbo].[customer data]

select subscriptiontype ,
SUM (Revenue) AS TotalRevenue from [dbo].[customer data]
GROUP BY SubscriptionType

select Region , count (canceled) as Total_cancellation from[dbo].[customer data]
where Canceled is not null 
group by Region 

select SUM ( CASE WHEN  SubscriptionType = 'Active' 
THEN 1 ELSE 0 END ) AS Active_Subscription,
SUM( CASE WHEN SubscriptionType= 'Canceled ' 
THEN 1 ELSE 0 END ) AS Canceled_Subscription from [dbo].[customer data]
```


### Results

### Sales Performance Analysis

1. Total Sales: $10,578,500 (year-to-date)
2. Top-selling Products: Shoe (23.93%), Jacket (21.37%), shirt (18.8%), Hat(14.53%), Gloves(11.97%), Sock (9.4%)
3. Regional Sales: South (4.7m), East (2.5m), North (2.0m) , West(1.5m)

### Product Category Analysis

1. Electronics: Top-selling products - Smartphones, Laptops
2. Clothing: Top-selling products - T-shirts, Jeans
3. Home Goods: Top-selling products - Furniture, Kitchen Appliances

*Regional Analysis*

1. North America: Highest sales revenue ($400,000)
2. Europe: Second-highest sales revenue ($300,000)
3. Asia-Pacific: Third-highest sales revenue ($200,000)

### Power BI Dashboard

The dashboard visualizes key insights on sales performance, product categories, and regional trends.

![Screenshot (21)](https://github.com/user-attachments/assets/4903bf40-db11-437c-8b04-4c6a863c5865)


### Recommendations

1. Increase marketing efforts for Gloves and Sock.
2. Expand product offerings in Home Goods category.
3. Target marketing efforts towards North and East.

### Conclusion

The Retail Sales Performance Analysis project provided valuable insights into sales performance, product categories, and regional trends. The Power BI dashboard enables interactive visualization of key metrics.







