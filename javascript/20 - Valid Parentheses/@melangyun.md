Author: @melangyun

Date: July 25, 2020

# Attempt 1

1. stack 에 괄호를 쌓는다.
2. 쌓여있는 stack의 마지막 index와 현재 string의 char(문자 1개)와 짝이 맞는다면 pop, 그렇지 않다면 push 하여 괄호를 쌓는다

```js
/**
 * @param {string} s
 * @return {boolean}
 */
var isValid = function(s) {
    const array = ["(", "[", "{", ")", "]", "}"];
    const stack = [];
    for( let i = 0 ; i < s.length ; i +=1 ){
        const index = array.indexOf(s[i]);
        const savedIndex = stack[stack.length-1];
        index - 3 === savedIndex? stack.pop() : stack.push(index);
    }
    
    return !stack.length;
};
```

Time complexity : O(N^2)

Space complexity : O(2N)

> 시간 복잡도가 높음

# Attempt 2

위와 동일히 stack을 활용하되, 괄호를 체크하는 방법을 바꿈

```js
/**
 * @param {string} s
 * @return {boolean}
 */
var isValid = function(s) {
    const checker = { "{" : "}", "[": "]", "(": ")"};
    const stack = []; 
    for( let i = 0 ; i < s.length ; i += 1 ){
        const lastVal= stack[stack.length-1];
        checker[lastVal] === s[i] ? stack.pop() : stack.push(s[i]);
    }
    return !stack.length;
};
```

Time complexity : O(N)

Space complexity : O(3N)