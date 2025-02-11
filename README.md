<h1 align="center">Data Analysis Project</h1>


![Image](https://github.com/user-attachments/assets/cbb499f2-76f0-4745-8e60-48fb8c6c96e0)

In the above dashboard, the total revenue generated in 2017 is $92.88M, and the total sales quantity is 234K units. Additionally, the dashboard allows you to explore the data in more detail by providing a month-wise breakdown and by segmenting revenue according to different market sets.

**Problem Statement**:


The sales team faces difficulties in accessing real-time sales performance data, leading to delays in decision-making and a lack of clarity on key performance indicators (KPIs). Existing sales reports are static, making it hard to analyze trends, track goals, and detect opportunities for improvement.


Here are some sample code for visualization 


### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

