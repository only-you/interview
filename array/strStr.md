# LeetCode 28 Implement strStr()

```
常规解法解这道题足够，不需要也没必要用KMP算法，也不需要掌握KMP算法，考察这道题的目的其实就是看你会不会写代码。
```

[题目链接](https://leetcode.com/problems/implement-strstr/submissions/)

```
Implement strStr().
Return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.
Example 1:
Input: haystack = "hello", needle = "ll"
Output: 2

Example 2:
Input: haystack = "aaaaa", needle = "bba"
Output: -1

Clarification:
What should we return when needle is an empty string? This is a great question to ask during an interview.
For the purpose of this problem, we will return 0 when needle is an empty string. This is consistent to C's strstr() and Java's indexOf().
```

# 思路
```
直观解法：
拿s2和s1一一比较，只要一不相同便s2从0开始，s1的下标加一。
```
# code
![](https://github.com/only-you/-/blob/master/picture/str.png)
