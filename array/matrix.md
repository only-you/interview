# LeetCode 54 Spiral Matrix

```
Given a matrix of m x n elements (m rows, n columns), return all elements of the matrix in spiral order.
Example 1:
Input:
[
 [ 1, 2, 3 ],
 [ 4, 5, 6 ],
 [ 7, 8, 9 ]
]
Output: [1,2,3,6,9,8,7,4,5]

Example 2:
Input:
[
  [1, 2, 3, 4],
  [5, 6, 7, 8],
  [9,10,11,12]
]
Output: [1,2,3,4,8,12,11,10,9,5,6,7]
```

# idea:
```
思路：按照矩阵的四个方向，右、下、左、上这样螺旋添加数字进入列表。T：O（n）；S:O（n）
```
![](https://github.com/only-you/interview/blob/master/picture/matrix1.png)

# 第一种写法：
![](https://github.com/only-you/interview/blob/master/picture/matrix2.png)

# 第二种写法：
![](https://github.com/only-you/interview/blob/master/picture/matrix3.png)
