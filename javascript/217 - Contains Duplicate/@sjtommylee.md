Author: @sjtommylee

Date: April 29, 2021

# Attempt 1

1. creating a new Set object
2. Essentially, Set object lets you store unique values of any type. A value in the Set many only occur once
3. size accessor prop will return the number of unique elements in the set object !== length of the array

```js
/**
 * @param {string} s
 * @return {boolean}
 */

const containsDuplicate = (nums) => {
  const set = new Set(nums);
  return set.size !== nums.length;
};
```

Time complexity : O(N)
Space complexity : O(N)
