[Go To Home Page ](./READEME.md)
# SQL Queries 
## SQL:  stand for structerd query language
 
| summarizing  | Image |
|---|---|
|The **SELECT** statement is used to select data from a database.The data returned is stored in a result table  | ![Exercise 1 ](./images/exercise1.png) |
| The **WHERE** clause is used to filter records.  | ![Exercise 2 ](./images/2.png) |
|operators can be used in the WHERE clause =,>,<,<=,>=,**LIKE**, **NOT LIKE**,..etc | ![ Exercise 3 ](./images/exercise3.png) |
| The SELECT **DISTINCT** statement is used to return only distinct (different) values. The **ORDER BY** keyword is used to sort the result-set in ascending or descending order. The **LIMIT row_count** determines the number of rows returned by the query. The **OFFSET** will specify where to begin counting the number rows from.| ![Exercise 4 ](./images/4.png) |
| SQL Review:   | ![Review 1 ](./images/5.png)  |
| The **INNER JOIN** selects all rows from both tables as long as there is a match between the columns.   | ![Exercise 6 ](./images/6.png)  |


## Queries
-  SELECT
```
SELECT column, another_column, … FROM mytable WHERE condition AND/OR another_condition AND/OR …;
```
***Queries with constraints***

- = Case sensitive exact string comparison

- != or <> Case sensitive exact string inequality comparison

- LIKE Case insensitive exact string comparison

- NOT LIKE Case insensitive exact string inequality comparison

- % Used anywhere in a string to match a sequence of zero or more characters

- IN (…) String exists in a list

- NOT IN (…) String does not exist in a list

***Filtering and sorting Query results***
```
SELECT DISTINCT column, another_column, … FROM mytable WHERE condition(s) ORDER BY column ASC/DESC LIMIT num_limit OFFSET num_offset;
```
***Multi-table queries with JOINs***
```
SELECT c1,c2,... FROM table1 INNER JOIN table2 ON table1.id = table2.id WHERE condition(s) ORDER BY c1 or c2 ASC/DESC LIMIT num_limit OFFSET num_offset;
```
- INSERT rows
```
INSERT INTO table (c1,c2,c3,..) VALUES (v1,v2,v3,...)
```
