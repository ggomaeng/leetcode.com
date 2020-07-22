Author @melangyun

Date : July 22, 2020

# Appempt 1

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
 
