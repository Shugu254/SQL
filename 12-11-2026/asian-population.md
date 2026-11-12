## Population Census


Link: [Hackerrank]https://www.hackerrank.com/challenges/asian-population/problem?isFullScreen=true


Difficulty : easy
DB Engine : MySQL

*********

## Intuition
JOIN connects the CITY and COUNTRY tables using their matching country codes.
WHERE filters countries belonging to Asia.
SUM(CITY.POPULATION) adds up the populations of all cities in those Asian countries.

## Solution

```SQL
SELECT SUM(CITY.POPULATION)
FROM CITY
JOIN COUNTRY
ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Asia';

```