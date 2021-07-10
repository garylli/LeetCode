## Problem Name: Jump Game
### Difficulty: Medium
#### Date Completed: July 10th, 2021
#### Time Taken: 8:13.83
#### [Problem Link](https://leetcode.com/problems/jump-game/)

#### Thought Process:
2:00 If each index of the array represents the max jump height, then that means you can jump to any index <= the current value away
from the current index. Since we're trying to jump as far as possible, we would only jump to an array if its subsequent jump height
is greater than the number of indices it is away from our current index.

For example, if our current index allows us to jump 5 squares, and in the index after the one we're currently on allows us to jump
3 squares, we would not take it since it takes 1 to reach that square, but we could still jump 4. Since 4 > 3, we would continue onto
the next square.

5:00 starting algorithm writing.

8:13.83 Finished.

#### What I learned:
Subproblems are problems that lead up to the solution of the problem we're solving.
