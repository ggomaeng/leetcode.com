Author: @sjtommylee

Date: Aug 05, 2020

# Attempt 1

Prompt: 
A country is big if it has an area of bigger than 3 million square km or a population of more than 25 million.
Write a SQL solution to output big countries' name, population and area.

tb: World
cols: continent, area, population, gdp


You can use a combination of WHERE + OR clauses to satisfy the two conditions. 


```sql

SELECT 
        name, population, area
FROM
        World
WHERE   
        area > 3000000 OR population > 25000000
```

Time complexity: O(N)

Space complexity: O(N)