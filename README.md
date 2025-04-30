class Solution(object):
    def lengthOfLIS(self, nums):
        m=len(nums)
        maxwell=1
        dp=[1]* (m)
        for i in range(1,m):
            for j in range(i):
                if(nums[i]>nums[j]):
                    dp[i]=max(dp[i],dp[j]+1)
            maxwell=max(maxwell,dp[i])
        return maxwell
