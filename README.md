## National Paper Manufacturing
The data for this ficticious company was obtained through the sql for data analysis course of Udacity and the raw data is in this repository. After completing the basic excercises of the course, I was incline to do some extra work, and give a exploratory analysis to the data and create new queries that will give important real life observations that could help the need of the company to allocate new financial injection of resouces to their top players if that would be the case.

<br>

Postgresql was used to create a database with this data, appropiate tables relations and column types were applied to the data. Having a final schema with 5 tables; One fact table: orders; And four dimentional tables: accounts, and  web_events, sales_reps, region, which are sub-tables.

<br>

First and one of the most important steps is to make this data accurate and relyable by cleaning it, and getting rid of any error, resolving missing values, and checking for inconsistencies

<br>

Filling missing values: I could use the "IS NULL" functionality then UPDATE any value WHERE needed. <br>
Identify potential errors: By using DISTINCT I can observe what potential misspelling exist in a column, then UPDATE. <br>
Check for inconsistencies: If I want to check proper range value in a column. MIN and MAX, <br>
                            along with LENGTH can be used then DELETE, WHERE needed.  <br>
                            In the case of extra spaces on values, TRIM can be used. <br>
Mismatched data types: When encounter this problem I can use CAST to convert into an appropiate value. <br>
Check for inconsistent strings: Strings are consistent and meaningful. <br>
Check for misleading column/attributes labels: Columns name are meaningful. <br>
Truncated data: There is not missing data. <br>
Business Logic: Data makes sense given the nature of the business process. <br>


<br>
<br>
<br>




#### List regions buying the most first along with each representatives for each region and which are the most active accounts

Find the number of sales reps in each region. Your final table should have two columns - the region and the number of sales_reps. Order from fewest reps to most reps.

How many of the sales reps have more than 5 accounts that they manage?


How many accounts have more than 20 orders?


Which account has the most orders?


Which accounts spent more than 30,000 usd total across all orders?


Provide a table that provides the region for each sales_rep along with their associated accounts. Your final table should include three columns: the region name, the sales rep name, and the account name. Sort the accounts alphabetically (A-Z) according to account name
Provide the name for each region for every order, as well as the account name and the unit price they paid (total_amt_usd/total) for the order. Your final table should have 3 columns: region name, account name, and unit price. A few accounts have 0 for total, so I divided by (total + 0.01) to assure not dividing by zero.


