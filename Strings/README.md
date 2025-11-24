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

## 📌 Problem 3:
**LeetCode 12** - Integer to Roman (https://leetcode.com/problems/integer-to-roman):
**Approach**
 - Make a final inetger values[] storing all  13 values from 1000 to 1  (remember by 10,9,5,4).
 - Make a final string symbols[] storing all 13 corresponding symbols.
 - Make a StringBuilder sb initialize with empty string.
 - Iterate over the values array. Break the loop when num==0.
 - While(num>=values[i]) append the symbol corresponding to value in sb.
 - and num is num-values[i].
 - Return sb.toString().

## 📌 Problem 4:
**LeetCode 3541** -(https://leetcode.com/problems/find-most-frequent-vowel-and-consonant):
**Approach**
 - Make a frequency array of size 26 storing frequency of characters
 - Initialize maxvowel and maxconsonant two variables with 0 .
 - Iterate over the string length , get char at each index store in variable c .
 - Subtract c with 'a' (bcoz char has their values a has 97 value ).
 - Increment freq[i].
 - Check if c is vowel if yes increase maxvowel using Math.max, else maxconsonant.
 - Return maxvowel+maxconsonant.  

## 📌 Problem 4:
**LeetCode 14** -Longest Common Prefix(https://leetcode.com/problems/longest-common-prefix)
**Approach**
 - Sort the array of string first.Because it gives the extreme cases for comparing.
 - Make two strings s1 and s2 containing first and last string of the given string.
 - Initialize index variable by zero .
 - While idx > s1.length() && s2.length() as well. Compare each char of s1 and s2. If equal increment idx ,else break the loop.
 - Return s1.substring(0,idx).
 
## 📌 Problem 4:
**LeetCode** - Will be added soon
