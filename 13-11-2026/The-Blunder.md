## The Blunder


Link: [Hackerrank](https://www.hackerrank.com/challenges/the-blunder/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
REPLACE() changes the salary values, while AVG() calculates their average. CEIL() rounds the final result upward
## Solution

```SQL
select ceil(avg(salary)-avg(replace(salary, '0', '')))
from employees;

```