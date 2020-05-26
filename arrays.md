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
print('Hello world!')
```

## Two Sum

https://leetcode.com/problems/two-sum/

```python
def twoSum(self, nums: List[int], target: int) -> List[int]:
    data = sorted(enumerate(nums), key=lambda x: x[1])

    first = 0
    second = len(data) - 1
    while first != second:
        if data[first][1] + data[second][1] == target:
            return [data[first][0], data[second][0]]
        elif data[first][1] + data[second][1] < target:
            first += 1
        else:
            second -= 1
```
