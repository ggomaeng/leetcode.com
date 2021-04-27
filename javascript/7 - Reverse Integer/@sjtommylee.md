Author: @sjtommylee

Date: Apr 27, 2021

# Attempt 1

N = length of input as string

```js
/**
 * @param {number} x
 * @return {boolean}
 */

const reverse = (x) => {
  let arr = x.toString().split("");
  let left = arr[0] == "-" ? 1 : 0;
  let right = arr.length - 1;
  while (left < right) {
    [arr[left], arr[right]] = [arr[right], arr[left]];
    left++, right--;
  }
  let res = Number(arr.join(""));
  return res >= -(2 ** 31) && res <= 2 ** 31 - 1 ? res : 0;
};
```

Time complexity: O(N)
Space complexity: O(N)

# Attempt 2
