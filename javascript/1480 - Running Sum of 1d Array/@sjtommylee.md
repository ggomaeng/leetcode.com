Author: @sjtommylee

Date: Aug 09, 2020

# Attempt 1

Mapping solution. 


```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
const runningSum = (nums) => {
    let total = 0;
    return nums.map((x) => (total += x));
}
```

Time complexity: O(N)

Space complexity: O(N)
