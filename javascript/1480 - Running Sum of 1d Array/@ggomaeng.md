Author: @ggomaeng

Date: July 20, 2020


# Attempt 1

My initial thought was to use `.map` or `.forEach`.

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var runningSum = function(nums) {
    let sum = 0;
    return nums.map(v => {
        sum += v;
        return sum;
    });
};
```

Time complexity: O(N)

Space complexity: O(2N), because it iterates nums and returns a new array.

# Attempt 2

Wanted to try squeezing the extra space by directly modifying the input array.

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var runningSum = function(nums) {
    for(let i = 0; i < nums.length; i++) {
        if(nums[i + 1] !== undefined) {
            nums[i + 1] += nums[i];
        }
    }

    return nums;
};
```

Time complexity: O(N)

Space complexity: O(N)
