# Intervals

+ [Insert Interval](#insert-interval)
+ [Merge Intervals](#merge-intervals)
+ [Non-overlapping Intervals](#non-overlapping-intervals)

## Insert Interval

https://leetcode.com/problems/insert-interval/

```python
def insert(self, intervals: List[List[int]], newInterval: List[int]) -> List[List[int]]:
    data = sorted(intervals + [newInterval], key=lambda x: x[0])
    result = list()
    for interval in data:
        if not result or result[-1][1] < interval[0]:
            result.append(interval)
        else:
            result[-1][1] = max(result[-1][1], interval[1])
    return result
```

## Merge Intervals

https://leetcode.com/problems/merge-intervals/

```python
print('Hello world!')
```

## Non-overlapping Intervals

https://leetcode.com/problems/non-overlapping-intervals/

```python
print('Hello world!')
```
