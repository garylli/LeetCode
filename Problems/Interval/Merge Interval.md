## Problem Name: Merge Interval
### Difficulty: Medium
#### Date Completed: July 12th, 2021
#### Time Taken: 17:08.69, (98% | 95%)
#### [Problem Link](https://leetcode.com/problems/merge-intervals/)

#### Thought Process:
With merge interval, we're doing the same thing as the last problem, except we simply need to merge the already overlapping intervals.

After I finished Insert Interval, I looked at the discussions and it was simple to come up with a merging algorithm after reading up on them.

For my merging algorithm, I simply kept track of the new interval to be inserted and checked if the beginning of the new interval was less than the end of the current interval or 
if the ending of the new interval was greater than or equal to the beginning of the current interval. If it was, I would update newInterval to have start = min(start,curr[0]) and
end = max(start,curr[1]).

Otherwise, I'd insert the new interval and create a "new" new interval by resetting start and end to the current interval's.


#### What I learned: 
Intervals come pretty naturally to me so far!
