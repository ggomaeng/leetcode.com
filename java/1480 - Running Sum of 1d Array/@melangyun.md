Author: @melangyun

Date : 2020. 11. 04

Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).

Return the running sum of nums.
```
Input: nums = [1,2,3,4]
Output: [1,3,6,10]
```

```
Input: nums = [1,1,1,1,1]
Output: [1,2,3,4,5]
```
# Attempt 1

- input array와 output array와 할당되는 수가 같으므로 length만큼 선언하고 시작,
- 시작을 0번째로 시작하고, 이후에 누적 합을 더해감

```java
class Solution {
    public int[] runningSum(int[] nums) {
        int[] result = new int[nums.length];
        result[0] = nums[0];
        for(int i = 1 ; i < nums.length ; i++ ){
            result[i] = nums[i]+ result[i-1];
        }
        return result;
    }
}
```

Time complexity : O(N)

Space complexity : O(2N)
