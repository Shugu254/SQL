## Weather Observation Station 5


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-5/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
MIN(LENGTH(CITY)) → finds the shortest city name length.

WHERE LENGTH(CITY) = ... → keeps only cities with that shortest length.

ORDER BY CITY ASC → breaks ties alphabetically.

LIMIT 1 → returns the first city only.

MAX(LENGTH(CITY)) → finds the longest city name length.

WHERE LENGTH(CITY) = ... → keeps only cities with that longest length.

ORDER BY CITY ASC → breaks ties alphabetically.

LIMIT 1 → returns the first city only.
## Solution

```SQL
SELECT CITY, LENGTH(CITY) 
    FROM STATION
    WHERE LENGTH(CITY)=(select min(LENGTH(CITY)) FROM STATION)
    ORDER BY CITY ASC LIMIT 1;
SELECT CITY, LENGTH(CITY) 
    FROM STATION
    WHERE LENGTH(CITY)=(select MAX(LENGTH(CITY)) FROM STATION)
    ORDER BY CITY ASC LIMIT 1;
```