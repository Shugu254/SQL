## Weather Observation Station 19


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-19/problem?isFullScreen=true)


Difficulty : meduim
DB Engine : MySQL

*********

## Intuition
to try again later

## Solution

```SQL
select cast(round((max(lat_n)-min(lat_n))+(max(long_w))-min(long_w)),4) as decimal(10,4))
from STATION;
```