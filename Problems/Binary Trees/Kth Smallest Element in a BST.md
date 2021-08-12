## Problem Name: Kth Smallest Element in a BST
### Difficulty: Medium
#### Date Completed: August 12th, 2021.
#### Time Taken:  16:35.06
#### [Problem Link](https://leetcode.com/problems/kth-smallest-element-in-a-bst/submissions/)

#### Thought Process:
I thought about it from the computer's point of view again and it helped speed it up a lot! So for the computer, we start from the root and we need to find out where to stop
our traversal. However, that's kind of annoying because we don't know how many nodes are less than the current node we're at so we don't know if we need to keep going to the
left or not.

The question that arose was How many nodes are less than the current node?

Well we can find that out using a helper function to provide the computer that information.

If we run nodesSmaller on the root node, we know that every node ot the left is going to be smaller than the current node and every nod eon the right has the current node + all the nodes on the left that are smaller than it.

Thus we can simply sum it in a way that follows this form of thinking.

Runtime Complexity: 9% - 95.66%
Space Complexity: 33.51%
#### What I learned: 
