Author: @melangyun

Date July 30, 2020

# Attempt 1

자릿수가 2의 배수일 경우에만 카운트한다.

```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var findNumbers = function(nums) {
    return nums.reduce((acc,val)=>{
        if(`${val}`.length % 2 === 0) acc++;
        return acc;
    },0)
};
```



Time complexity: O(N)

Space complexity: O(1)