Author: @melangyun

Date: July 29, 2020

# Attempt 1

```js
/**
 * @param {string} s
 * @return {number}
 */
var balancedStringSplit = function(s) {
    let count = 0;
    for( let i = 0 ; i < s.length - 1 ; i +=1 ){
        const str = s[i] + s[i+1];
        if(str === "RL" || str == "LR" ){
            count++;
            i++;
        }
    }
    return count;
};
```


Time complexity: O(N)

Space complexity: O(N+1)