有機會再做Hashmap版本，這題基本上就是給定一個Target值，求會是哪兩個鍵中的值相加會跟Target值相同，暴力解法就是雙迴圈把所有可能依序解出，哪個是正確的就將其輸出

class Solution {
    public int[] twoSum(int[] nums, int target) 
    {
        for(int i=0;i<nums.length;i++)
        {
            for(int j=1;j<nums.length;j++)
            {
                if(nums[i]+nums[j]==target)
                {
                    return new int[]{i,j};
                }
            }
        }
        return new int[0];
    }
}
        
//暴力迴圈解題