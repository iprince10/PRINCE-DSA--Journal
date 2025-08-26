# Arrays Problems Journal

This section contains all the array problems I solve, along with short explanations of their approaches.

## 📌 Problem 1:
**LeetCode 704** - Binary Search (https://leetcode.com/problems/binary-search);
**Approach**
  - Use binary search
  - Time _O(log n ) | Space_O(1)

## 📌 Problem 2:
**LeetCode 53** - Maximum Subarray ( https://leetcode.com/problems/maximum-subarray);
**Approach**
 - Use Kadane's Algorithm :Initialize current sum and max sum, track current sum, update maxsum with max(cs,ms) ,reset cs if negative, keep max.
 - Time_O(n) | Space_O(1)

## 📌 Problem 3:
**LeetCode 121** - Best Time to buy and Sell Stock (https://leetcode.com/problems/best-time-to-buy-and-sell-stock);
**Approach**
 - Intiliaze Buyprice with initial price or +infinity and maxprofit with 0 , update buyprice if selling price is lower (b.p.= s.p.) or calculate         profit if buyprice is < selling price.
 - Then update maxprofit with max(profit, maxprofit), keep maxprofit

## 📌 Problem 4:
**LeetCode 42**-Trapping Rain Water(https://leetcode.com/problems/trapping-rain-water);
**Approach**
 - Calculate leftmaximum and rightmaximum boundary by creating leftmax and rightmax array[]. [0]th index is same , other index are max(height[i],lm[i-1];
 - Calculate waterlevel for each height[i] by min(leftmax[i],rightmax[i]).
 - Initialize trappedrainwater by 0 and calculate trw by +=waterlevel -height[i].
 - keep trappedrainwater.
   
