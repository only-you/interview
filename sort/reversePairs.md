归并排序的应用

[题目链接](https://www.lintcode.com/problem/reverse-pairs/description)

```
Description
For an array A, if i < j, and A [i] > A [j], called (A [i], A [j]) is a reverse pair.
return total of reverse pairs in A.
Example
Given A = [2, 4, 1, 3, 5] , (2, 1), (4, 1), (4, 3) are reverse pairs. return 3
```

```
第一种方法：直接两层for循环，两两比较，记录满足条件的对数，时间复杂度为（n2）；
```


```
第二种方法：利用归并排序的合并过程，因为合并的时候两个子数组已经是有序的了，
这样子便可以直接得到最小的满足条件的元素的下标，之后的元素便都满足条件。时间复杂度（nlogn）
```
![](https://github.com/only-you/-/blob/master/picture/reverse.png)
