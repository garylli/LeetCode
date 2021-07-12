## Problem Name: Longest Consecutive Sequence
### Difficulty: Medium
#### Date Completed: July 11th, 2021
#### Time Taken: ~30min
#### [Problem Link](https://leetcode.com/problems/longest-consecutive-sequence/)

#### Thought Process:
Since we're looking to find the length of the longest consecutive subsequence, we know that every new number that we find can either
border 0, 1 or 2 pre-existing numbers.

Thus, if we're going to insert a new number, we have to update the value depending on how many pre-existing numbers it borders.
If, for example, we're inserting a number that borders two already inserted numbers, the new length of the longest consecutive
sequence would be LCS[new - 1] + 1 + LCS[new + 1]. However, this relies on the fact that the length of the neighboring consecutive
sequences are stored on the edges of said sequences.

Therefore, to optimize it, I simply would set the edge numbers of the longest consecutive sequence every time the length of said
sequence changed.

#### What I learned: 
~50% Runtime complexity. Not horrid, but not great.
