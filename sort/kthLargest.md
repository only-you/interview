# 方法1：堆 方法二：快速排序（推荐）

[题目链接](https://leetcode.com/problems/kth-largest-element-in-an-array/description/)

## 题目简介
```
Find the kth largest element in an unsorted array. Note that it is the kth largest element in the sorted order, not the kth distinct element.
Example 1:
Input: [3,2,1,5,6,4] and k = 2
Output: 5

Example 2:
Input: [3,2,3,1,2,4,5,5,6] and k = 4
Output: 4
Note: 
You may assume k is always valid, 1 ≤ k ≤ array's length.
```

## 方法一
```
O(N lg K) running time + O(K) memory
java没有现成的数据结构：堆
但是有优先级队列PriorityQueue，方法类似于堆
PriorityQueue是从JDK1.5开始提供的新的数据结构接口，它是一种基于优先级堆的极大优先级队列。优先级队列是不同于先进先出队列的另一种队列。每次从队列中取出的是具有最高优先权的元素。如果不提供Comparator的话，优先队列中元素默认按自然顺序排列，也就是数字默认是小的在队列头。
采用升序优先级队列，遍历nums，插入队列，如果队列的大小大于k的话，就把堆顶（即队列头部元素即最小的元素删除），这样子遍历下来的话，留下来的就是最大的k个元素，而队列头便是要求的值。

```
![](https://github.com/only-you/-/blob/master/picture/priorityQueue.png)

## 方法二
```
（利用快排的分区函数确定的下标来判断其是第几大）
O(N) best case / O(N^2) worst case running time + O(1) memory
```
![](https://github.com/only-you/-/blob/master/picture/kthMax.png)

from typing import List
import heapq

Python的版本

class Solution:

    # 使用容量为 k 的小顶堆
    # 元素个数小于 k 的时候，放进去就是了
    # 元素个数大于 k 的时候，小于等于堆顶元素，就扔掉，大于堆顶元素，就替换

    def findKthLargest(self, nums: List[int], k: int) -> int:
        size = len(nums)
        if k > size:
            raise Exception('程序出错')

        L = []
        for index in range(k):
            # heapq 默认就是小顶堆
            heapq.heappush(L, nums[index])

        for index in range(k, size):
            top = L[0]
            if nums[index] > top:
                # 看一看堆顶的元素，只要比堆顶元素大，就替换堆顶元素
                heapq.heapreplace(L, nums[index])
        # 最后堆顶中的元素就是堆中最小的，整个数组中的第 k 大元素
        return L[0]


