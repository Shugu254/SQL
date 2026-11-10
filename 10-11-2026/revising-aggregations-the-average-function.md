## Revising Aggregations - Averages


Link: [Hackerrank](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
The query first filters all cities located in the California district using the WHERE clause, then calculates the average of their populations using the AVG() aggregate function.
## Solution

```SQL
SELECT avg(population)
from City
where district='California';

```