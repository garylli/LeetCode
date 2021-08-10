## Problem Name: Validate Binary Search Tree
### Difficulty: Medium
#### Date Completed: August 10th, 2021.
#### Time Taken: 18:09.95 
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

///////////////////////////////////////////////////////////////////////////////////
Okay so after trying this problem with a pen and paper (ipad), it was MUCH easier. I simply drew out which connections the child had to be less than and greater than, finding the pattern only took me a couple minutes. Here are the notes I had:


For a BST to be valid:
Any node in its right subtree must be larger than it.

Any nod ein its left subtree must be less than it.

When traversing to right child, the greaterThan is the parent while the lessThan is the parents lessThan. Vice versa for when traversing to the left child.


Solution:
Runtime: 59.75% - 98.58%
Memory: 58.37% - 99%

Solved exactly how it was explained above, tracking which made the subtree had to be greaterThan and which node the subree had to be lessThan.

Solution time:
18:09.95
#### What I learned: 
