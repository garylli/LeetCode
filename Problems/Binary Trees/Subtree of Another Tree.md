## Problem Name: Subtree of Another Tree
### Difficulty: Easy
#### Date Completed: August 1st, 2021.
#### Time Taken:  43:48
#### [Problem Link](https://leetcode.com/problems/subtree-of-another-tree/)

#### Thought Process:
Honestly I was getting really tired at this point. It took me forever to realize that what I was doing was propagating the modified subroots down.

My initial thought was just to check if the current value matched the subroot value. If it did, we could simply check it the subtrees of the subroot were subtrees of the current root.
However, simply doing it this way would be finding if they were _subtrees_ of the current root. This means that we could skip values. However, in reality we should've been checking
whether or not the left and right were true matches to the subroot left and right.

In the end, I did a preorder traversal where I first checked if the root value was equal to subroot value. If it was, I checked if the child trees matched. if not, we simply
recall the function on the root's left and right child.

Runtime: 35.95% - 98.55%
Space: 24% -81%
#### What I learned: 
