## Weather Observation Station 16


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-16/problem?isFullScreen=true)


Difficulty : easy
DB Engine : MySQL

*********

## Intuition
The query retrieves the smallest latitude (LAT_N) greater than 38.7780 from the STATION table, rounds it to 4 decimal places, and displays the result in decimal format.
## Solution

```SQL
SELECT cast(round(min(lat_n),4) as decimal (10,4))
From station 
where lat_n>38.7780;

```