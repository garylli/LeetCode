## Problem Name: Merge K Sorted Lists
### Difficulty: Medium
#### Date Completed: July 19th, 2021
#### Time Taken: 
#### [Problem Link](https://leetcode.com/problems/longest-substring-without-repeating-characters/)

#### Thought Process:
Post Read: After reading the problem, I think that the problem most likely is some form of dp.

The first possible solution that comes to mind is to simply track the longest substring until a number repeats and reset it to 1.
Every time before it resets while iterating through the string, we check if it's greater than the largest length up to that point.
If it is, we replace the longest with the new length and reset to 1.

Now, this probably works, but the hard part is identifying if the current character is a repeat in a timely fashion. Most likely, we
could simply use find every time.

No it doesn't work. We can't simply reset the length to 1 unless the repeating character is directly following the previous iteration
of that character.

19:13 Used a sliding window. 40% runtime with 10% space complexity.

This is because I had the program reallocate a new string every time using substring when it wasn't necessary.

#### What I learned: 
