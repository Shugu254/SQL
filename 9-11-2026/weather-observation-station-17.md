## weather-observation-station-17


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-17/problem?isFullScreen=true)


Difficulty : EASY
DB Engine : MySQL

*********

## Intuition
Find the LONG_W corresponding to the smallest LAT_N greater than 38.7780, then round the result to 4 decimal places

## Solution

```SQL
SELECT cast(round(long_W,4) as decimal (10,4))
from station
where LAT_N=(SELECT MIN(LAT_N)From STATION WHERE lat_n>38.7780);

```