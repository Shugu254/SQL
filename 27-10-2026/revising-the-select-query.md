## Revising the Select Query I


Link: [Hackerrank](https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
I filter for cities in the USA with a population greater than 100,000, then return all their details 

## Solution

```SQL
SELECT *from CITY where COUNTRYCODE= 'USA' AND POPULATION> 100000;
```