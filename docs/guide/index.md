---
title: 教程
icon: material/map
---

# :material-map:<br>教程

## 差异速览

!!! Example "关于本页"

    本页内容主要介绍 Python 与 C 等语言的差异，以便于读者快速了解 Python 的特点。读者不必深究本页内容，可继续阅读后续章节。

与 C 语言相比，Python 的语法更加简洁，贴近自然语言。Python 的语法有如下的差异：

**动态类型**

:   变量不需要声明类型，Python 会根据赋值自动推断变量类型，且可以随时自动转换。

    ``` python
    a = 1           # 变量 a 被赋值为整数 1
    print(type(a))      # 当前变量 a 的类型: <class 'int'>
    a /= 2          # / 是除法运算符，返回浮点数
    print(a)            # 当前变量 a 的值: 0.5
    print(type(a))      # 当前变量 a 的类型: <class 'float'>
    ```

**缩进控制作用域**

:   代码块作用域使用缩进来控制，而不是使用大括号。缩进的空格数以一个文件中首个缩进为基准，通常为 4 个空格或 1 个制表符。

    ``` python
    for i in range(4):
        if i % 2 == 0:
            print(f'{i} is even')
        else:
            print(f'{i} is odd')
    ```

**多重赋值**

:   可以同时给多个变量赋值。这为交换变量值提供了一种简洁的方式。

    ``` python
    a, b = 1, 2
    print(a, b)     # 1 2
    a, b = b, a
    print(a, b)     # 2 1
    ```

**列表推导式**

:   可以使用列表推导式来生成列表。列表推导式是一种简洁的方式，用于根据现有列表生成新列表。

    ``` python
    squares = [i ** 2 for i in range(5)]
    print(squares)  # [0, 1, 4, 9, 16]
    ```
