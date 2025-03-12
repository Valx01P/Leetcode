```python

```


Conceptual Idea (Optimal Solution)
This problem can be solved optimally using the Sliding Window + Two Pointers technique.

Key Observations:
Expanding the Window: Use two pointers (left and right) to form a window that contains all characters of t.
Shrinking the Window: Once a valid window is found (i.e., it contains all characters from t), try to shrink it by moving the left pointer while still maintaining the valid condition.
Tracking Frequencies: Use a hashmap (Counter) to track the character counts in t and another hashmap to track the frequency of characters in the current window.
Plan (Step-by-Step)
Initialize Two Pointers:

left and right both start at index 0.
Maintain a frequency map t_freq for t (how many times each char appears).
Use another frequency map window_freq to track characters in our current window.
Use formed to track how many characters in window_freq meet the required frequency in t_freq.
Expand the right pointer to find a valid window:

Increase the frequency of the current character in window_freq.
If a character count matches in both window_freq and t_freq, increment formed.
Contract the left pointer to minimize the window while keeping it valid:

If all characters are still in the window, check if it's the smallest found so far.
Remove the leftmost character from window_freq and update formed if necessary.
Move left forward.
Continue until right reaches the end and return the smallest window found.

