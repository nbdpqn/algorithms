# Arrays

+ [Subarray Sum Equals K](#subarray-sum-equals-k)
+ [3Sum](#3sum)
+ [Two Sum](#two-sum)

## Subarray Sum Equals K

https://leetcode.com/problems/subarray-sum-equals-k/

```python
def subarraySum(self, nums: List[int], k: int) -> int:
    counter = 0
    total_sum = 0
    d = {0: 1}
    for num in nums:
        total_sum += num
        if total_sum - k in d.keys():
            counter += d.get(total_sum - k)
        d.update({total_sum: d.setdefault(total_sum, 0) + 1})
    return counter
```

## 3Sum

https://leetcode.com/problems/3sum/

```python
print('Hello world!')
```

## Two Sum

https://leetcode.com/problems/two-sum/

```python
def twoSum(self, nums: List[int], target: int) -> List[int]:
    sorted_nums = sorted(enumerate(nums), key=lambda x: x[1])

    first = 0
    second = len(sorted_nums) - 1
    while first != second:
        if sorted_nums[first][1] + sorted_nums[second][1] == target:
            return [sorted_nums[first][0], sorted_nums[second][0]]
        elif sorted_nums[first][1] + sorted_nums[second][1] < target:
            first += 1
        else:
            second -= 1
```
