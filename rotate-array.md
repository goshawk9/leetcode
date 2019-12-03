# Problem

Rotate Array

https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/646/

# solution

```
/**
 * @param {number[]} nums
 * @param {number} k
 * @return {void} Do not return anything, modify nums in-place instead.
 */
var rotate = function(nums, k) {
    const len = nums.length

    k %= len
    reverse(nums, 0, len-1)
    reverse(nums, 0, k-1)
    reverse(nums, k, len-1)

    return nums
};

function reverse(nums, start, end) {
    while(start < end) {
        let sum = nums[start] + nums[end]
        nums[start] = sum - nums[start]
        nums[end] = sum - nums[end]
        start ++
        end --
    }
}
```
