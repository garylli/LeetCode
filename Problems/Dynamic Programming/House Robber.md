## Problem Name: House Robber
### Difficulty: Medium
#### Date Completed: July 8th, 2021
#### Time Taken: 56:11.95
#### [Problem Link](https://leetcode.com/problems/house-robber/)

#### Thought Process:
This problem asks us to find the maximum possible sum of an array if we cannot choose two adjacent numbers. This problem seems fairly simple at first glance. It seems as if
it's a simple matter of finding the maximum net gain at each index of the array. This can be calculated by choosing the move that maximizes the largest profit.

56:11.95 It wasn't as simple as I thought HAHA. I keep thinking that there's a way to do these DP problems without actually doing DP but it keeps slowing me down. My first attempt
was to create an array to calculate net gain at each index and what the best move was, but I realized that such an approach would run into many issues with repeated consecutive 
numbers, etc. Thus, I decided to take some time to think of a DP approach and came up with the solution I submitted.

The solution was to simply create a dp array that contains the max value at each point. This is possible because when the robber robs a house, it's next robbery is either 2 or 3 
houses from the last one it's robbed. Thus, we can do the same thing except building off of previous robberies and always choosing the maximum value combination in hindsight.

#### What I learned:
Try to use DP for DP problems :)
