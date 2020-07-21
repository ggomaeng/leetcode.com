Author: @ggomaeng

Date: July 21, 2020

# Attempt 1

```js
/**
 * @param {number} num
 * @return {number}
 */
var numberOfSteps  = function(num) {
    let step = 0;

    while (num !== 0) {
        num % 2 === 0 ? num /= 2 : num--;
        step++;
    }

    return step;
};
```

Time complexity: O(1)

Space complexity: O(1)
