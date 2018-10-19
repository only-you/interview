# LeetCode 1 Two Sum

```
Given an array of integers, return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
Example:
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```


# 方法一
```
暴力搜索法，两个for循环枚举所有的情况，满足则返回，时间复杂度n2

```
# code
![](https://github.com/only-you/-/blob/master/picture/twosum1.png)

# 方法二
```
拿空间换时间，用map记录遍历过的数值和其下标，当target-nums[i]在map中存在时便找到了满足条件的answer
空间复杂度O(n), 时间复杂度O（n）

```
# code
![](https://github.com/only-you/-/blob/master/picture/twosum2.png)
