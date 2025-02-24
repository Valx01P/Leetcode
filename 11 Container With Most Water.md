```python
class Solution:
    def maxArea(self, height: List[int]) -> int:
        l, r, curr_area, max_area = 0, len(height)-1, 0, 0

        while l < r:
            
            curr_area = min(height[l],height[r]) * abs(l - r)
            max_area = max(max_area, curr_area)

            if height[l+1] > height[r-1]:
                l+=1
            else:
                r-=1
            
        return max_area
```

Maximizing Area using two pointers and variables
Keeping track of current and max values