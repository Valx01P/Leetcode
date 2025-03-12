```python
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        write = 0

        for read in range(0, len(nums)):

            if nums[read] != 0:
                nums[write], nums[read] = nums[read], nums[write]
                write += 1
                
        return nums
```

You will be swapping zeroes with numbers you encounter
to push them to the right, we will have a write pointer
to store the spot where the next non-zero number will go