## Weather Observation Station 14


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-14/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
WHERE LAT_N < 137.2345 → Filters rows.
MAX(LAT_N) → Returns the highest latitude that meets the condition.
ROUND(value, 4) → Rounds the value to 4 decimal places.
CAST(... AS DECIMAL(10,4)) → Formats the output to show 4 decimal places.
## Solution

```SQL
SELECT cast(round(max(lat_n),4)as decimal (10,4))
From station 
where lat_n<137.2345;

```