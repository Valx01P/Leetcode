```Python
class Solution:
    def removeElement(self, nums: List[int], val: int) -> int:
        write = 0

        for read in range(0, len(nums)):
            
            if nums[read] != val:
                nums[write], nums[read] = nums[read], nums[write]
                write += 1
                
        return write 
```

This problem is very similar to leetcode 283 and 26
and involve moving all the values to be removed to the
far right of the array, however that is not necessary as
you can just do it like this as well, where you don't swap,
just overwrite

```python
class Solution:
    def removeElement(self, nums: List[int], val: int) -> int:
        write = 0

        for read in range(0, len(nums)):
            
            if nums[read] != val:
                nums[write] = nums[read]
                write += 1

        return write 
```