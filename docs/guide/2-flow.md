---
title: Day 2：流程控制
---

# Day 2<br>**流程控制**

!!! abstract "关于本章"

    本章「流程控制」将介绍 Python 的流程控制语句，包括条件语句、循环语句等。

!!! tip "文档"

    请花费约 15 分钟阅读[**流程控制**](../doc/syntax/flow.md){target="_blank"}。

!!! question "小测：条件语句"

    请使用 Python 编写一个函数 `is_prime(n: int) -> bool`，判断一个整数 `n` 是否为素数。

    提示：素数是指除了 1 和自身外，没有其他正因数的数。

    <!--
    ``` python
    def is_prime(n: int) -> bool:
        if n < 2:
            return False
        for i in range(2, int(n ** 0.5) + 1):
            if n % i == 0:
                return False
        return True
    print(is_prime(2))   # True
    print(is_prime(4))   # False
    print(is_prime(7))   # True
    print(is_prime(9))   # False
    ```
    -->

!!! question "小测：列表推导式"

    请使用 Python 的[嵌套列表](https://docs.python.org/zh-cn/3/tutorial/introduction.html#lists:~:text=%E8%BF%98%E5%8F%AF%E4%BB%A5-,%E5%B5%8C%E5%A5%97%E5%88%97%E8%A1%A8,-%EF%BC%88%E5%88%9B%E5%BB%BA%E5%8C%85%E5%90%AB%E5%85%B6%E4%BB%96){target="_blank"}生成一个 $10\times 10$ 的矩阵，其中矩阵的每个元素为其行列索引的积。

    即：
    $$
    \begin{bmatrix}
    0 & 0 & 0 & \cdots & 0 \\\
    0 & 1 & 2 & \cdots & 9 \\\
    0 & 2 & 4 & \cdots & 18 \\\
    \vdots & \vdots & \vdots & \ddots & \vdots \\\
    0 & 9 & 18 & \cdots & 81
    \end{bmatrix}
    $$

    提示：可行的思路包括 `for` 循环、列表推导式等。

    <!--
    ``` python
    matrix = [[i * j for j in range(10)] for i in range(10)]
    print(matrix)
    ```
    -->
