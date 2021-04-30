Author: @sjtommylee

Date: 04 09, 2021

# Attempt 1

Prompt:
The Employee table holds all employees including their managers. Every employee has an Id, and there is also a column for the manager Id.
+----+-------+--------+-----------+
| Id | Name | Salary | ManagerId |
+----+-------+--------+-----------+
| 1 | Joe | 70000 | 3 |
| 2 | Henry | 80000 | 4 |
| 3 | Sam | 60000 | NULL |
| 4 | Max | 90000 | NULL |
+----+-------+--------+-----------+
Given the Employee table, write a SQL query that finds out employees who earn more than their managers.

```sql

SELECT e1.Name as Employee
From Employee e1, Employee e2
WHERE e1.ManagerId = e2.Id and e1.Salary > e2.Salary

```

Time complexity: O(N)

Space complexity: O(N)
