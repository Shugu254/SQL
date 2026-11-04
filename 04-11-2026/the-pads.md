## the-pads


Link: [Hackerrank](https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition

 SUBSTR(OCCUPATION,1,1) gets the occupation's first letter and combines it with the name as Name(O), while GROUP BY OCCUPATION and COUNT(*) count people in each occupation and display the totals, sorted first by count and then alphabetically.

## Solution

```SQL
SELECT NAME || '(' || SUBSTR(OCCUPATION, 1, 1) || ')'
FROM OCCUPATIONS
ORDER BY NAME;

SELECT 'There are a total of ' || COUNT(*) || ' ' ||
       LOWER(OCCUPATION) || 's.'
FROM OCCUPATIONS
GROUP BY OCCUPATION
ORDER BY COUNT(*), OCCUPATION;
```