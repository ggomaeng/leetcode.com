Author: @sjtommylee

Date: Apr 08, 2021

# Attempt 1

Simple string solution.
pass in -1 as third argument
compare reversed string & the converted string(num => str)

```python

class Solution:
    def isPalindrome(self, x: int) -> bool:
        if x < 0:
            return False
        else:
            s = str(x)
            if s[::-1] == s:
                return True
            else:
                return False


```

Time complexity: O(N^2)

Space complexity: O(N)
