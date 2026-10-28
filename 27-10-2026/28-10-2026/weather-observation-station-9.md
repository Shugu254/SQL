## Weather Observation Station 9


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-9/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
I check if the first letter of each city is not a vowel. Then, I return only the unique city names that meet this condition.

## Solution

```SQL
SELECT DISTINCT CITY FROM STATION WHERE LOWER(SUBSTR(CITY,1,1)) NOT IN ('a','e','i','o','u');
```