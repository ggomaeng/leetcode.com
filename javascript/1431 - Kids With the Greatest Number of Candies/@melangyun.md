Author @melangyun

Date : July 22, 2020

# Appempt 1

```javascript
/**
 * @param {number[]} candies
 * @param {number} extraCandies
 * @return {boolean[]}
 */
var kidsWithCandies = function(candies, extraCandies) {
    const max = Math.max(...candies);
    return candies.map(curval => curval + extraCandies >= max );
};
```