## Higher Than 75 Marks


Link: [Hackerrank](https://www.hackerrank.com/challenges/more-than-75-marks/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
MARKS > 75 → filters students who scored more than 75 marks.
RIGHT(NAME, 3) → extracts the last 3 characters of each student's name for sorting.
ID ASC → if multiple names have the same last 3 characters, sort those students by ascending ID.

## Solution

```SQL
SELECT NAME
From STUDENTS
WHERE marks>75
ORDER BY RIGHT(NAME, 3), ID ASC;
```