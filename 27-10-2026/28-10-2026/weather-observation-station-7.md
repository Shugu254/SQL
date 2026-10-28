## Weather Observation Station 7


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
I check if a city ends with a vowel and return only unique city names. 

## Solution

```SQL
SELECT DISTINCT CITY FROM STATION WHERE LOWER(RIGHT(CITY,1))IN ('a','e','i','o','u')
```