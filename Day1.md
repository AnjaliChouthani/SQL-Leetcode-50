## Day 1 - SQL Practice

### Q1. Big Countries (SQL LeetCode 50)

**Given:**  
We have a table which consists of `name`, `continent`, `area`, `population` and `gdp`.

**Task:**  
Find the name, area and population of big countries.

**A country is called a big country if:**
- area is at least 3 million **OR**
- population is at least 25 million

**SQL Query:**

```sql
SELECT name, population, area
FROM world
WHERE area >= 3000000
   OR population >= 25000000;
```


### Q2. Article Views I

**Given:-**
We have given a views table that consist of some column -
| article_id    | int    |
| author_id     | int    |
| viewer_id     | int    |
| view_date     | date   |


**Write a solution to find all the authors that viewed at least one of their own articles.**

**SQL Query**

```select distinct author_id as id from views where author_id = viewer_id order by author_id asc;
```


### Q3. Invalid Tweets

**Given:-**

| Column Name    | Type    |
+----------------+---------+
| tweet_id       | int     |
| content        | varchar |
+----------------+---------+


**Write a solution to find the IDs of the invalid tweets.**
**The tweet is invalid if the number of characters used in the content of the tweet is strictly greater than 15.**



**SQL Query**
```
select tweet_id from tweets where LENGTH(content)>15;
```


### Q4. Replace Employee ID With The Unique Identifier

Table: Employees

+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| id            | int     |
| name          | varchar |


Table: EmployeeUNI

+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| id            | int     |
| unique_id     | int     |
+---------------+---------+

**Write a solution to show the unique ID of each user, If a user does not have a unique ID replace just show null.**

```
select b.unique_id, a.name from employees  a left join employeeUNI b on 
a.id=b.id;
```
