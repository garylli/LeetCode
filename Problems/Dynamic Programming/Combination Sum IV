## Problem Name: Combination Sum IV
### Difficulty: Medium
#### Date Completed: July 8th, 2021
#### Time Taken: 26:17.77
#### [Problem Link](https://leetcode.com/problems/combination-sum-iv/)

#### Thought Process:
This problem asks us to find how many combinations of int[] nums can be used to form int target.

This immediately reminded me of the coin change solution that I did a couple days ago where the sub problem is finding the maximum number of combinations of nums that can be used
to form any number from 0 to target.

The reasoning behind this is because when we're trying to find all possible sums up to a certain number using a pre-determined array of numbers, we know that any correct 
combination must contain only numbers from said array.

With that in mind, we can simply choose a number from the array as our first number in the permutation.
For example, if the current number is 30, and we're given [10, 20], we can choose 10 as our first number and find how many ways we can form 20 using [10,20]. The total number
of sums to hit 30 is simply the sum of all these possible permutations.

So for our algorithm, we get dp[curr] = Sum of dp[curr - nums[i]].

#### What I learned:
Doing DP problems really helps you come up with solutions to future problems that are similar in nature.

This was a super quick problem simply because I've done the coin change problem before.
