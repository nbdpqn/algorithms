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
    sorted_nums = sorted(nums)
    result = list()
    for first in range(len(sorted_nums) - 2):
        if first > 0 and sorted_nums[first] == sorted_nums[first - 1]:
            continue
        second = first + 1
        third = len(sorted_nums) - 1
        while second < third:
            total_sum = sorted_nums[first] + sorted_nums[second] + sorted_nums[third]
            if total_sum < 0:
                second += 1
            elif total_sum > 0:
                third -= 1
            else:
                result.append([sorted_nums[first], sorted_nums[second], sorted_nums[third]])
                while second < third and sorted_nums[second] == sorted_nums[second + 1]:
                    second += 1
                while third > second and sorted_nums[third] == sorted_nums[third - 1]:
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
