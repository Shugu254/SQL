## Japan Population


Link: [Hackerrank](https://www.hackerrank.com/challenges/japan-population/problem?isFullScreen=true)


Difficulty : Easy
DB Engine : MySQL

*********

## Intuition
finding population for japan only
## Solution

```SQL
select sum(population)
from city
WHERE countrycode='JPN';

```