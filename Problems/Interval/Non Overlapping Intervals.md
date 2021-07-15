## Problem Name: Non Overlapping Intervals
### Difficulty: Medium
#### Date Completed: July 13th, 2021
#### Time Taken: 2:17:21.63
#### [Problem Link](https://leetcode.com/problems/non-overlapping-intervals/)

#### Thought Process:
5:47.55 We want to return the minimum number of intervals we need to remove.
Thus, we can probably sort the intervals by interval size and insert in that order. This is because the least amount of overlapping intervals we'd have to remove would be the
n-largest overlapping intervals in the array. However, we run into a problem in tracking which intervals are already inserted.

I'm a bit tired of doing leetcode problems so I'm going to take a break and read some of the javascript guide but I'll come back to this later :).

2:17:21.63
So after the first hour, I had an already working solution except it was shrinking the intervals based on smaller size instead of based on ending index.

It took me an hour+ to figure out the optimal solution. Here's the thought process that led me to the answer:

First, I already knew we should sort the interval array. This yields us two advantages: 
We will be iterating through the intervals in terms of their beginning term. This means that the next interval in the array will always be the one that begins closest to the current interval. This is important because without this sorting, it's much harder to determine whether or not there are more intervals that the current interval overlaps.

If the next interval's beginning point is after the current interval's ending point, we know that the current interval overlaps no more intervals and we can continue on to checking the next interval.

At first, I knew that we should shrink the interval and keep track of the smallest current interval. However, this was wrong since we cannot simply shrink based on size. 
Consider [1,100],[3,196],[190,191],[191,192]. Our first interval has a size of 100 and the second interval has a size of less than 100. If we were just shrinking based on size, we would remove the first interval even though doing so actually *expands* our current interval. (it goes from ending at 100 to ending at 196).

Therefore, the *correct* way to shrink our intervals would be in a manner that does not open our current interval to further overlaps. This would be shrinking it based on ending index.

If we know the current interval ends at 100, if any future interval has an ending index <= 100, we can replace that as our current interval. This is because, 1) our array is sorted in order of increasing beginning index, so any future intervals will have a greater beginning index and therefore a smaller size and 2) because if the ending index is < 100, we can only get rid of overlaps by shrinking in that direction ([1,100] and [3,96] will overlap all the same up until 96 but [1,100] can only overlap more in the range of 96-100).

With this in mind, we have an algorithm for handling intervals that end earlier or at our current ending.

Now, we must take care of intervals that end later than our current ending.

Well, if the interval ends later than our current ending, we must simply check if we should remove the current interval or that interval. 
Then we have 3 cases: 
- nextBeg < currEnd < newEnd
- currEnd < nextBeg < newEnd
- currEnd < newEnd < nextbeg

The first case cannot be true since we know that our array is sorted in order of interval beginning. 
If the next beginning is **after the current end**** and **before the new end**, then it would make sense to remove the new interval as it overlaps an additional interval than the current one.
If the beginning is after the next end and current end, it might seem like it doesn't matter which one we remove, but it actually does matter.

See, the thing is, if the beginning is after the next end, that means that we can technically expand the current interval to the next one without increasing any number of overlaps. Therefore, we actually do not remove anything if the next beginning is after the newEnding. We simply expand the current interval to that interval and continue on. 

Therefore, we end up with some code like this:
```
#include <iostream>
class Solution {
public:
    int eraseOverlapIntervals(vector<vector<int>>& intervals) {
        sort(intervals.begin(), intervals.end());
        int currBeg = intervals[0][0];
        int currEnd = intervals[0][1];
        int index = 1;
        int removed = 0;
        
        for (index; index < intervals.size(); index++) {
            if (intervals[index][0] < currEnd) {
                if (intervals[index][1] <= currEnd) {
                    currBeg = intervals[index][0];
                    currEnd = intervals[index][1];
                    removed++;
                } else {
                    if (index + 1 >= intervals.size() || intervals[index+1][0] < intervals[index][1]) {
                        removed++;
                    }
                }
            } else {
                currEnd = intervals[index][1];
                currBeg = intervals[index][0];
            }
        } 
        return removed;
    }
};
```
#### What I learned: 
You need to think about what advantages sorting offers you and use it to your advantage when constructing your algorithms

