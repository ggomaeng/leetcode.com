Author: @sjtommylee

Date: 04 09, 2021

# Attempt 1

Prompt:
Write a SQL query to delete all duplicate email entries in a table named Person, keeping only unique emails based on its smallest Id.
Tb Person
Id, Email Col.

used a join - on

```sql
DELETE P1
FROM Person p1
JOIN Person p2 on p1.Email = p2.Email
AND p1.ID > p2.ID

```

Time complexity: O(N)

Space complexity: O(N)
