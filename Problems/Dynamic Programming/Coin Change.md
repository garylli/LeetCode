## Problem Name: Coin Change
### Difficulty: Medium
#### Date Completed: July 3rd, 2021
#### Time Taken: 2:32:xx
#### [Problem Link](https://leetcode.com/problems/coin-change/)

#### What I learned:
This problem was the first DP problem I've really attempted. It took me 2 and a half hours since I kept dismissing solutions I felt would not run quick enough. 

I've still not drilled it into my mind that I should find an algorithm that works first and then worry about runtimes later. For example, the solution to this problem required
a dp array where each index would require (amount) comparisons.

I actually thought of this idea and immediately dismissed it thinking that it was too slow. However, after thinking about other ways to optimize the solution for 2 hours, I
eventually gave up and decided to try submitting the orginal solution to see if it would work.

It did and it was actually pretty quick. Even with all those comparisons, it was still techincally O(n) and beat 80+% of other submissions.

Note to self: You dismiss a lot of algorithms under the premise that they are too slow when in reality they are not. Runtimes are not always as they seem 
