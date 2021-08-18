## Problem Name: Find Median From Data Stream
### Difficulty: Hard
#### Date Completed: August 18th, 2021.
#### Time Taken:  42:06.14
#### [Problem Link](https://leetcode.com/problems/find-median-from-data-stream/submissions/)

#### Thought Process:
So I took the shitty draft approach again and started with the first idea that came to midn.

The firs thting I thought of when maintaining a median is adding the new numbers into a priority queue and simply finding the middle of the priority queue every time when
we needed the median.

However, it turns out that we can't access the elements of a priority queue by index.

Thus, to work around it, I decided to just keep a minheap and a maxheap (one side stores the numbers higher than the median, and the other side stores numbers lower than the 
current median).

Now, inserts are just done with balancing in mind and we just check if the sizes are equal to see if it's even. If it is, we return the midpoint of both the maxheap and minheap top.
If not, we make sure that the median lies on the maxheap.

Runtime: 308ms - 264ms (23% - 40%)
Spacetime: 6%
#### What I learned: 
You can't access priority queues by index in cpp.
Also that the shitty draft approach has been working fairly well!
