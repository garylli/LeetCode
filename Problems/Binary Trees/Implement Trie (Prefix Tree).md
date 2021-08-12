## Problem Name: Implement Trie (Prefix Tree)
### Difficulty: Medium
#### Date Completed: August 12th, 2021.
#### Time Taken:  58:25.56
#### [Problem Link](https://leetcode.com/problems/implement-trie-prefix-tree/)

#### Thought Process:
This problem was simply implementing a trie. It was fairly easy because I've already done this in the past in CSE100. However, I ran into some issues due to my relative lack of familiarity
with C++.

Mainly, the issue was initiating the character property to NULL instead of 0. This made it so I would implicitly convert the NULL constant into a character instead of simply
storing the null character.

Other than that it was pretty good. Took 58:25.56 minutes but the runtime complexity wasn't too bad

Runtime Complexity: 20.88 - 99.05%
Space Complexity: 98.44%

#### What I learned: 
When intializing a property to null in cpp, you can probably just use 0 to represent a null value rather than doing an implicit conversion between the null constant and that
data type.
