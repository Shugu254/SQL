## Weather Observation Station 19


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-19/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
MAX(LAT_N) - MIN(LAT_N) calculates the latitude difference.
MAX(LONG_W) - MIN(LONG_W) calculates the longitude difference.
POWER(..., 2) squares each difference.
SQRT() calculates the square root of their sum.
ROUND(..., 4) rounds the final distance to 4 decimal places.
## Solution

```SQL
SELECT round(sqrt(power(max(lat_n)-min(lat_n),2)+power(max(long_w)-min(long_w),2)),4)
from station;

```