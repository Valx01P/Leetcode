```python
class Solution:
    def fib(self, n: int) -> int:
        if n <= 1:
            return n

        prev1 = 0   # base case 1 for fib seq
        prev2 = 1   # base case 2 for fib seq

        # we know the first and second fib numbers as part
        # of the recurrence relation, so we start our computations
        # at the third fib number
        for i in range(2, n+1):
            curr = prev1 + prev2 # currently computed fib number from prev1 and prev2
            prev1 = prev2 # move the prev1 to the next in the imaginary fib values array
            prev2 = curr # move the prev2 to the next in the imaginary fib values array

        return prev2
```