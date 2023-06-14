# Data-Analysis-With-SQL---Sales-Revenue-Insights


# Project Description:

Data Cleaning with SQL - MySQL tool to clean the Data and Data analysis using SQL Query.
Calculated Sales, Profit and Revenue using Measures and Analysed data.
Extract the data from SQL, Transform and Load data to Tableau for Business analysis.

![image](https://github.com/Meenaharshini/Data-Analysis-With-SQL---Sales-Revenue-Insights/assets/108173891/eea411d9-9290-410a-a969-af2a77f7369b)

# SQL Query:

SELECT * FROM sales.transactions;
Select * from sales.transactions where market_code = 'Mark001'; 
Select distinct product_code from sales.transactions where market_code = 'Mark001';

Select * from sales.transactions where currency = "USD";

    # Using Inner Join
    
Select sales.transactions.*, sales.date.* FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date 
WHERE sales.date.year = 2020;

SELECT sum(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date
WHERE sales.date.year = 2020 AND sales.transactions.currency = "INR\r" OR sales.transactions.currency ="USD\r";

Select sum(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date
WHERE sales.date.year = 2020 AND sales.date.month_name = "January" AND (sales.transactions.currency ="INR\r" OR sales.transactions.currency="USD\r");

SELECT sum(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date
WHERE sales.date.year = 2020 AND sales.date.month_name="January";
