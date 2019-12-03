# Problem

Contains Duplicates

https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/578/

# solution

```
/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
    const unique = Array.from(new Set(nums))
    if (nums.length !== unique.length)
        return true
    return false
};
```
