一對數組candies和整數extraCandies，其中candies[i]代表第i位孩子擁有的糖果數量，判斷如果將extraCandies給數組中的任一數，也就是任一個孩子，他是否能成為擁有糖果數量最多的人。

```
class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        int max = Arrays.stream(candies).max().getAsInt();
        List<Boolean> result = new ArrayList<>();
        for(int i=0;i<candies.length;i++){
        if(candies[i]+extraCandies>=max){
        result.add(true);
        }
        else 
        result.add(false);
        }
        return result;
    } 

}
```