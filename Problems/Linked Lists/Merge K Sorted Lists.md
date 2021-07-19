## Problem Name: Merge K Sorted Lists
### Difficulty: Hard
#### Date Completed: July 18th, 2021
#### Time Taken: 
#### [Problem Link](https://leetcode.com/problems/merge-k-sorted-lists/)

#### Thought Process:
Post Read: Immediately, the first solution I think of is merging 2 lists at a time until we've merged all of the lists in sorted order.
However, this definitely does not seem like the most optimized approach, so I'll be attempting to come up with a more optimized approach.

So, with a cursory glance, we can see that the biggest problem is keeping track of the current index to track for each of the linked lists.
We could make n comparisons with each of the link lists to check which one is the smallest and add them.

First off, the easiest way to optimize the simple approach would to decrease the number of merges by a factor of 2 by pairing up the original lists to merge
before remerging already merged lists. This way we won't be merging all of them into one super long list, but instead into log2(lists).

#### What I learned: 
