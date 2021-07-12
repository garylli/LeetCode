## Problem Name: Insert Interval
### Difficulty: Medium
#### Date Completed: July 12th, 2021
#### Time Taken: 25:59.76
#### [Problem Link](https://leetcode.com/problems/pacific-atlantic-water-flow/)

#### Thought Process:
Right away, you know that when you're inserting an interval, the first number of the interval should be greater than the second
number of the previous interval. Therefore, we can start our search by finding where the first nubmer of our interval is less than 
the second number of an interval within the given array.

A [better explanation](https://leetcode.com/problems/insert-interval/discuss/21669/Easy-and-clean-O(n)-C%2B%2B-solution) for the algorithm is:
put all intervals that come before the new interval.
merge all intervals that overlap with the given interval
put all intervals that come after the given interval.


#### What I learned: 
Data structures matter! Maybe for DP problems you didn't have to worry about them, but now you do.
