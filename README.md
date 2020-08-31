# MaximumSubSubArray
Link to the problem: https://www.interviewbit.com/problems/max-sum-contiguous-subarray/
Big O(N^3) solution in python

class Solution:
    # @param A : tuple of integers
    # @return an integer
    def maxSubArray(self, A):
        ans=0
        s=0
        for i in range(len(A)):
            s=A[i]
            if s>ans:
                ans=s
            else:
                pass
        for j in range(len(A)):
            for z in range(j+1,len(A)):
                s=sum(A[j:z])
                if s>ans:
                    ans=s
        return ans
       
        
            
#Sample input in problem link.
