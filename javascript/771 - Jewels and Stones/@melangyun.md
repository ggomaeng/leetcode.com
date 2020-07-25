Author @melangyun

Date : July 22, 2020

# Appempt 1

```javascript
/**
 * @param {string} J
 * @param {string} S
 * @return {number}
 */
var numJewelsInStones = function(J, S) {
    let count = 0;
    for(let i= 0 ; i < S.length ; i+=1 ){
        if(J.indexOf(S[i]) !== -1){
            count += 1;
        }
    }
    return count;
};
```

Time complexity : O(N^2)

Space complexity : O(2N + 1)