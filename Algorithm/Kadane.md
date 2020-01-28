
asdasdasdasdasda 
```  //python 
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        sum_tmp = nums[0]
        res = nums[0]
        for i in range(1,len(nums)):
            sum_tmp = nums[i] if sum_tmp < 0 else sum_tmp + nums[i]
            res = max(res, sum_tmp);
        return res;
```
