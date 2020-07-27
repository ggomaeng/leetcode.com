Author @melangyun

Date : July 27, 2020

# Attempt 1



```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var findDisappearedNumbers = function(nums) {
    const checkObj = {};
    const numberingArr = [];
    for(let i = 0 ; i < nums.length ; i+=1 ){
        if(!checkObj[nums[i]]){
            checkObj[nums[i]] = 1;
        }
        numberingArr.push(i+1);
    }
    
    return numberingArr.reduce((acc, curVal) => {
        if(!checkObj[curVal]){
            acc.push(curVal);
        }
        return acc;
    },[]) 
};

```

Time complexity : O(N)

Space complexity : O(2N + 1)