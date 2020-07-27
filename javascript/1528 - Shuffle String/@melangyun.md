Author: @melangyun

Date: July 27, 2020

# Attempt 1


```js
/**
 * @param {string} s
 * @param {number[]} indices
 * @return {string}
 */
var restoreString = function(s, indices) {
    const container = new Array(s.length);
    for( let i= 0 ; i < s.length ; i+=1 ){
        container[indices[i]] = s[i];
    }
    return container.join("");
};
```

Time complexity : O(N)

Space complexity : O(2N)