## Weather Observation Station 15


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-15/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
The subquery finds the largest latitude (LAT_N) that is less than 137.2345, while the outer query retrieves the corresponding longitude (LONG_W) for that latitude. The ROUND() function rounds the longitude to four decimal places, and CAST() formats the output as a decimal value with exactly four digits after the decimal point.
## Solution

```SQL
SELECT cast(round(long_w,4) as decimal (10,4))
from station
where lat_n=(select max(lat_n) from station where lat_n<137.2345);

```