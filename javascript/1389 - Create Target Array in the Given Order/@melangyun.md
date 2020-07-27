Author: @melangyun

Date : July 28, 2020

# Attempt 1

reArrange Array

```js
/**
 * @param {number[]} nums
 * @param {number[]} index
 * @return {number[]}
 */
var createTargetArray = function(nums, index) {
    
    const returnArr = new Array(nums.length);
    
    for(let i = 0 ; i < nums.length ; i += 1){
        const pointer = index[i];
        if(returnArr[pointer] !== undefined){
            returnArr.pop();
            returnArr.splice(pointer,0,nums[i]);
         }else{
             returnArr.splice(pointer,1,nums[i]);
         }
    }
    
    return returnArr;
};
```

Time complexity: O(N^2)

Space complexity: O(2N)