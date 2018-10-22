# LintCode 144 Interleaving Positive and Negative Numbers

```
Description
Given an array with positive and negative integers. Re-range it to interleaving（交错） with positive and negative integers.
You are not necessary to keep the original order of positive integers or negative integers.
Have you met this question in a real interview?  
Example
Given [-1, -2, -3, 4, 5, 6], after re-range, it will be [-1, 5, -2, 4, -3, 6] or any other reasonable answer.
Challenge
Do it in-place and without extra memory.
```

# idea:
```
1、利用快排的partition进行分区，将数组分成负数在左边，正数在右边
2、根据上面快排partition得到的负数的个数，得到正数的个数，交换的时候进行分类讨论
--》一：负数多，则interleave（A， 1， n-1）
--》二：正数多，则interleave（A，0，n-2）
--》三：一样多，则interleave（A，1， n-2）
```

# code:
![](https://github.com/only-you/-/blob/master/picture/interleave.png)
