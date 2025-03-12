```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        '''
            two pointers, if both sides are alnum, compare them in lowercase, otherwise move them
        '''
        formatted = "".join(char.lower() for char in s if char.isalnum())

        l, r = 0, len(formatted)-1
        while l <= r:
            if formatted[l] == formatted[r]:
                l += 1
                r -= 1
            else:
                return False

        return True
```

Format the string accordingly
Use two pointers and a while loop
Compare elements