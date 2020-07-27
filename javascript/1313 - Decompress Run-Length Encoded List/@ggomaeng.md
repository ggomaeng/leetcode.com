Author: @ggomaeng

Date: July 27, 2020

# Attempt 1

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var decompressRLElist = function(nums) {
    let result = [];
    for(let i = 0; i < nums.length; i += 2) {
        const freq = nums[i];
        const val = nums[i + 1];
        [...new Array(freq)].forEach(() => {
            result.push(val);
        })
    }

    return result;
};
```


Time complexity: O(N^2)

Space complexity: O(N)
