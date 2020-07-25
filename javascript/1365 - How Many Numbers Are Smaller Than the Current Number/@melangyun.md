Author: @melangyun

Date: July 25, 2020

# Attempt 1

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var smallerNumbersThanCurrent = function(nums) {
    return nums.map(curVal => {
        let count = 0;
        for( let i = 0 ; i < nums.length ; i +=1 ){
            if(curVal > nums[i]){
                count += 1;
            }
        }
        return count;
    })
};
```

Time complexity: O(N^2)

Space complexity: O(2N)