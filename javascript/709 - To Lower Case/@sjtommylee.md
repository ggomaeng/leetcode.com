Author @sjtommylee

Date : May 16, 2021

# Attempt1

Using the charcode table, where the difference between uppercase and lowercase is 32 items.

```js
const toLowerCase = function (str) {
  let lowerCase = "";

  for (let letter of str) {
    const index = letter.charCodeAt(0);
    if (index >= 65 && index <= 90) {
      letter = String.fromCharCode(index + 32);
    }
    lowerCase += letter;
  }
  return lowerCase;
};
```

Time complexity : O(N)

Space complexity : O(N)
