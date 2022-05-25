## Sales Insights Data Analysis Project

 **Microsoft Power Bi, Mysql, Data Wrangling.**

Mysql database has all sales transactions, customers, products and markets information. I have analyse this database and than hook it up with power BI. In power BI I perform ETL and data cleaning operations to make it ready so that we can build our dashboard. Then build a powerful dashboard that can help us generate sales insights on Atliq hardware business.

 **Data Analysis Using SQL**

1. All customer records

    SELECT * FROM customers;

1. Total number of customers

    SELECT count(*) FROM customers;

1. Transactions for Chennai market (market code for chennai is Mark001

    SELECT * FROM transactions where market_code='Mark001';

1. Distinct product codes that were sold in chennai

    SELECT distinct product_code FROM transactions where market_code='Mark001';

1. Transactions where currency is US dollars

    SELECT * from transactions where currency="USD"

1. Transactions in 2020 join by date table

    SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

1. Total revenue in year 2020,

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
	
1. Total revenue in year 2020, January Month,

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

1. Total revenue in year 2020 in Chennai

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";


**Data Visualization**

![image](https://user-images.githubusercontent.com/46858938/170222482-820e29b8-3422-4b4a-9f16-4f42394cb2c1.png)
![image](https://user-images.githubusercontent.com/46858938/170222623-79a476e9-eb06-432f-9251-63c2c34029e0.png)
![image](https://user-images.githubusercontent.com/46858938/170223016-64e54fc9-1a2e-4b22-8494-62f642f3237d.png)



