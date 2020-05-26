# Arrays

+ [Subarray Sum Equals K](#subarray-sum-equals-k)
+ [3Sum](#3sum)
+ [Two Sum](#two-sum)

## Subarray Sum Equals K

https://leetcode.com/problems/subarray-sum-equals-k/

```python
print('Hello world!')
```

## 3Sum

https://leetcode.com/problems/3sum/

```python
from itertools import count


def threeSum(self, nums: List[int]) -> List[List[int]]:
    data = sorted(nums)
    result = list()
    for first in range(len(data) - 2):
        if first > 0 and nums[first] == data[first - 1]:
            continue
        second = first + 1
        third = len(data) - 1
        while second < third:
            total_sum = data[first] + data[second] + data[third]
            if total_sum < 0:
                second += 1
            elif total_sum > 0:
                third -= 1
            else:
                result.append([data[first], data[second], data[third]])
                while second < third and data[second] == data[second + 1]:
                    second += 1
                while third > second and data[third] == data[third - 1]:
                    third -= 1
                second += 1
                third -= 1
    return result
```

## Two Sum

https://leetcode.com/problems/two-sum/

```python
print('Hello world!')
```
