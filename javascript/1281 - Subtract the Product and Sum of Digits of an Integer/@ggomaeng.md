Author: @ggomaeng

Date: July 27, 2020

# Attempt 1

```js
/**
 * @param {number} n
 * @return {number}
 */
var subtractProductAndSum = function(n) {
    const digits = [...`${n}`];
    let product = 1, sum = 0;
    digits.forEach(d => {
        product *= +d;
        sum += +d;
    })

    return product - sum;
};
```


Time complexity: O(N)

Space complexity: O(N)
