Author: @sjtommylee

Date: Aug 05, 2020

# Attempt 1

Prompt: 
Write a SQL query to get the second highest salary from the Employee table.

tb: Employee
cols: Id, Salary

Select the highest Salary, under the alias SecondHighestSalary(required)
WHERE + Subquery should ensure you get the second highest value. 



```sql
SELECT
        MAX(Salary) as SecondHighestSalary
        
FROM
        Employee
        
WHERE
        Salary < (SELECT MAX(Salary) FROM Employee)

```

Time complexity: O(N)

Space complexity: O(N)





# Attempt 2

Solution with no subquery 

```sql
SELECT MAX(a.Salary) as SecondHighestSalary

FROM
    Employee a, Employee b
    
WHERE a.Salary < b.Salary
```

Time complexity: O(N)

Space complexity: O(N)
