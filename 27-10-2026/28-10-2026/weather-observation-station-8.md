## Weather Observation Station 8


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-8/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
I check whether both the first and last letters of a city name are vowels. Then, I return only the unique city names that meet this condition.  

## Solution

```SQL
SELECT DISTINCT CITY FROM STATION WHERE LOWER(SUBSTR(CITY,1,1)) IN ('a','e','i','o','u') AND LOWER(RIGHT(CITY,1)) IN ('a','e','i','o','u');
```