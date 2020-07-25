Author @melangyun

Date : July 22, 2020

# Appempt 1

```javascript
/**
 * @param {number[]} nums
 * @param {number} n
 * @return {number[]}
 */

var shuffle = function(nums, n) {
    const result = [];
    let isOdd = true;
    
    for (let i = 0 ; result.length < nums.length ; ) {
        result.push(nums[i]);
        isOdd ? i += n : i = i - n + 1 ;
        isOdd = !isOdd;
    }
    
    return result;
};
```

Time complexity: O(N)

Space complexity: O(2N + 1)
 
