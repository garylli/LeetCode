## Problem Name: Word Break
### Difficulty: Medium
#### Date Completed: July 8th, 2021
#### Time Taken: 2:02:35
#### [Problem Link](https://leetcode.com/problems/word-break/)

#### Thought Process:
The problem asks us to see if a given string can be broken down into a combination of a specific set of words given to us. 

My first thought is to insert the words in wordDict into an MWT and check every time whether the word exists starting from the leftmost letter of the string to the rightmost.
However, this would have a fairly heavy overtime to construct the MWT, so I'm going to try and think of any other patterns that may optimize this process.

If the string is to be broken down into words, it must contain a word from left to right (aka starting from the first letter and reading right should yield a word, 
there can be no incompletes.)

6:52 How can this problem be broken up into DP?
We can think of a 2D dp array where the rows are the beginning index and the columns are the ending index of the substring. Within each square of the 2D array contains whether or
not that word is contained within wordDict. If the first column is all false, we return false. Otherwise, if the square is true, we use the column number + 1 as the next row to
check. If we can land on anything in the last column that's true, then the solution is true. Otherwise it's false.

13:00 After giving this a thought, I'm going to simply try using a modified MWT and see what the runtime is. It should be O(n * k) where k is length of wordDict.

25:00 After spending some time looking up string manipulation in cpp, I realized that simply searching left to rigth can work in the simplest of cases. However, if the wordDict is
tricky and contains words such as \[cat,cats\], simply finding the first word might not be enough.

57:44 I implemented the algorithm using recursion and it's too slow, but it should be a simple fix! Now it's just optimizing.
1:27:37 Okay maybe it isn't a simple fix. My algorithm is too inefficient when dealing with multiples of the same letter/repeated words. In order to solve this problem, I can 
either increase the speed at which the algorithm 

1:37:01 
#### What I learned:
