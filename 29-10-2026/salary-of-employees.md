## Employee Salaries


Link: [Hackerrank](https://www.hackerrank.com/challenges/salary-of-employees/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition

SALARY > 2000 → filters employees earning more than 2000.
MONTHS < 10 → keeps only employees who have worked for less than 10 months.
AND → ensures both conditions must be true for an employee to be included.
ORDER BY EMPLOYEE_ID ASC → sorts the results by Employee ID in ascending order (smallest ID first).

## Solution

```SQL
SELECT name
From employee
WHERE salary>2000
and months <10
ORDER by employee_id ASC;
```