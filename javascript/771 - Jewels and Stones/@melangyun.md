Author @melangyun

Date : July 22, 2020

# Attempt 1

보석 J를 돌면서 S에 존재하는 것인지 체크한다.<br>
- **indexOf** method는 N의 시간복잡도를 갖음

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
