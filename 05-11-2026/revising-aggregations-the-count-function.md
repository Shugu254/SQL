## Revising Aggregations


Link: [Hackerrank](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem?isFullScreen=true)


Difficulty : EASY
DB Engine : MySQL

*********

## Intuition

 COUNT(*) → counts all rows that match the condition.
FROM CITY → looks at the CITY table.
WHERE population > 100000 → keeps only cities with a population greater than 100,000.
The result is the number of cities whose population exceeds 100,000.

## Solution

```SQL
SELECT COUNT (*)
FROM CITY 
WHERE population>100000;

```