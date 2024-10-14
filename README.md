## Sales Insights Data Analysis 

## Sales Insights 
![Screenshot 2023-12-13 134743](https://github.com/Shashikanttt/sales-insights-data-analysis/assets/101270238/544c7859-5eeb-404c-9af2-6f1f0ef1d709)



### Instructions to setup on your local computer

1. Clone the repository to your local machine.

```bash
git clone git clone https://github.com/Shashikant075/HR-Data-analytics-HR-Domain.git

### Data Analysis Using SQL
### Data Analysis Using power Query and DAX 

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
1. Show total revenue in year 2020 in Chennai
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`
Data Analysis Using Power BI
============================
1. Formula to create norm_amount column
`= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`








