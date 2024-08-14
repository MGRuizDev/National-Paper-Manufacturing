## National Paper Manufacturing
The data for this ficticious company was obtained through the sql for data analysis course of Udacity and the data is in this repository. After completing the basic excercises of the course, I was incline to do some extra work, and give a exploratory analysis to the data and create new queries that will give important real life observations that could help the need of the company to allocate new financial injection of resouces to their top players if that would be the case.

<br>

Postgresql was used to create a database with this data, appropiate tables relations and column types were applied to the data. Having a final schema with 5 tables; One fact table: orders; And four dimentional tables: accounts, and  web_events, sales_reps, region.

<br>

First and one of the most important steps is to make this data accurate and reliable by cleaning it, getting rid of any error, resolving missing values, and checking for inconsistencies.

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




#### 1  List all regions along with each representatives for each region and their respective active account.
<br>
#1picture
<br>
A quick overview of the 350 accounts with the representative and region to which they belong and the total revenue. We can tell that Northeast has more accounts.
<br>
<br>
2 Provide the name of the sales_rep in each region with their amount of total_amt_usd sales.
<br>
##2
<br>
This shows the total amount of revenue by each representative.
<br>
<br>
3 Joining two subqueries
<br>
##3
<br>
A small tweak to the last query (sub2) to show only regions and largest total revenue, then join two queries, the modified sub2 and the sub. Now we can get the best representatives by region.
<br>
<br>
4 For the region with the largest (sum) of sales total_amt_usd, how many total (count) orders were placed?
<br>
##4
<br>
