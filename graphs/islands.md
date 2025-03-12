```python
x = [
    [1,0,1,0,1],
    [1,1,1,0,0],
    [0,0,0,1,1],
    [1,0,1,0,1],
]

# output should be 3 islands

def totalIslands(grid):
    
    rows, cols = len(grid), len(grid[0])
    total_islands = 0
    
    def sinkIsland(row, col):
        
        if row < 0 or row >= rows or col < 0 or col >= cols or grid[row][col] == 0:
            return
        
        grid[row][col] = 0

        sinkIsland(row - 1, col) # top
        sinkIsland(row - 1, col + 1) # top-right
        sinkIsland(row, col + 1) # right
        sinkIsland(row + 1, col + 1) # bottom-right
        sinkIsland(row + 1, col) # bottom
        sinkIsland(row + 1, col - 1) # bottom-left
        sinkIsland(row, col - 1) # left
        sinkIsland(row - 1, col - 1) # top-left


    for row in range(0, rows):
        for col in range(0, cols):
            
            if grid[row][col] == 1:
                total_islands += 1
                sinkIsland(row, col)
                
    return total_islands

print(totalIslands(x))
```

Uses dfs to search through possible islands