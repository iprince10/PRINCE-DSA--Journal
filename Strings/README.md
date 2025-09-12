# Strings Problems Journal

This section contains all the strings problems I solve, along with short explanations of their approaches.

## 📌 Problem 1:
**LeetCode 3227** - Vowels game in a string(https://leetcode.com/problems/vowels-game-in-a-string):
**Approach**
 - Iterate over the string elements.
 - Find if any there is any vowel in the string , if yes return true.
 - else return false.

## 📌 Problem 2:
**LeetCode 3227** -Roman to integer(https://leetcode.com/problems/roman-to-integer):
**Approach**
 - make a map storing character and integer
 - Initialize a result variable . Iterate over the string elements , declare a curr variable store the integer value of current index iteration.
 - Check if next index of iteration is smaller than string length if yes then store its number value in next variable.
 - compare curr and next values , if curr < next then result = result - curr
 - else result = result+curr.
 - return result.   
