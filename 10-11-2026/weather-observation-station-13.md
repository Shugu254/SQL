## Weather Observation Station 13


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-13/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
This query filters all latitude values (LAT_N) that fall between 38.7880 and 137.2345 using the BETWEEN operator, calculates their total using SUM(), and then formats the result as a decimal number with 10 digits in total and 4 digits after the decimal point using DECIMAL().
## Solution

```SQL
SELECT DECIMAL(SUM(LAT_N), 10, 4)
FROM STATION
WHERE LAT_N BETWEEN 38.7880 AND 137.2345;

```