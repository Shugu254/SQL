## Weather Observation Station 11


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-11/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.

## Solution

```SQL
SELECT DISTINCT CITY FROM STATION WHERE LOWER(SUBSTR(CITY,1,1)) NOT IN ('a','e','i','o','u') OR LOWER(RIGHT(CITY,1)) NOT IN ('a','e','i','o','u');
```