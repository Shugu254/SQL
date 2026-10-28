## Revising the Select Query 2


Link: [Hackerrank](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
I filter for cities in the USA with a population greater than 120,000 and return only the city names.

## Solution

```SQL
SELECT NAME from CITY WHERE COUNTRYCODE= 'USA' and POPULATION > 120000;
```