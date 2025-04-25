```js
 
/**
 * @param {number[]} nums
 * @return {number}
 */
function removeDuplicates(nums) {
    let l = 0
    for (let r = 1; r < nums.length; r++) {
        if (nums[l] !== nums[r]) {
            l += 1
            nums[l] = nums[r]
        }
    }
    return l + 1
}

// [1, 1, 2, 2, 3]
// [1, 2, 3, 4]
```