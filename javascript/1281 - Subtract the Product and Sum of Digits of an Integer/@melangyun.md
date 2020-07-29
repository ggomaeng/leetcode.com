Author: @melangyun

Date: July 29, 2020

# Attempt1

```js
/**
 * @param {number} n
 * @return {number}
 */
var subtractProductAndSum = function(n) {
    let product = 1;
    let sum = 0;
    [...(n+"")].forEach( val => {
        product *= val;
        sum += val*1;
    });
    return product - sum;
};
```