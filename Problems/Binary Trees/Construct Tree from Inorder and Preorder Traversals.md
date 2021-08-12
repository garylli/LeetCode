## Problem Name: Construct Tree from Inorder and Preorder Traversals
### Difficulty: Medium
#### Date Completed: August 12th, 2021
#### Time Taken:  1:19:00
#### [Problem Link](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)

#### Thought Process:
1:00:00 I realzed fairly quickly that the inorder and preorder traversals collide at points where the preorder needs to change directions, but got stuck on implementing
the algorithm.

This problem was very hard without being able to draw anything out, so hopefully the next time I resume this problem I can draw it out and help visualize my thoughts.

1:22:00
Inorder traversals of the binary tree are LVR, meaning that any nodes to the left of the node will be before the index that contains the value of the node itself.
Any nodes to the right of the node will be after the index that contains the value of the node itself.

Preorder traversals of a binary tree are VLR, meaning that any nodes that are to the left of the current node are going to be before any nodes that are to the right of the current node. Also any nodes that are after the current node must be after the index containing the current node.

1:54:00
I keep thinking I know how to do it, but I'm having a hard time visualizing the coding algorithm like I usually would. For the next problem I'm going to immediately try to think of it from the system's point of view and see what questions need to be answered in order for it to find the next appropriate action. Hopefully this will make solving the next problem much faster.


1:19:00
So my initial idea was correct, and it was much easier on paper. However, the recursion still messed with me and I think I just need to continue to try thinking about it in terms of a machine's point of view.

Runtime was 5% - 30%
Space complexity was 99%
#### What I learned: 
