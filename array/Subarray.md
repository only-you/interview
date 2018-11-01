# LintCode 138 Subarray Sum

```
Description
Given an integer array, find a subarray where the sum of numbers is zero. Your code should return the index of the first number and the index of the last number.
There is at least one subarray that it's sum equals to zero.

Example
Given [-3, 1, 2, -3, 4], return [0, 2] or [1, 3].
```

# idea
```
用空间换时间：hashmap       O（n）
HashMap 在Array 题目中一般可以用O(n)的时间复杂度解决两种问题
1，求两者之和为固定某数
   if (map.contains(sum - curtValue)) {
       index1 = map.get(sum - curtValue);
       index2 = curtIndex;
       break;
   }

2，求两个index之间的所有数的和为某数
   if (map.contains(curtSum - sum)) {
       index1 = map.get(curtSum - sum);
       index2 = curtIndex;
       break;
   }
思路：sum + 一堆连续的数字（也就是连续子数组）后  如果还是 = sum；
则证明这个连续子数组之和 = 0，
所以可以利用hashmap记录之前产生过的每次sum和其遍历所到达的下标；
如果hashmap中已经有过这个sum，则证明这之间的连续子数组之和为0
```

# code
![](https://github.com/only-you/interview/blob/master/picture/138.png)
