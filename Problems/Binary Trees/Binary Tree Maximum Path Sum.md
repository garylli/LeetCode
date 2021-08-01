## Problem Name: Binary Tree Maximum Path Sum
### Difficulty: Hard
#### Date Completed: August 1st, 2021.
#### Time Taken: 48:55
#### [Problem Link](https://leetcode.com/problems/binary-tree-maximum-path-sum/)

#### Thought Process:
First thought that comes to mind is that we're essentially dealing with netvalue of adding all the trees above the current sub tree. If the netvalue is positive, we continue up 
the tree. If not, we don't continue up the tree.

The problem with doing htis recurisvely with a postorder traversal is that the stack is built with the idea that all nodes should be included. That would lead to sums that
have a negative net value as no matter what the net value of going up the tree is, it will still traverse back up the function call stack.

So, I ended up just thinking about if it was feasible to sum up all of the values before and after the current path. I decdied taht there wasn't a feasible way since both depended on each other.
Thus, I began to simply include the reverse stack traversals as a part of the process. My final algorithm simply passed up an appropriate value assuming that the parent node was taken.

My ending runtime was between 36% and 15%. Space was 21.5%.

The 0.001% runtime did the exact same thing actually! It was just a simple difference between space allocation and me adding a lot of useless checks that were not needed.
#### What I learned: 
Runtime changes a lot based on small simple changes!
