## Problem Name: Unique Paths
### Difficulty: Medium
#### Date Completed: July 10th, 2021
#### Time Taken: 43:55.55
#### [Problem Link](https://leetcode.com/problems/unique-paths/)

#### Thought Process:
29:00 For the first 29 minutes, I've been trying to figure out how the branching works and how many new possibilities there would be for each movement to the right. Although this
information might be useful, it's taken way too long. I feel like the time spent up until now would've been more productive if I would've tried searching for the correct 
subproblem.

43:55 So the combinatorics solution did work, however I decided to try and find an appropriate subproblem for the dp solution. The subproblem that I ended up choosing was the 
number of unique paths to the square above the ending square and to the left of the ending square. This is because there is only one way to go from those squares to the ending
squares and no more unique paths will be generated. Therefore, we can reduce our problem of m x n to  (m - 1) x n + m x (n - 1) until the base case where it is simply 1.

#### What I learned:
The sub problem was not very clear this time, I simply found it by experimenting with numbers and found out that the paths could be broken down in such a manner.

I'll check through the solutions to see what explanations other people have on their process for finding the dp solution.
