## Problem Name: Binary Tree Level Order Traversal
### Difficulty: Medium
#### Date Completed: August 1st, 2021.
#### Time Taken:  42:49
#### [Problem Link](https://leetcode.com/problems/binary-tree-level-order-traversal/)

#### Thought Process:
So I first thought that the preorder traversal would yield a level order traversal.

Then, I moved onto the correct line of thinking that we could use a queue to retain the correct order of levels, but the hard part was figuring out how to keep track
of the number of nodes per level.

I ended up using a vector that would automatically expand to keep track of the number of nodes per level. Then, when the number of nodes on the current level was met, we would
push the current vector that was being built onto the solution vector.

38.8% - 80.61% Runtime
32% Space.
#### What I learned: 
