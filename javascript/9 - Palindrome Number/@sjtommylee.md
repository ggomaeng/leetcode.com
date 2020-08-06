Author: @sjtommylee

Date: Aug 05, 2020


# Attempt 1

convert numbers into a string
return a new array nums with comma separated values 
iterate through the array nums, if the first / last element to be compared do not match, return false. 

```js
/**
 * @param {number} x
 * @return {boolean}
 */
var isPalindrome = function(x) {
    let num = x.toString();
    let nums = num.split('');

    for (let c of nums) {
        if (c != nums.pop()) {
            return false;
        }
    }
    return true;
};
```

Time complexity: O(N)

Space complexity: O(N)