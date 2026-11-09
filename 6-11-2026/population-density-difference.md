## Population Density Difference


Link: [Hackerrank](https://www.hackerrank.com/challenges/population-density-difference/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
Find the difference between the most populated city and the least populated city in the CITY table
## Solution

```SQL
select max(population)-min(population)
from city;
```