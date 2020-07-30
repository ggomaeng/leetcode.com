Author @melangyun

Date : July 31, 2020

# Attempt1
ascii code를 이용하여 비교하고, 대문자일 경우에만 소문자로 변경 후 return

```js
var toLowerCase = function(str) {
    const capital = "A".charCodeAt();
    const small = "a".charCodeAt();
    const btw = small - capital;
    return [...str].map( val => {
        const ascii = val.charCodeAt();
        return ascii < small && ascii >= capital ? String.fromCharCode(ascii + btw) : val; 
    }).join("");
};
```
Time complexity : O(N)

Space complexity : O(2N+3)
