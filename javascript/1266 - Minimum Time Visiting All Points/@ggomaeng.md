Author: @ggomaeng

Date: August 5, 2020

# Attempt 1

Because the time it takes for you to move vertically, horizontally, or diagonally all takes 1 second, , you really only have to consider the bigger difference between (x1, x2) and (y1, y2).

```js
/**
 * @param {number[][]} points
 * @return {number}
 */
var minTimeToVisitAllPoints = function(points) {
    return points.reduce((acc, curr, i) => {
        if(points[i + 1]) {
            const [x1, y1] = curr;
            const [x2, y2] = points[i + 1];
            const dX = Math.abs(x1 - x2);
            const dY = Math.abs(y1 - y2);
            return acc + Math.max(dX, dY);
        } else return acc;
    }, 0)
};
```


Time complexity: O(N)

Space complexity: O(1)
