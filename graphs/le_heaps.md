```python
import heapq as h

n = []

h.heappush(n, -2)
h.heappush(n, -3)
h.heappush(n, -4)
h.heappush(n, -1)

print(-n[0])

x = [6, 4, 3, 8, 9]

h.heapify(x)

print(x)

h.heappop(x)

print(x)
```

```python
class Math:
    
    def __init__(self, num1, num2):
        self.x = num1
        self.y = num2
    
    def add(self):
        return self.x + self.y


yo = Math(2, 4)
print(yo.add())
```