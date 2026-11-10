## Top Earners


Link: [Hackerrank](https://www.hackerrank.com/challenges/earnings-of-employees/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition


The query calculates each employee's total earnings using salary * months, finds the maximum total earnings with MAX(), and then counts how many employees earned that maximum amount using COUNT(*).

## Solution

```SQL
select max(salary*months), count(*)
from employee
where salary*months =(select max(months*salary) from Employee)

```