Author: @ggomaeng

Date: July 30, 2020

# Attempt 1

Sweet and simple O(N) solution.

```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var findNumbers = function(nums) {
    return nums.reduce((acc, curr, i) => nums[i].toString().length % 2 === 0 ? acc + 1 : acc, 0);
};
```


Time complexity: O(N)

Space complexity: O(N)