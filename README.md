## National Paper Manufacturing
The data for this ficticious company was obtained through the sql for data analysis course of Udacity and the data is in this repository. After completing the basic excercises of the course, I was incline to do some extra work, and give a exploratory analysis to the data and create new queries that will give important real life observations that could help the need of the company to allocate new financial injection of resouces to their top players if that would be the case.

<br>

Postgresql was used to create a database with this data, appropiate tables relations and column types were applied to the data. Having a final schema with 5 tables; One fact table: orders; And four dimentional tables: accounts, and  web_events, sales_reps, region.

<br>

First and one of the most important steps is to make this data accurate and reliable by cleaning it, getting rid of any error, resolving missing values, and checking for inconsistencies.

<br>

Filling missing values: <br>
I could use the "IS NULL" functionality then UPDATE any value WHERE needed. <br>
<br>
Identify potential errors: <br>
By using DISTINCT I can observe what potential misspelling exist in a column, then UPDATE. <br>
<br>
Check for inconsistencies: <br>
If I want to check proper range value in a column. MIN and MAX, <br>
                            along with LENGTH can be used then DELETE, WHERE needed.  <br>
                            In the case of extra spaces on values, TRIM can be used. <br>
<br>
Mismatched data types: <br>
When encounter this problem I can use CAST to convert into an appropiate value. <br>
<br>
Check for inconsistent strings: <br>
Strings are consistent and meaningful. <br>
<br>
Check for misleading column/attributes labels: <br>
Columns name are meaningful. <br>
<br>
Truncated data: <br>
There is not missing data. <br>
<br>
Business Logic: <br>
Data makes sense given the nature of the business process. <br>


<br>
<br>
<br>




#### QUERIES
1.- List all regions with their respective representatives showing active accounts and total revenue for each representative.
<br>
![Region, Account, Representative Revenue](/images/1.png)
<br>
 A quick overview of the 350 accounts and which representatives they are working with and  total revenue each is accumulaiting. We can tell that Northeast has more accounts.
 
<br>
<br>
<br>
<br>

2.- Provide the representatives with their total revenue by region.
<br>
![Total Revenue Representative](/images/2.png)
<br>
What region has more bestsellers representatives and which are not doing very good.

<br>
<br>
<br>
<br>

3.- List only the best sellers of each region.
<br>
![Total Region Revenue](/images/3.png)
<br>
A small tweak to the last query (sub2) to show only regions and largest total revenue, then join two queries, the modified sub2 and the sub. Now we can get only the best representatives by region.

<br>
<br>
<br>
<br>

4.- For the region with the largest of sales, how many total orders were placed?
<br>
![Total Orders By Region](/images/4.png)
<br>
The volume of orders made from the best performer region.

<br>
<br>
<br>
<br>

5.- The time between first contact and buying can tell us if the channel is working properly or if there is a preferred channel to use. And if the order is small or large) Show orders time by web_events time, calculate duration time between them, and channel used, also account name,(avg duration by channel). Total in usd.
<br>
![Dummy ](/images/5.png)
<br>
How long it took for the buyers to make the sale from the time of initial interest for the product to the time of the order placed.

<br>
<br>
<br>
<br>

6.- How many times was each chanel used?
<br>

![](/images/6.png)
<br>
Which of the channels, to attract buyers and generate sales, are the most used.

<br>
<br>
<br>
<br>

7.- For the customer that spent the most over their lifetime, how many web_events did they have for each channel?
<br>
![](/images/7.png)
<br>
Which are the buying habits of the best customer.

<br>
<br>
<br>
<br>

8.- Find the sum of sales revenue for each year, order by year. 
<br>
![](/images/8.png)
<br>
I can observe the sales data over time, in order to notice any trends in the yearly sales totals.

<br>
<br>
<br>
<br>

9.- Total revenue and number of orders by month.
<br>
![](/images/9.png)
<br>
Which months have more sales and total revenue.


<br>
<br>
<br>
<br>

10.- Find the mean (AVERAGE) amount spent per order on each paper type, as well as the mean amount of each paper type purchased per order.
<br>
![](/images/10.png)
<br>
Which type of paper is more in demand and which are not, there is a reason. The reputation of the company is greatly represented by the quality of their products, therefore having a view of how the products sales situation it is important.


<br>
<br>
<br>
<br>

11.- List accounts top buyers from top to bottom along with the total quantity of each product.
<br>
![](/images/11.png)
<br>
Which accounts are the top buyers and what products are they buying.

<br>
<br>
<br>
<br>

12.- For each account, determine the average amount spent per order on each paper type.
<br>
![](/images/12.png)
<br>
How much are customers spending on each product, and what is the mean of total sales to avoid outliers that my skewd the results.

<br>
<br>
<br>
<br>

13.- We would like to understand 3 different levels of customers based on the amount associated with their purchases. The top level includes anyone with a Lifetime Value (total sales of all orders) greater than 200,000 usd. The second level is between 200,000 and 100,000 usd. The lowest level is anyone under 100,000 usd. Provide the level associated with each account in the results.
<br>
![](/images/13.png)
<br>
Want to know who is your most loyal customer who spends a lot of money on the products.

<br>
<br>
<br>
<br>

14.- How many accounts had more total purchases than the account name which has bought the most standard_qty paper throughout their lifetime as a customer?
<br>
![](/images/14.png)
<br>

<br>
<br>
<br>
<br>

15.- What is the lifetime average amount spent in terms of total_amt_usd for the top 10 total spending accounts?
<br>
![](/images/15.png)
<br>

<br>
<br>
<br>
<br>

16.- What is the average of total sales for each of the top 10 buyers.
<br>
![](/images/16.png)
<br>

<br>
<br>
<br>
<br>



What is the lifetime average amount spent in terms of total_amt_usd, including only the companies that spent more per order, on average, than the average of all orders.




