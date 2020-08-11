Author: @melangyun

Date : Aug 11, 2020

# Attempt 1

create descending array and multiply array[0] and array[1]

```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var maxProduct = function(nums) {
    const sortedArr = nums.sort((a,b)=> b-a);
    return (sortedArr[0]-1) * (sortedArr[1]-1);
};
```

Time complexity: O(N)

Space complexity: O(N)
