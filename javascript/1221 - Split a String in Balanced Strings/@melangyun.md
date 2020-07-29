Author: @melangyun

Date: July 29, 2020

# Attempt 1

```js
/**
 * @param {string} s
 * @return {number}
 */
var balancedStringSplit = function(s) {
    let checker = 0;
    return [...s].reduce((acc,val) => {
        val === "L" ? checker++ : checker--;
        if(!checker) acc++;
        return acc;
    },0)
};
```


Time complexity: O(N)

Space complexity: O(N)