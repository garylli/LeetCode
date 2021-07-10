## Problem Name: House Robber II
### Difficulty: Medium
#### Date Completed: July 8th, 2021
#### Time Taken: 
#### [Problem Link](https://leetcode.com/problems/house-robber-ii/)

#### Thought Process:
1.3 This problem is just like house robber: you're trying to find the maximum sum of an array with the idea in mind that you cannot pick adjacent houses. This time, however, the
array is circular. Therefore we must be careful about the first, second, and third index.

29:45:00 So, we know that the only difference between house robber II and house robber I is that the array is now circular. Thus, we get an issue when we add both the first and the last number of the array as that would result in an illegal robbery.

To counteract this, we must figure out how to account for only choosing one or the other to include in our robbery, if it's included at all.

This can easily be solved by checking whether the first index is used. If it is used, then we add the last - first. Otherwise, if the first house is not robbed, we can always just add the last one as normal.

1:07:00 okay this might not work LOL

#### What I learned:
Try to use DP for DP problems :)
