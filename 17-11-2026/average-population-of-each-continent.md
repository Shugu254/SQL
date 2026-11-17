## Average Population of Each Continent


Link: [Hackerrank](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
JOIN: Connect CITY and COUNTRY to know which continent each city belongs to.
AVG(): Calculate the average population of cities.
CEILING(): Round the average UP to the nearest whole number.
GROUP BY: Calculate a separate average for each continent.
## Solution

```SQL
SELECT COUNTRY.CONTINENT, CEILING(AVG(CITY.POPULATION))
FROM CITY
JOIN COUNTRY
ON CITY.COUNTRYCODE = COUNTRY.CODE
GROUP BY COUNTRY.CONTINENT;

```