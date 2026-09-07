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
