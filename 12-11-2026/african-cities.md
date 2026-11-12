## African Cities


Link: [Hackerrank](https://www.hackerrank.com/challenges/african-cities/problem?isFullScreen=true)


Difficulty : easy
DB Engine : MySQL

*********

## Intuition
JOIN connects CITY and COUNTRY using their matching country codes.
WHERE COUNTRY.CONTINENT = 'Africa' filters countries in Africa.
SELECT CITY.NAME returns the names of cities in those countries.

## Solution

```SQL
SELECT CITY.NAME
FROM CITY
JOIN COUNTRY
ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Africa';
```