## Problem Name: Decode Ways
### Difficulty: Medium
#### Date Completed: July 10th, 2021
#### Time Taken: 54:34.89
#### [Problem Link](https://leetcode.com/problems/decode-ways/)

#### Thought Process:
5:03 One possible subproblem is how many ways the substring up to the current index can be formed.

54:34.89 So, the subproblem I originally came up with was actually correct. The reason why this problem took so long was because 
I was doing comparisons of characters and numbers instead of the ascii value of the numbers.

The final algorithm I came up with was simply checking if the current number could combine to form a number. If so, it would add the
way to make the substring up to the current index with the ways to make the substring up to the index behind the current one as 
the letter can either be the single digit number or double digit number. Thus, you'd have to add how many ways you can make the 
substring before the single digit number and before the double digit number.

#### What I learned:
This was fairly easy! If I can find the correct sub problem from the start, I don't have to worry too much about much else other
than checking my code.

Note to self: Sometimes the issue isn't the algorithm! If you've gone through multiple trials of your algorithm and it seems to be
working, try checking your code from time to time!
