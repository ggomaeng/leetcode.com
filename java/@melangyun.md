Author: @melangyun

Date: September 27, 2020

# Attempt 1

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int i = 0 ; i < nums.length ; i++ ){
            for(int j = i + 1 ; j < nums.length ; j++){
                if(nums[j] == target - nums[i]){
                    return new int[] {i, j};
                }
            }
        }
    }
}
```

Time complexity : O(N^2)

Space complexity : O(N)
