Author: @ggomaeng

Date: July 21, 2020

# Attempt 1

`Array.prototype.splice()` can have O(N) at worst case scenarios. Thus, this might not be the optimal solution. At the sacrifice of performance, this uses O(N) space.

```js
/**
 * @param {number[]} nums
 * @param {number} n
 * @return {number[]}
 */
var shuffle = function(nums, n) {
    for (let i = n; i < nums.length - 1; i++) { // O((N/2) - 1)
        nums.splice((i - n) * 2 + 1, 0, nums.splice(i, 1)[0]); // O(N)
    }

    return nums;
};
```

Time complexity: O(N^2);

Space complexity: O(N)


# Attempt 2

To shorten the time complexity, we iterate over an empty array and assign the left half of the `nums` array to even indices and right half of the `nums` array to odd indices. At the sacrifice of space, this uses O(N) time complexity.

```js
/**
 * @param {number[]} nums
 * @param {number} n
 * @return {number[]}
 */
var shuffle = function(nums, n) {
    const arr = new Array(2 * n).fill(undefined);

    arr.forEach((v, i) => {
        if(i < n) arr[i * 2] = nums[i];
        else arr[(i - n) * 2 + 1] = nums[i];
    })

    return arr;
};
```

Time complexity: O(N);

Space complexity: O(2N)
