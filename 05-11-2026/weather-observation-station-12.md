## Weather Observation Station 12


Link: [Hackerrank](https://www.hackerrank.com/challenges/weather-observation-station-12/problem?isFullScreen=true)


Difficulty : EASY
DB Engine : MySQL

*********

## Intuition

 LOWER(CITY) → converts the city name to lowercase so the check is case-insensitive.
LEFT(...,1) → gets the first letter of the city.
NOT IN ('a','e','i','o','u') → ensures the first letter is not a vowel.
RIGHT(...,1) → gets the last letter of the city.
Another NOT IN ('a','e','i','o','u') → ensures the last letter is not a vowel.
AND → both conditions must be true, meaning the city neither starts nor ends with a vowel.
DISTINCT → removes duplicate city names from the result. 
## Solution

```SQL
SELECT distinct city
FROM station 
where left(lower(city),1) not in ('a', 'e', 'i', 'o', 'u') and right(lower(city),1) not in ('a', 'e', 'i', 'o', 'u');

```