class Solution {
    public int fun(int[] nums, int i, int[] dp) {
        if (i < 0) {
            return 0;
        }
        if (dp[i] != -1) {
            return dp[i];
        }
        if (i == 0) {
            return nums[i];
        }
        int take = nums[i] + fun(nums, i - 2,dp);
        int notTake = fun(nums, i - 1,dp);
        dp[i] = Math.max(take, notTake);
        return dp[i];
    }

    public int rob(int[] nums) {
        int[] dp = new int[nums.length + 1];
        Arrays.fill(dp, -1);
        return fun(nums, nums.length - 1, dp);
    }
}