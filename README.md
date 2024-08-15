## National Paper Manufacturing
The data for this ficticious company was obtained through the sql for data analysis course of Udacity and the data is in this repository. After completing the basic excercises of the course, I was incline to do some extra work, and give a exploratory analysis to the data and create new queries that will give important real life observations that could help the need of the company to allocate new financial injection of resouces to their top players if that would be the case.

<br>

Postgresql was used to create a database with this data, appropiate tables relations and column types were applied to the data. Having a final schema with 5 tables; One fact table: orders; And four dimentional tables: accounts, and  web_events, sales_reps, region.

<br>

First and one of the most important steps is to make this data accurate and reliable by cleaning it, getting rid of any error, resolving missing values, and checking for inconsistencies.

<br>

Filling missing values: I could use the "IS NULL" functionality then UPDATE any value WHERE needed. <br>
<br>
Identify potential errors: By using DISTINCT I can observe what potential misspelling exist in a column, then UPDATE. <br>
<br>
Check for inconsistencies: If I want to check proper range value in a column. MIN and MAX, <br>
                            along with LENGTH can be used then DELETE, WHERE needed.  <br>
                            In the case of extra spaces on values, TRIM can be used. <br>
<br>
Mismatched data types: When encounter this problem I can use CAST to convert into an appropiate value. <br>
<br>
Check for inconsistent strings: Strings are consistent and meaningful. <br>
<br>
Check for misleading column/attributes labels: Columns name are meaningful. <br>
<br>
Truncated data: There is not missing data. <br>
<br>
Business Logic: Data makes sense given the nature of the business process. <br>


<br>
<br>
<br>




#### QUERIES
List all regions along with each of their representatives and their respective active account.
<br>
![Region, Account, Representative Revenue](/images/1.png)
<br>
A quick overview of the 350 accounts with the representative and region to which they belong and the total revenue. We can tell that Northeast has more accounts.
<br>
<br>
Provide the name of the sales_rep in each region with their amount of total_amt_usd sales.
<br>
![Total Revenue Representative](/images/2.png)
<br>
This shows the total amount of revenue by each representative.
<br>
<br>
Show the best representative for each region
<br>
![Total Region Revenue](/images/3.png)
<br>
A small tweak to the last query (sub2) to show only regions and largest total revenue, then join two queries, the modified sub2 and the sub. Now we can get the best representatives by region.
<br>
<br>
For the region with the largest (sum) of sales total_amt_usd, how many total (count) orders were placed?
<br>
![Total Orders By Region](/images/4.png)
<br>





(The time between first contact and buying can tell us if the channel is working properly or if there is a preferred channel to use. And if the order is small or large)
Show orders time by web_events time, calculate duration time between them, and channel used, also account name,(avg duration by channel). Total in usd.

<br>
![](/images/5.png)
<br>

Which accounts used facebook as a channel to contact customers more than 6 times?


<br>
![](/images/6.png)
<br>


For the customer that spent the most (in total over their lifetime as a customer) total_amt_usd, how many web_events did they have for each channel?


<br>
![](/images/7.png)
<br>
