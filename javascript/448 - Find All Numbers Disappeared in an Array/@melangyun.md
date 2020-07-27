Author @melangyun

Date : July 27, 2020

# Attempt 1

checkObj를 만들어 넣고, key값으로 nums(Array)의 배열을 추가한다.<br>
object에 key로 array가 존재하는지 확인하고, 없다면 배열에 담아 return

```js
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var findDisappearedNumbers = function(nums) {
    const checkObj = {};
    const numberingArr = [];
    for(let i = 0 ; i < nums.length ; i+=1 ){
        if(!checkObj[nums[i]]){
            checkObj[nums[i]] = 1;
        }
        numberingArr.push(i+1);
    }
    
    return numberingArr.reduce((acc, curVal) => {
        if(!checkObj[curVal]){
            acc.push(curVal);
        }
        return acc;
    },[]) 
};

```

Time complexity : O(N)

Space complexity : O(2N + 1)