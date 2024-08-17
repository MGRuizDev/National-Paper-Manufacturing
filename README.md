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
![Dummy ](/images/5.png)
<br>

How many times was each chanel used?
<br>
![](/images/6.png)
<br>


For the customer that spent the most (in total over their lifetime as a customer) total_amt_usd, how many web_events did they have for each channel?
<br>
![](/images/7.png)
<br>






<br>
<br>
<br>
<br>



Let’s observe the sales data over time.


Find the sales in terms of total dollars for all orders in each year, ordered from greatest to least. Do you notice any trends in the yearly sales totals?
<br>
![](/images/8.png)
<br>



Which month did Parch & Posey have the greatest sales in terms of total dollars? Are all months evenly represented by the dataset? Include of total number of orders?
<br>
![](/images/9.png)
<br>



<br>
<br>
<br>
<br>






(The reputation of the company is greatly represented by the quality of their products)

Find the mean (AVERAGE) amount spent per order on each paper type, as well as the mean amount of each paper type purchased per order. Your final answer should have 6 values - one for each paper type for the average number of sales, as well as the average amount.
<br>
![](/images/10.png)
<br>



<br>
<br>
<br>
<br>







(Which accounts are the top buyers and what products are they buying)
List accounts top buyers from top to bottom along with the quantity and total of each product
<br>
![](/images/11.png)
<br>




For each account, determine the average amount spent per order on each paper type. Your result should have four columns - one for the account name and one for the average amount spent on each paper type.
<br>
![](/images/12.png)
<br>





We would like to understand 3 different levels of customers based on the amount associated with their purchases. The top level includes anyone with a Lifetime Value (total sales of all orders) greater than 200,000 usd. The second level is between 200,000 and 100,000 usd. The lowest level is anyone under 100,000 usd. Provide a table that includes the level associated with each account. You should provide the account name, the total sales of all orders for the customer, and the level. Order with the top spending customers listed first.
<br>
![](/images/13.png)
<br>






How many accounts had more total purchases than the account name which has bought the most standard_qty paper throughout their lifetime as a customer?
<br>
![](/images/14.png)
<br>




What is the lifetime average amount spent in terms of total_amt_usd for the top 10 total spending accounts?
<br>
![](/images/15.png)
<br>




######################################################
<br>
![](/images/16.png)
<br>






What is the lifetime average amount spent in terms of total_amt_usd, including only the companies that spent more per order, on average, than the average of all orders.




