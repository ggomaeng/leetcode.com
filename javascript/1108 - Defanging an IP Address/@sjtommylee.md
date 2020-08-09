Author: @sjtommylee

Date: Aug 05, 2020

# Attempt 1

Simple brute force solution in two steps. 
run split('.') on address and store in newAddress
join each index with [.]

```js
/**
 * @param {string} address
 * @return {string}
 */
const defangIPaddr = (address) => {
    let newAddress = address.split(".")
    let newIp = newAddress.join('[.]')
    
    return newIp
}

```

Time complexity: O(N)

Space complexity: O(N)