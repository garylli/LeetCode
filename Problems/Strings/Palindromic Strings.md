## Problem Name: Palindromic Substrings
### Difficulty: Medium
#### Date Completed: 
#### Time Taken: 
#### [Problem Link](https://leetcode.com/problems/palindromic-substrings/)

#### Thought Process:
12:10
The problem I'm facing is how to actually find the center of a palindromic substring.

abbcdde racecar abaddca

So my original line of thought involved expanding backward from one end to the start, but that isn't very helpful with finding all the possible palindromes as we won't know which
way to expand.

So the way that we could search is find when s[i] == s[i-1] or s[i] == s[i-2]. The problem is that this would get stuck on strings that are all the same.
For example, aaaaaaaa, we would get way too many "centers" of the palindromes. Thus, what we could do is repeatedly go until there are no further palindromes. However this poses
the issue of telling where the actual center of the palindromes are.

Let's go with the first idea that comes to mind and searches through all the palindromes and checks if they are valid. If they aren't, we search the next, and so on.
abbaaaaa
adddaccbbaadaa
racecar
40:00
So my approach that I had down at 12 minutes could work if I don't try and make a stack of palindromic centers but instead expand at every center
as we encounter them

What really helped with making this decision was thinking as if I was the computer, only reading in one letter at a time and trying to determine when there
was a palindrome only with that information. 
7 + 1 + 1 + 1 + 1

48:52

1:20:00
My initial line of thought was practically correct. You have to count the palindromes as they come, but you also need to count both the s[i] == s[i-1] case and s[i] == s[i-2] cases.

I looked at the answers for this one as I was taking too long so I'll have to revisit this problem.

#### What I learned: 
However, although I looked at the answers for this problem, I learned a way of thinking that I think I've used int he past but proved extremely helpful for forming an algorithm.
This is thinking as if you were the machine, something I was also told to do in CSE140. This helps you really visualize what you have to do step by step with variable inputs.
