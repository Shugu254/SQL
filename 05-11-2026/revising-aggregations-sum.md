## Revising Aggregations - The Sum Function


Link: [Hackerrank](https://www.hackerrank.com/challenges/revising-aggregations-sum/problem?isFullScreen=true)


Difficulty : EASY
DB Engine : MySQL

*********

## Intuition
District = 'California' → keeps only California cities.
SUM(population) → totals their populations.
Returns the combined population of all cities in California.

## Solution

```SQL
SELECT sum(population)
From city
where District='California';

```