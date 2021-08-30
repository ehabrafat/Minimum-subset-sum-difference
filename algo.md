# Divide array into 2 subsets such that difference of their sum is minimized
Example: 
 A = {1,6,11,5}
Solutaion:
  {1,6,5} - {11} -> 12 - 11 = 1
# Algorithm
 - We need to find sum equal to or closest to (ArraySum/2)
 # why
 suppos ArraySum is 9 when divide 9/2 it gives us 4 ( (9-4) - 4) = 1 -> min diff 
# How can we get sum 
 We will use dynamic programming (tabulation method) to get sum in  O(n * sum)
1. Create 2D Boolean Array (n+1) * (sum+1)
2. loop and check if (j == 0) every item can make sum of 0 so make it True
               else if(i == 0 && j > 0) item 0 cannot create sum of j so make it False
               else if(A[i] > j) we cannot include this item so value still same in dp[i-1][j]
               else  dp[i][j] = dp[i-1][j] || dp[i-1][j - A[i]] // include item or exclute item 
               
3. if dp[n][sum/2] is false  // last row
   loop back to find closest sum 
   return (sum - 2*closestSum) // same as ( (sum - closestSum) - closestSum)





