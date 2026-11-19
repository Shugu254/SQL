## Contest Leaderboard


Link: [Hackerrank](https://www.hackerrank.com/challenges/contest-leaderboard/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
Subquery (MAX): Find the highest score each hacker achieved in each challenge.
GROUP BY (inside): Group submissions by hacker_id and challenge_id so we get one highest score per challenge.
JOIN: Connect the results to the Hackers table to get the hackers' names.
SUM(): Add each hacker's highest scores across all challenges to get their total score.
GROUP BY (outside): Group results by hacker ID and name to calculate one total score per hacker.
HAVING: Exclude hackers whose total score is zero.
ORDER BY: Sort by total score (highest first), then hacker ID (smallest first).
## Solution

```SQL
SELECT HT.hacker_id,HT.name,SUM(ST.max_score) AS total_score
FROM Hackers HT
JOIN (SELECT hacker_id, challenge_id, MAX(score) AS max_score
FROM Submissions
GROUP BY hacker_id, challenge_id) ST
ON HT.hacker_id = ST.hacker_id
GROUP BY HT.hacker_id, HT.name
HAVING total_score > 0
ORDER BY total_score DESC, HT.hacker_id ASC;

```