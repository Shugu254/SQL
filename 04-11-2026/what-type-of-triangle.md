## Type of Triangle


Link: [Hackerrank](https://www.hackerrank.com/challenges/what-type-of-triangle/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition

 Intuition:
 CASE checks the triangle sides in order: first confirms whether a triangle can be formed (A + B > C, A + C > B, B + C > A), then classifies it as Equilateral (all sides equal), Isosceles (any two sides equal), or Scalene (all sides different).

## Solution

```SQL
SELECT
    CASE
        WHEN A + B <= C OR A + C <= B OR B + C <= A THEN 'Not A Triangle'
        WHEN A = B AND B = C THEN 'Equilateral'
        WHEN A = B OR B = C OR A = C THEN 'Isosceles'
        ELSE 'Scalene'
    END
FROM TRIANGLES;

```