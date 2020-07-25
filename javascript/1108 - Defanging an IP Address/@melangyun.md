Author @melangyun

Date : July 22, 2020

# Appempt 1

```javascript

/**
 * @param {string} address
 * @return {string}
 */
var defangIPaddr = function(address) {
    return address.replace(/\./g,"[.]");
};

```

Time complexity: O(N)

Space complexity: O(N)