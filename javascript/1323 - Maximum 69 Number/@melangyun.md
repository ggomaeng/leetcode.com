Author: @melangyun

Date : Aug 11. 2020

# Attempt 1

직관적으로 풀어 씀
```js
/**
 * @param {number} num
 * @return {number}
 */
var maximum69Number  = function(num) {
    const numArr = (num+"").split("");
    for( let i = 0 ; i < numArr.length ; i ++ ){
        if(numArr[i] === "6"){
            numArr[i] = "9";
            break;
        }
    }
    
    return numArr.join("") * 1 ;
};
```

Time complexity: O(N)

Space complexity: O(N)


# Attempt 2
replace 는 정규표현식 옵션이 없다면, 가장 앞의 글자만 바꾼다
```js
/**
 * @param {number} num
 * @return {number}
 */
var maximum69Number  = function(num) {
    return +(num+"").replace("6","9");
};
```

Time complexity: O(1) ~ O(N)

Space complexity: O(N)