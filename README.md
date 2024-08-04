## National Paper Manufacturing
The data for this ficticious company was obtained through the sql for data analysis course of Udacity and the raw data is in this repository. After completing the basic excercises of the course, I was incline to do some extra work, and give a exploratory analysis to the data and create new queries that will give important real life observations that could help the need of the company to allocate new financial injection of resouces to their top players if that would be the case.

<br>

Postgresql was used to create a database with this data, appropiate tables relations and column types were applied to the data. Having a final schema with 5 tables; One fact table: orders; And four dimentional tables: accounts, and  web_events, sales_reps, region, which are sub-tables.

<br>

First and one of the most important steps is to make this data accurate and relyable by cleaning it, and getting rid of any error, resolving missing values, and checking for inconsistencies

<br>

Filling missing values      WHERE num_of_doors IS NULL; if there are use: UPDATE car_info SET num_of_doors = "four" WHERE make = "dodge"
Identify potential errors   You can use SELECT DISTINCT to check what values exist in a column any misspelling, if any use UPDATE
Check for inconsistencies   length column (SELECT MIN(length), MAX(length) FROM cars.car_info;), proper range value column (SELECT MIN(length), if                              any can use DELETE WHERE), extra spaces

Sources of errors:
Null data: 
Misspelled words: 
Mistyped numbers: 
Extra spaces and characters:  TRIM function?
Duplicates: DISTINCT in SQL?
Mismatched data types: numeric, date, and string data are typecast correctly?
Messy (inconsistent) strings: strings are consistent and meaningful?
Messy (inconsistent) date formats: 
Misleading variable labels (columns): columns name are meaningful?
Truncated data: truncated or missing data that needs correction?
Business Logic: Did you check that the data makes sense given your knowledge of the business? 




