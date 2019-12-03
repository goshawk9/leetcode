# Problem

Best Time to Buy and Sell Stock II

https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/564/

# solution

```
/**
 * @param {number[]} prices
 * @return {number}
 */
var maxProfit = function(prices) {
    let maxProfit = 0
    for(let i = 1; i < prices.length; i ++) {
        if (prices[i] > prices[i - 1]) {
            maxProfit += prices[i] - prices[i - 1]
        }
    }
    return maxProfit
};
```
