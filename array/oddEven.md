# LintCode 373 Partition Array by Odd and Even

```
Description
Partition an integers array into odd number first and even number second.
Have you met this question in a real interview?  
Example
Given [1, 2, 3, 4], return [1, 3, 2, 4]
Challenge
Do it in-place.
```

# idea:
```
快速排序中的一次partition：把交换条件从大小比较，换成判断奇偶；
也就是说把排序改成奇偶两边排。

```

# code:
![](https://github.com/only-you/-/blob/master/picture/oddEven.png)
