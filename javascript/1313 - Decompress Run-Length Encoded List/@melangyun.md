Author: @melangyun

Date July 30, 2020

# Attempt 1

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var decompressRLElist = function(nums) {
    const result = []
    for(let i = 0 ; i < nums.length ; i+=2 ){
        for(let j = 0 ; j < nums[i] ; j +=1 ){
            result.push(nums[i+1]);
        }
    }
    
    return result;
};
```



Time complexity: O(N^2)

Space complexity: O(2N)