Author: @ggomaeng

Date: August 5, 2020

# Attempt 1

Take a look at the bit comparison below:

a 1100001 A 1000001
b 1100010 B 1000010
c 1100011 C 1000011

The difference between capital letter and lowercase letter is 32, which means we only need to flip the 6th bit of the string. To go from A -> a, we do an OR bitwise operation on the charcode and "0100000".

```js
/**
 * @param {string} str
 * @return {string}
 */
var toLowerCase = function(str) {
    let result = "";
    for(let char of str) result += String.fromCharCode(char.charCodeAt(0) | 32);
    return result;
};
```


Time complexity: O(N)

Space complexity: O(2N)
