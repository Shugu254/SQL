## Weather Observation Station 4


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-4/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
COUNT(CITY) → counts all city records in the table.
COUNT(DISTINCT CITY) → counts each unique city only once.
COUNT(CITY) - COUNT(DISTINCT CITY) → gives the number of duplicate city entries.

## Solution

```SQL
SELECT count(City) - count(distinct City)
From station;
```