## Weather Observation Station 18


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-18/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
MAX() → Finds the highest value.
MIN() → Finds the lowest value.
+ → Adds the latitude and longitude distances
ROUND(..., 4) → Rounds the result to 4 decimal places.
CAST(... AS DECIMAL(10,4)) → Displays the result with exactly 4 decimal places.
## Solution

```SQL
select cast(round((max(lat_n)-min(lat_n))+(max(long_w)-min(long_w)),4) AS decimal(10,4))
from station;

```