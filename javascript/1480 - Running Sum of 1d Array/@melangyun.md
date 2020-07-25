Author @melangyun

Date : July 22, 2020

# Attempt 1

```javascript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var runningSum = function(nums) {
    let sum = 0;
    return nums.map(curVal => { 
        sum += curVal;
        return sum;
    });
};
```

Time complexity: O(N)

Space complexity: O(2N+1)
