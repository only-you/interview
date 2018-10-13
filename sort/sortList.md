# 链表排序，最简单是用归并排序做，有余力可以尝试快速排序来做

[题目链接](https://leetcode.com/problems/sort-list/description/)

题目介绍：
```
Sort a linked list in O(n log n) time using constant space complexity.
Example 1:
Input: 4->2->1->3
Output: 1->2->3->4

Example 2:
Input: -1->5->3->4->0
Output: -1->0->3->4->5
```

```
第一种方法：
归并排序
计算出链表的长度，分治法，一分为二，分到直至只有一个节点，然后开始合并链表
```
![](https://github.com/only-you/-/blob/master/picture/sortlist2.png)

```
第二种方法
归并排序
非常巧妙：一个慢指针slow每走一步、一个快指针fast便走两步，通过不计算长度的方法来将链表一分为二 
合并部分一样
```
![](https://github.com/only-you/-/blob/master/picture/sortlist.png)
