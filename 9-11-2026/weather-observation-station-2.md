## Weather Observation Station 2


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-2/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
Calculate the total of all LAT_N and LONG_W values, round each total to 2 decimal places, and format the output to display exactly 2 decimal places.
## Solution

```SQL
SELECT
    CAST(ROUND(SUM(LAT_N), 2) AS DECIMAL(10,2)),
    CAST(ROUND(SUM(LONG_W), 2) AS DECIMAL(10,2))
FROM STATION;

```