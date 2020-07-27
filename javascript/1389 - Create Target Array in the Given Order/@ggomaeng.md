Author: @ggomaeng

Date: July 27, 2020

# Attempt 1

Sweet and simple O(N^2) solution. However, could there be a better way to solve this in O(N)?

```js
/**
 * @param {number[]} nums
 * @param {number[]} index
 * @return {number[]}
 */
var createTargetArray = function(nums, index) {
    let target = [];
    index.forEach((v, i) => {
        target.splice(v, 0, nums[i]);
    });
    return target;
};
```

Time complexity: O(N^2)

Space complexity: O(N)

# Attempt 2

This solution can solve the case at O(N), at best case, but at worst, it can achieve O(N^2). The worst case would be to insert at the beginning of the array repeatedly.

```js
/**
 * @param {number[]} nums
 * @param {number[]} index
 * @return {number[]}
 */
var createTargetArray = function(nums, index) {
    let target = new Array(nums.length);

    index.forEach((v, i) => {
        let insertIndex = v;
        let valueToInsert = nums[i];

        while(target[insertIndex] !== undefined) {
            const temp = target[insertIndex];
            target[insertIndex] = valueToInsert;
            valueToInsert = temp;
            insertIndex++;
        }

        target[insertIndex] = valueToInsert;
    });

    return target;
};
```


Time complexity: Worst case - O(N^2), Best case - O(N)

Space complexity: O(N)