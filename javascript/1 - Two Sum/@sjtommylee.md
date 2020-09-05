Author: @sjtommylee

Date: Sept 05, 2020

# Attempt 1

```js

/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */


function twoSum(arr, S) {
    for (var i = 0; i < arr.length; i++) {
        for (var j = i + 1; j < arr.length; j++) {
            if (arr[i] + arr[j] === S) {
                return [i, j];
            }
        }
    }
}



```



Time complexity: O(N)

Space complexity: O(N)