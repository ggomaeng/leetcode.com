Author: @melangyun

Date: July 25, 2020

# Attempt 1

target이 맞을때 까지 반복문을 돈다

```js
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for( let i = 0 ; i < nums.length - 1 ; i +=1 ){
        for(let j = i + 1 ; j < nums.length ; j +=1 ){
            if( nums[i] + nums[j] === target ){
                return [ i, j ];
            }
        }
    }
};
```

Time complexity : O(N^2)

Space complexity : O(N)



# Solution 1

**comp**
- key : target - nums[i]
- value : index
<br><br>
`comp[nums[i]]`가 0 이상이라면(존재한다면) index들을 return. <br>
comp에는 target과 nums[i]와의 차가 key로 존재함으로, 또다른 index의 value가 그 차와 같다면 둘의 합은 0일것이다 

```js
var twoSum = function(nums, target) {
    const comp = {};
    for(let i = 0 ; i < nums.length ; i++){
        if(comp[nums[i]]>=0){
            return [ comp[nums[i] ] , i]
        }
        comp[target-nums[i]] = i
    }
};
```

Time complexity : O(N)

Space complexity : O(N)
