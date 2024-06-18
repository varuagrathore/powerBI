# MySQL Database Load and Power BI Connection

This README provides detailed steps to load a database in MySQL and connect it to Power BI for data visualization. Follow these instructions to set up your environment.

## Prerequisites

- MySQL Server
- MySQL Workbench or any MySQL client tool
- Power BI Desktop
- Necessary database files (e.g., `.sql` file for MySQL)

## Step 1: Load Database in MySQL

### 1.1 Import Database from SQL File

1. Open MySQL Workbench.
2. Connect to your MySQL Server instance.
3. In the Navigator panel, right-click on the "Schemas" node and select "Create Schema...".
4. Provide a name for your new schema (database) and click "Apply".
5. Open a new SQL script window by clicking on the "File" menu, then "Open SQL Script...".
6. Browse and select your `.sql` file.
7. Execute the script by clicking on the "Execute" button (lightning bolt icon).

### 1.2 Verify Database Import

1. Once the import is complete, refresh the "Schemas" node to see your new database.
2. Verify that your tables and data are loaded correctly.
3. Run basic queries to ensure the data is loaded correctly.

sql
SELECT * FROM your_table_name LIMIT 10;

### **Step 2:** Connect MySQL Database to Power BI

### 2.1 Install Power BI Desktop

Download and install Power BI Desktop from the official website.

### **-2.2** Install MySQL ODBC Driver

Download and install the MySQL ODBC driver from the official MySQL website.

### **-2.3** Configure ODBC Data Source

Open the ODBC Data Source Administrator:

For Windows, search for "ODBC Data Sources" in the start menu and select the 64-bit version.

Click on the "System DSN" tab.

Click "Add..." to create a new data source.

Select "MySQL ODBC 8.0 Unicode Driver" and click "Finish".

Enter the following details:

Data Source Name: (e.g., MySQL_PowerBI)

Description: (optional)

Server: (your MySQL server address, e.g., localhost)

User: (your MySQL username)

Password: (your MySQL password)

Database: (the name of your database)

Click "Test" to ensure the connection works, then click "OK" to save.

### **2.4** Connect to MySQL Database from Power BI

Open Power BI Desktop.

Click on "Get Data" on the Home ribbon.

Select "ODBC" from the list of data sources and click "Connect".

In the "From ODBC" dialog, select the Data Source Name you configured (e.g., MySQL_PowerBI) and click "OK".

Provide the necessary credentials if prompted and click "Connect".

### **2.5** Load Data into Power BI

After successfully connecting, the Navigator window will appear.

Select the tables or views you want to load into Power BI.

Click "Load" to import the data or "Transform Data" to make adjustments in the Power Query Editor.

## Sales Insights Data Analysis Project





1. SQL database dump is in db_dump.sql file above. Download `db_dump.sql` file to your local computer



### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001)

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



