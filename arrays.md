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
print('Hello world!')
```
