## Binary Tree Nodes


Link: [Hackerrank](https://www.hackerrank.com/challenges/binary-search-tree-1/problem?isFullScreen=true)


Difficulty : medium
DB Engine : MySQL

*********

## Intuition
P IS NULL: No parent → Root.
N IN (SELECT P FROM BST): If the node appears in the parent column, it has children → Inner.
ELSE: If neither condition applies → Leaf.
ORDER BY N: Arrange nodes from smallest to largest.
## Solution

```SQL
SELECT N,
CASE
WHEN P IS NULL THEN 'Root'
WHEN N IN (SELECT P FROM BST) THEN 'Inner'
ELSE 'Leaf'
END
FROM BST
ORDER BY N;

```