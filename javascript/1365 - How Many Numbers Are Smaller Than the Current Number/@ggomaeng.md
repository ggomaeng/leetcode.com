Author: @ggomaeng

Date: July 23, 2020

# Attempt 1

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var smallerNumbersThanCurrent = function(nums) {
    const sorted = [...nums].sort((a, b) => a - b);
    return nums.map(n => sorted.indexOf(n));
};
```

Time complexity: O(N)

Space complexity: O(2N)
