## The report


Link: [Hackerrank](https://www.hackerrank.com/challenges/the-report/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
JOIN: Use BETWEEN to match each student's marks to the correct grade range (Min_Mark and Max_Mark).
CASE WHEN: Use a conditional statement to hide the names of students who scored a grade below 8 by displaying 'NULL'. For grades 8–10, display their actual names.
ORDER BY: Apply different sorting rules:
- Grade DESC – Arrange grades from highest to lowest.
- CASE WHEN Grade >= 8 THEN Name END ASC – For grades 8–10, arrange names alphabetically.
- CASE WHEN Grade < 8 THEN Marks END ASC – For grades 1–7, arrange marks from lowest to highest.
## Solution

```SQL
SELECT
CASE
WHEN G.Grade < 8 THEN 'NULL'
ELSE S.Name
END AS Name,
G.Grade,
S.Marks
FROM Students S
JOIN Grades G
ON S.Marks BETWEEN G.Min_Mark AND G.Max_Mark
ORDER BY
G.Grade DESC,
CASE WHEN G.Grade >= 8 THEN S.Name END ASC,
CASE WHEN G.Grade < 8 THEN S.Marks END ASC;

```