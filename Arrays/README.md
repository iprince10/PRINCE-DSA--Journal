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
   
## 📌 Problem 5:
**LeetCode 287**- Find the duplicate number (https://leetcode.com/problems/find-the-duplicate-number);
**Approach**
 - Use binary search on the value range from 1 to n.
 - For each mid, count how many numbers in the array are <= mid.
 - If count > mid, the duplicate must be in the left half; otherwise, it’s in the right half.
 - Narrow down until low == high, which is the duplicate number.

## 📌 Problem 6:
**LeetCode 136**- Single Number(https://leetcode.com/problems/single-number);
**Approach**
 - Bit Manipulation, initialize a variable index with 0 and for the array length:
 - XOR of number with itself is 0 and XOR of number with 0 is number itself, return index

## 📌 Problem 7:
**LeetCode 33**- Search in sorted rotated array(https://leetcode.com/problems/search-in-rotated-sorted-array):
**Approach**
 - Initialize start and end of the array . Calculate mid while start<end.
 - If number[mid]== target , return mid; if not check for both sorted rotated left and sorted rotated right.
 - For sorted left half,nums[start]<=nums[mid], if number lies in left update end = mid-1,else start = mid+1.
 - For sorted right half, nums[end]>=nums[mid] ,if number lies in right side update start = mid + 1, else end = mid-1.
 - Return -1 , if number not found.

## 📌 Problem 8:
**LeetCode 81**-Search in sorted rotated array ii (https://leetcode.com/problems/search-in-rotated-sorted-array-ii):
**Approach**
 - Initialize left and right of the array . Calculate mid while left <= right .
 - If number[mid]== target , return true;
 - Put condition if (nums[left]== nums[mid] && nums[right]== nums[mid]) , increment left++ decrement right -- ,continue,this cancels out repeated nums that causes problems in finding left and right sorted arrays from both sides of mid.
 - If nums [mid] != target , check for both sorted rotated left and sorted rotated right.
 - For sorted left half, if number lies in left update right ,else left.
 - For sorted right half . if number lies in right side update left, else right.
 - Return false , if number not found.

## 📌 Problem 9:
**LeetCode 560**- Subarray Sum equals k (https://leetcode.com/problems/subarray-sum-equals-k):
**Approach**
 - This approach is not optimal but still can be used , use hashmap for better solution.
 - initialise count variable as 0 and declare sum variable . Calculate sum for outer loop index and if sum == target , count++
 - similarly for inner loop starting from index+1 , do the same and return count.

## 📌 Problem 10:
**LeetCode 153**-Find minimum in rotated sorted array(https://leetcode.com/problems/find-minimum-in-rotated-sorted-array):
**Approach**
 - Use Binary search , initialize left and right (since it demands last element (left<right)not equal to.
 - calculate mid , compare mid with right , if mid >= right , update left,else right = mid .
 - Return nums[left].

## 📌 Problem 11:
**LeetCode 154**-Find minimum in rotated sorted array ii(https://leetcode.com/problems/find-minimum-in-rotated-sorted-array-ii):
**Approach**
 - Same as above just add a condition to check duplicates (if nums[left] and nums[right] == nums [mid] , left ++, right--, continue.
 - Another approach is without condition , compare mid , if mid > right , update left = mid +1 , else if mid < right, right = mid , else right --.
 - Second approach should be considered as it is more reliable for all test cases.

## 📌 Problem 12:
**LeetCode 162**-Find peak element(https://leetcode.com/problems/find-peak-element):
**Approach**
 - Use binary search , initialize left=0 and right=n-1 , while (left<right), find mid ,
 - compare mid with mid + 1, if mid <= mid + 1, update left = mid +1, else right = mid, return left.

## 📌 Problem 13:
**LeetCode 912**-Sort an Array(https://leetcode.com/problems/sort-an-array):
**Approach**
 - Find the largest and smallest element of the nums array.
 - Make a count array to store frequncies of the elements of the nums array. Size of the count array is (largest - smallest + 1).
 - Store the frequencies by count[nums[i]-smallest].
 - Now sort this count array containing frequncies. Make a variable for pointing indexes of nums array j = 0, iterate over the count array, while count[i]>0, nums[j]=i+smallest,j++,count[i]--.
 - Return nums.
 - This approach works for negative elements in array as well.

## 📌 Problem 14:
**LeetCode 75**-Sort colors(https://leetcode.com/problems/sort-colors):
**Approach**
 - Can be done by any sorting technique like insertion and counting sort , but best is counting sort because of small input.
 - Use counting sort , find largest and smallest element.
 - Make count array to store frequencies and count array length is (l-s+1). Store frequncies in array by count[nums[i]-smallest].
 - Now sort the counting array . Refer to problem 13 for sorting.

## 📌 Problem 15:
**LeetCode 283**- Move Zeroes(https://leetcode.com/problems/move-zeroes):
**Approach**
 - Using two pointers.
 - Initialize left pointer with 0, and iterate right pointer over the nums length.
 - When nums[right] != 0, then swap the element of left and right , increment left.
