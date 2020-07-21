Author: @ggomaeng

Date: July 21, 2020

# Attempt 1

Using two arrays, and comparing intersection.

```js
/**
 * @param {string} J
 * @param {string} S
 * @return {number}
 */
var numJewelsInStones = function(J, S) {
    const jewels = J.split("");
    const stones = S.split("");
    let count = 0;

    stones.forEach(s => {
        if(jewels.includes(s)) {
            count++;
        }
    })

    return count;
};
```

Time complexity: O(N^2)

Space complexity: O(M + N)


# Attempt 2

Using regular expression to check matches.

```js
/**
 * @param {string} J
 * @param {string} S
 * @return {number}
 */
var numJewelsInStones = function(J, S) {
    const chars = [...J];
    const exp = chars.reduce((acc, c, i) => i === 0 ? c : `${acc}|${c}`);
    const regExp = new RegExp(exp, 'g');
    const matches = S.match(regExp);
    return matches ? matches.length : 0;
};
```

Time complexity: O(N)

Space complexity: O(M)
