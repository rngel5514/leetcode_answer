## 算法介绍
解决最大子序列的和（maximum subarray)
## 算法时间复杂度&空间复杂度
时间复杂度O(n)  
空间复杂度
## 算法示例代码
```   python 
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        sum_tmp = nums[0]
        res = nums[0]
        for i in range(1,len(nums)):
            sum_tmp = nums[i] if sum_tmp < 0 else sum_tmp + nums[i]
            res = max(res, sum_tmp);
        return res;
```
## 算法理解
1.将最大子序列分块  
2.最大子序列是以一个正数开头并以最大和为正数结尾  
3.不断比较各个符合2要求的子序列值找出最大值
