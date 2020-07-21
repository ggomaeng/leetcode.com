Author: @ggomaeng

Date: July 21, 2020

# Attempt 1

```js
/**
 * @param {number[]} candies
 * @param {number} extraCandies
 * @return {boolean[]}
 */
var kidsWithCandies = function(candies, extraCandies) {
    const max = Math.max(...candies);
    return candies.map(candy => candy + extraCandies >= max);
};
```


Time complexity: O(2N) = O(N)

Space complexity: O(2N)
