# Problem

Single Number

https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/549/

# solution

> c = 2 \*(a + b + c) - (a + b + c)

```
/**
 * @param {number[]} nums
 * @return {number}
 */
var singleNumber = function(nums) {
    const unique = Array.from(new Set(nums))
    let sum1 = 0
    unique.forEach(i => {
        sum1 += parseInt(i)
    })
    let sum2 = 0
    nums.forEach(i => {
        sum2 += parseInt(i)
    })
    return 2 * sum1 - sum2
};
```

> a xor a = 0, a xor 0 = a

```
/**
 * @param {number[]} nums
 * @return {number}
 */
var singleNumber = function(nums) {
    let a = 0
    for (let i = 0; i < nums.length; i++) {
        a ^= nums[i]
    }
    return a
};
```
