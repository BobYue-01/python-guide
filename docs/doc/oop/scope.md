---
title: 作用域与命名空间
icon: material/variable
---

# :material-variable:<br>作用域与命名空间

!!! tip "官方教程"

    请参阅 [**Python 教程 » 9. 类 » 9.2. Python 作用域和命名空间**](https://docs.python.org/zh-cn/3/tutorial/classes.html#python-scopes-and-namespaces){target="_blank"}。  
    如果官方教程较为困难，请直接阅读本页面。

    :material-timer-sand: 预计阅读时间：5 分钟
    {style="font-size: 0.8em"}

Python 中的作用域和命名空间与 C 语言中的类似，但有一些细微的差别。在 C 语言中，作用域和命名空间是通过花括号 `{}` 来划分的，而在 Python 中则是通过缩进来划分的。

在函数内部定义的变量称为局部变量，它们的作用域仅限于函数内部。在函数外部定义的变量称为全局变量，它们的作用域则是整个程序。在函数内部可以访问全局变量，但不能修改它们。如果需要修改全局变量，可以使用 `global` 关键字来声明。

在 Python 中，变量名查找的先后顺序为：

1.  局部命名空间（从内向外）；
2.  全局命名空间；
3.  内置命名空间。

若上述命名空间中均未找到对应的变量名，则会抛出 `NameError` 异常。

``` python
x = 10        # 全局变量

def foo():
    x = 20    # 创建局部变量
    print(x)  # 20

foo()

print(x)      # 10

def bar():
    global x  # 声明 x 为全局变量
    x = 30    # 修改全局变量
    print(x)  # 30

bar()

print(x)      # 30
```

在前两次输出中，`x` 分别位于局部作用域和全局作用域中，因此输出结果为 `20` 和 `10`。在 `bar` 函数中，使用 `global` 关键字声明 `x` 为全局变量，因此输出结果为 `30` 和 `30`。
