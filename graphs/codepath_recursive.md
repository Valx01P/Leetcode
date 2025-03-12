```python
def count_suits_iterative(suits):
    seen = {}
    count = 0
    
    for suit in suits:
        if suit in seen:
            continue
        else:
            seen[suit] = 1
            count += 1
    return count
        
            

def count_suits_recursive(suits, seen={}, count=0):
    
    if not suits:
        return count
    
    if suits[0] in seen:
        return count_suits_recursive(suits[1:], seen, count)
    else:
        seen[suits[0]] = 1
        return count_suits_recursive(suits[1:], seen, count+1)
        
print(count_suits_iterative(["Mark I", "Mark II", "Mark III"]))
print(count_suits_recursive(["Mark I", "Mark IIII", "Mark I", "Mark III", "Mark IIII"]))
```




```python
def fibonacci_growth(n):
    
    if n <= 1:
        return n
    
    n_prev_one, n_prev_two = 1, 0
    
    for _ in range(n-1):
        curr = n_prev_one + n_prev_two
        n_prev_two = n_prev_one
        n_prev_one = curr
        
    return n_prev_one
    
print(fibonacci_growth(5))
print(fibonacci_growth(8))
```




```python
def reverse_scroll(scroll):
    if len(scroll) == 1:
        return scroll[0]
    
    return reverse_scroll(scroll[1:]) + scroll[0]
    
print(reverse_scroll("cigam"))
print(reverse_scroll("lleps"))
```