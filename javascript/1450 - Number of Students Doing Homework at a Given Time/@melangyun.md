Author @melangyun

Date : August 15, 2020

# Attempt 1

```javascript
/**
 * @param {number[]} startTime
 * @param {number[]} endTime
 * @param {number} queryTime
 * @return {number}
 */
var busyStudent = function(startTime, endTime, queryTime) {
    let count = 0;
    for(let i = 0 ; i < startTime.length ; i +=1 ){
        if( queryTime >= startTime[i] && queryTime <= endTime[i] ) count++;
    }
    return count;
};
```

Time complexity: O(N)

Space complexity: O(1+2N)