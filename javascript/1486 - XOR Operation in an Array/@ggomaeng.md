Author: @ggomaeng

Date: July 27, 2020

# Attempt 1

Simple for loop

```js
/**
 * @param {number} n
 * @param {number} start
 * @return {number}
 */
var xorOperation = function(n, start) {
    let result = start;
    for(var i = 0; i < n - 1; i++) {
        start += 2;
        result ^= start;
    }
    return result;
}
```


Time complexity: O(N)

Space complexity: O(1)

# Attempt 2

Overkill one liner

```js
/**
 * @param {number} n
 * @param {number} start
 * @return {number}
 */
var xorOperation = function(n, start) {
    return new Array(n).fill(undefined).map((v, i) => start + 2 * i).reduce((acc, curr) => acc ^= curr)
};
```


Time complexity: O(N)

Space complexity: O(N)
