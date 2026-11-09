## Average Population


Link: [Hackerrank](https://www.hackerrank.com/challenges/average-population/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
round 0 ..... rounds off to the nearest whole number
avg.... gives the average for population
## Solution

```SQL
SELECT round(avg(population), 0)
From city;
```