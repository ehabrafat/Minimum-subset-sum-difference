# GOAL:- Divide array into 2 subsets such that difference of their sum is minimized
example: 
 A = {1,6,11,5}
solutaion:
  {1,6,5} {11} -> 12 - 11 = 1
 
# Steps
 - We need to find sum equal to or closest to (ArraySum/2)
# why
suppos ArraySum is 9 when divide 9/2 it gives us 4
 5 - 4 = 1 -> min diff
 
 - then we can subtract ArraySum from sum and return the min differnce 




