Author: @sjtommylee

Date: Aug 05, 2020

# Attempt 1

create a a new array filteredNums using filter() to search through the array of numbers, check if the length of the string is even using % 2.
//nums =  [12,345,2,6,7896]
//filteredNums =  [12, 7896]

return the length of new array filteredNums. 


```js
/**
 * @param {number[]} nums
 * @return {number}
 */


const findNumbers = (nums) => {
    let filteredNums = nums.filter(n => n.toString().length % 2 === 0)
    return filteredNums.length
}

```

Time complexity: O(N)

Space complexity: O(N)