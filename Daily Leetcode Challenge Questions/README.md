## 📌 Problem 1:
**LeetCode 1304**-Find n Unique Integers Sum up to zero(https://leetcode.com/problems/find-n-unique-integers-sum-up-to-zero/):
**Approach**
 - Declare an array nums of length n .
 - Make a var index that points to indexes of nums[] and var pairs of n/2 length.
 - Iterate over 1 to pairs. Store the no. in nums array both positive and negative. If n is odd store a 0 also in nums.
 - Return nums.

## 📌 Problem 2:
**LeetCode 1317**-Convert Integer to the Sum of Two No-Zero Integers(https://leetcode.com/problems/convert-integer-to-the-sum-of-two-no-zero-integers):
**Approach**
 - Traverse from 1 to n . calculate a and b where a is i and b is n-i
 - Since non zero is required put condition of a>0 and b >0 and make helper function isconatinszero(int n) which be == false for both a and b . 
 - Put a and b in isconatinszero(int n) .While (n > 0).  Return true if n%10 == 0 then  n=n/10  or false if not.
 - Return new int[][] in main func.

