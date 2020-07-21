Author: @ggomaeng

Date: July 21, 2020

# Attempt 1

```js
/**
 * @param {string} address
 * @return {string}
 */
var defangIPaddr = function(address) {
    return address.replace(/[.]/g, "[.]");
};
```


Time complexity: O(N)

Space complexity: O(N)
