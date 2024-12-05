# Data Analysis Using SQL

#### Total number of customers

SELECT count(*) FROM customers;

#### Wierd trasnsactions

SELECT * FROM sales.transactions WHERE sales_amount <=0;

#### Total revenue in year 2020 in Chennai

SELECT 
 SUM(sales.transactions.sales_amount)
FROM sales.transactions 
JOIN sales.date
ON sales.transactions.order_date = sales.date.date
WHERE sales.date.year = 2020 AND sales.transactions.market_code= 'Mark001' 
;