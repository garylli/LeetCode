## Problem Name: Lowest Common Ancestor of a Binary Search Tree
### Difficulty: Easy
#### Date Completed: August 12th, 2021.
#### Time Taken:  8:00.34
#### [Problem Link](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/)

#### Thought Process:
I used the idea of thinking about it from the computer's point of view and it helped me realize fairly quickly that, if we start from the root, the least common ancestor would either be at the root, the left, or the right.

When would it be at the root, on the left, or on the right?

The least common ancestor would be on the left if both p and q were less than the root's value.
The least common ancestor would be on the right if both p and q were greater than the root's value.
If neither of these were true, the root would be the least common ancestor.

#### What I learned: 
Thinking from the computer's point of view helps provide important questions that need to be answered and can speed up my thinking process.
