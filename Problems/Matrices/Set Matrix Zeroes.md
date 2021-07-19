## Problem Name: Set Matrix Zeroes
### Difficulty: Medium
#### Date Completed: July 15th, 2021
#### Time Taken: 
#### [Problem Link](https://leetcode.com/problems/non-overlapping-intervals/)

#### Thought Process:
4:25.63 I simply did it in O(m + n), using a map to track zeroes for rows and a map to track zeroes for columns.

However, there was a way to do it in O(1), which required using the matrix and the first index in each row/column to check if that row should be filled with zeroes or not.

#### What I learned: 
