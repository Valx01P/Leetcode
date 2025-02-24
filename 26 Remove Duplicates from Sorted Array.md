```python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        write = 1

        for read in range(1, len(nums)):
            if nums[read] != nums[read-1]:
                nums[write] = nums[read]
                write += 1
        
        return write
```

It is critical to remember that the array is sorted,
so naturally, we can implement a simple algorithm
where we can assume the element will either be
the one we just went past, or a new one, and we
will never encounter the same element we went past
once we encounter a new one, so this algorithm of
a read and write pointer can work, it is critical
to remember as well that the first value will always
be unique, so both pointers can start at it, the
write pointer keeps track of where to place unique
values and we can return its value to determine the
total amount of unique values we had