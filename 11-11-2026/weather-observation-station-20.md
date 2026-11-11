## Weather Observation Station 20


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-20/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
failed . i'll try again later
## Solution

```SQL
SELECT decimal(PERCENTILE_CONT(0.5)
WITHIN GROUP (ORDER BY LAT_N),10,4)
FROM STATION;
```