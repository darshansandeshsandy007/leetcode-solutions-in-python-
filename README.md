# leetcode-solutions-in-python-
free leetcode solutions in python :::
class Solution:
    def pivotIndex(self, nums: List[int]) -> int:
        sumL,sumR=0,0
        for i in range (len(nums)):
            for j in range (i+1,len(nums)):
                sumL=sumL+nums[j]
            if sumL==sumR:
                return i
            else:
                sumL=0
                sumR=sumR+nums[i]
        return -1
