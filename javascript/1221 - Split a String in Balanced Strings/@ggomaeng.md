Author: @ggomaeng

Date: July 27, 2020

# Attempt 1

Sweet and simple O(N) solution.

```js
/**
 * @param {string} s
 * @return {number}
 */
var balancedStringSplit = function(s) {
    let count = 0;
    let balance = 0;
    [...s].forEach(c => {
        c === "L"? balance-- : balance++;

        if(balance === 0) {
            count++;
        }
    })

    return count;
};
```


Time complexity: O(N)

Space complexity: O(N)