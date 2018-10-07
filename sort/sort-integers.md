# LintCode 463 Sort Integers

用冒泡排序、选择排序、插入排序都实现一遍(时间复杂度都是O(n^2))

# 冒泡排序：
冒泡排序算法的原理如下：
比较相邻的元素。如果第一个比第二个大，就交换他们两个。
对每一对相邻元素做同样的工作，从开始第一对到结尾的最后一对。在这一点，最后的元素应该会是最大的数。
针对所有的元素重复以上的步骤，除了最后一个。
持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。
![](https://github.com/only-you/-/blob/master/picture/bubble.png)


# 选择排序：
选择排序（Selection sort）是一种简单直观的排序算法。它的工作原理是每一次从待排序的数据元素中选出最小（或最大）的一个元素，存放在序列的起始位置，直到全部待排序的数据元素排完。 选择排序是不稳定的排序方法。
![](https://github.com/only-you/-/blob/master/picture/choose.png)

# 插入排序：
每次处理就是将无序数列的第一个元素与有序数列的元素从后往前逐个进行比较，找出插入位置，将该元素插入到有序数列的合适位置中。
![](https://github.com/only-you/-/blob/master/picture/insert.png)
