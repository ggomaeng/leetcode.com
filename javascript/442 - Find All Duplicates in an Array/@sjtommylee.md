Author: @sjtommylee

Date: Aug 18, 2020

# Attempt 1

Filter solution 


```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */


const findDuplicates =(nums) => {
    return nums.filter((a, b) => nums.indexOf(a) !== b)
}

```

Time complexity: O(N)
Space complexity: O(N)