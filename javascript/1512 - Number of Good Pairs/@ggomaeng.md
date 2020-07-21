Author: @ggomaeng

Date: July 21, 2020

# Attempt 1

My first go-to thought was to use 2 for loops and check for matching conditions `nums[i] == nums[j]` and `i < j`. This would result in a time complexity of O(N^2), and I wanted to try to think of a better solution. If we were to iterate the `nums` array from index 0, we can safely assume that our current index (or value) is already greater than the previous index. Thus, we can omit the `i < j` condition and only focus on `nums[i] == nums[j]`. I solved it by using a map, and counting the number as a pair if the key in the map already exists.

```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var numIdenticalPairs = function(nums) {
    const map = {};
    let pairs = 0;

    nums.forEach((n) => {
        if(map[n] === undefined) map[n] = 0;
        else {
            map[n]++;
            pairs += map[n];
        }
    })

    return pairs;
};
```


Time complexity: O(N)

Space complexity: O(N)
