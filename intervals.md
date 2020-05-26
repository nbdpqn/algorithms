# Intervals

+ [Insert Interval](#insert-interval)
+ [Merge Intervals](#merge-intervals)
+ [Non-overlapping Intervals](#non-overlapping-intervals)

## Insert Interval

https://leetcode.com/problems/insert-interval/

```python
print('Hello world!')
```

## Merge Intervals

https://leetcode.com/problems/merge-intervals/

```python
print('Hello world!')
```

## Non-overlapping Intervals

https://leetcode.com/problems/non-overlapping-intervals/

```python
def eraseOverlapIntervals(self, intervals: List[List[int]]) -> int:
    if not intervals:
        return 0
    data = sorted(intervals, key=lambda x: x[1])
    right_endpoint = data[0][1]
    counter = 0
    for interval in data[1:]:
        if interval[0] < right_endpoint:
            counter += 1
        else:
            right_endpoint = interval[1]
    return counter
```
