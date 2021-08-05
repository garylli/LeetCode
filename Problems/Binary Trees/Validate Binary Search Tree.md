## Problem Name: Validate Binary Search Tree
### Difficulty: Medium
#### Date Completed: 
#### Time Taken:  
#### [Problem Link](https://leetcode.com/problems/validate-binary-search-tree/)

#### Thought Process:
Can't we just iterate thorugh the tree and check if the left child's value is smaller than the current node's value, and whether or not
the right child's value is greater than the current node's value?

Nope I forgot that the tree hierachy transfers past the parent node. A node must be larger than any node it is on the right subtree of
and must be smaller than any node it is on the left subtree of.

52:46
Every time we go right on a tree, we're setting new restrictions on the right 

1:10:00
We could try a post order traversal where we update min and max of each traversal and check if the min on the right is greater than curr->val
and if max on the left is less than curr->val

#### What I learned: 
