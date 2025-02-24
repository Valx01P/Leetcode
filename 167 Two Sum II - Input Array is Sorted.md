```python
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        l, r = 0, len(numbers)-1
        
        while l < r:
            current_sum = numbers[l] + numbers[r]

            if current_sum == target:
                return [l+1,r+1]
            elif current_sum > target:
                r -= 1
            else:
                l += 1
```

We are given a sorted array of numbers, we are trying
to find a number that is made of two values in the input
array, we can find them by using the two pointer approach
and increasing the left side to get a higher value, and decreasing the right side to get a lower value