## Employee Names


Link: [Hackerrank](https://www.hackerrank.com/challenges/name-of-employees/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition

SELECT NAME → retrieves the names of all employees.
FROM EMPLOYEE → gets the data from the EMPLOYEE table.
ORDER BY NAME ASC → sorts the employee names in alphabetical order (A to Z).

## Solution

```SQL
SELECT NAME
From EMPLOYEE
ORDER BY NAME ASC;
```