Author: @sjtommylee

Date: Apr 08, 2021

# Attempt 1

First two lines provided.
Brute force solution using double loop.

```python

class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            for j in range(len(nums)):
                if nums[i] + nums[j] == target and i != j:
                    return [i, j]


```

Time complexity: O(N^2)

Space complexity: O(N)
