Author: @melangyun

Date : 2020. 11. 04

Given the array candies and the integer extraCandies, where candies[i] represents the number of candies that the ith kid has.

For each kid check if there is a way to distribute extraCandies among the kids such that he or she can have the greatest number of candies among them. Notice that multiple kids can have the greatest number of candies.

- extraCandies 를 받았을 때에 최대로 많은 수의 사탕을 받을수 있을까?

# Attempt 1
- 최대 사탕의 갯수를 구함
- extraCandies 를 받았을 때에 최대 사탕의 수 이상인가를 배열로 반환

```java

class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        int max = candies[0];
        for(int i = 0 ; i < candies.length ; i++ ){
            if(max < candies[i]){
                max = candies[i];
            }
        }
        
        List<Boolean> result = new ArrayList<Boolean>();
        for(int i = 0 ; i < candies.length ; i++ ){
            result.add(max <= (candies[i] + extraCandies));
        }
        
        return result;
    }
}

```