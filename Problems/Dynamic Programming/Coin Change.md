## Problem Name: Coin Change
### Difficulty: Medium
#### Date Completed: July 2nd, 2021.

#### What I learned:
Trying to fnid the least number of coins needed in order to make up a certain amount--if that amount exists, that is.

If the amount is not divisible by the smallest coin denomination given, does that mean that we cannot give the right amount of change?
No. [5,17] = 17: 17 % 5 = 2

How would we go about representing this problem as a dynamic programming solution?
If we start with the smaller denominations of coins first, we can create a dynamic array representing the maxmimum number 
of coins used for each denomination.

For example, if we had [3,5,7] = 41, we'll never use more than 41/3 = 13 3-coins. Then, if we go onto 5, we know that we 
only subtract from 13.

This doesn't seem very helpful though.

