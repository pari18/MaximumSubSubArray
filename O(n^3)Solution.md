# MaximumSubSubArray
Link to the problem: https://www.interviewbit.com/problems/max-sum-contiguous-subarray/
Big O(N^3) solution in python
        
            
#Sample input in problem link.
#CODE STARTS FROM HERE
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
N=int(input("enter size of elements"))
print("enter elements of array")
A=list(map(int, input().split()))[:N]
sol=Solution()
answer=sol.maxSubArray(A)
print(answer)
