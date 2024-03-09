---
title: 内置类型
icon: material/numeric
---

# :material-numeric:<br>内置类型

!!! tip "官方教程：数字、文本、列表"

    请参阅 [**Python 教程 » 3. Python 速览**](https://docs.python.org/zh-cn/3/tutorial/introduction.html){target="_blank"}。

    :material-timer-sand: 预计阅读时间：5 分钟
    {style="font-size: 0.8em"}

## [数字类型](https://docs.python.org/zh-cn/3/library/stdtypes.html#numeric-types-int-float-complex){target="_blank"}

??? info "官方文档"

    关于数字类型的完整用法，见 [**Python 标准库 » 内置类型 » 数字类型**](https://docs.python.org/zh-cn/3/library/stdtypes.html#numeric-types-int-float-complex){target="_blank"}。

    关于数字类型的实现细节，见 [**Python 语言参考手册 » 3. 数据模型 » 3.2.4. `numbers.Number`**](https://docs.python.org/zh-cn/3/reference/datamodel.html#numbers-number){target="_blank"}。

### 整数 (`int`)

在 Python 中，整数可表示任意大小的数字，仅受限于可用的内存 (包括虚拟内存)。这是因为 Python 的整数是对象 (object)，而不是原生的机器级整型。当整数的值超出机器级整型的取值范围时，Python 会自动采用 [`long` 类型](https://github.com/python/cpython/blob/main/Include/cpython/longintrepr.h){target="_blank"}来存储。<!-- 严谨性待审查 -->

``` python
a = 1234567890123456789012345678901234567890
print(a > 1e39)  # True
a *= a
print(a)         # 1524157875323883675049535156256668194500533455762536198787501905199875019052100
```

### 浮点型 (`float`)

在 Python 中，浮点型表示机器级的双精度浮点数。其所接受的取值范围和溢出处理将受制于底层的机器架构 (以及 C 或 Java 实现)。Python 不支持单精度浮点数；支持后者通常的理由是节省处理器和内存消耗，但这点节省相对于在 Python 中使用对象的开销来说太过微不足道，因此没有理由包含两种浮点数而令该语言变得复杂。

??? question "小测：数值计算"

    黄金比例 $\phi = \frac{1 + \sqrt{5}}{2}$。请计算 $\phi$ 的值。

    ``` python
    import math
    phi = ...
    print(phi)  # 1.618033988749895
    ```

    提示：使用 `math.sqrt()` 来计算平方根。

    <!--
    ``` python
    import math
    phi = (1 + math.sqrt(5)) / 2
    print(phi)  # 1.618033988749895
    ```
    -->

??? question "小测：浮点数比较"

    请在误差阈值 $\epsilon = 1 \times 10^{-6}$ 内判断 `a` 和 `b` 是否相等。

    ``` python
    eps = 1e-6
    a = 0.1 + 0.2
    b = 0.3
    print(...)  # True
    ```

    提示：使用 `abs()` 来计算绝对值。

    注：`math.isclose()` 是 Python 3.5 引入的新函数，用于比较浮点数是否相等。它更加灵活，可以指定绝对误差和相对误差。

    <!--
    ``` python
    eps = 1e-6
    a = 0.1 + 0.2
    b = 0.3
    print(abs(a - b) < eps)  # True
    ```
    -->

## [字符串 (`str`)](https://docs.python.org/zh-cn/3/library/stdtypes.html#textseq){target="_blank"}

字符串是不可变的序列。字符串是 Unicode 字符的序列，而不是字节 (`bytes`，仅支持 0~255 的 ASCII 码) 的序列。

``` python
s = 'Hello, world! 你好，世界！'
print(s[0])  # 'H'
print(s[-2]) # '界'
s[0] = 'h'   # TypeError: 'str' object does not support item assignment
```

### 字符串格式化

在 Python 中，字符串格式化有多种方式。最简单的方式是使用 `%` 运算符。但是，更推荐使用更现代的 `f-string`。

!!! tip "官方教程：`f-string`"

    请参阅 [**Python 教程 » 7. 输入和输出 » 7.1.1. 格式化字符串字面值**](https://docs.python.org/zh-cn/3/reference/lexical_analysis.html#f-strings){target="_blank"}。

    :material-timer-sand: 预计阅读时间：5 分钟
    {style="font-size: 0.8em"}

??? question "小测：字符串格式化"

    准确率 `acc` 为 `0.952357`。请使用 `f-string` 或其他方式格式化输出 `acc` 的值，以百分比形式表示，保留 2 位小数。

    ``` python
    acc = 0.952357
    print(...)  # 95.24%
    ```

    提示：使用 `f-string` 时，可以在大括号中使用 `:.nf` 来指定 $n$ 位小数。

    <!--
    ``` python
    acc = 0.952357
    print(f'{acc:.2%}')  # 95.24%
    ```
    -->

## [列表 (`list`)](https://docs.python.org/zh-cn/3/library/stdtypes.html#lists){target="_blank"}

Python 中的简单赋值永远不会复制数据。当你将一个列表赋值给一个变量时，该变量引用现有列表。通过一个变量对列表所做的任何更改都将通过所有引用它的其他变量看到。

``` python
rgb = ["Red", "Green", "Blue"]
rgba = rgb
id(rgb) == id(rgba)  # True: 它们引用同一个对象
rgba.append("Alph")
print(rgb)           # ["Red", "Green", "Blue", "Alph"]
```

??? question "小测：翻转列表"

    请使用列表的切片操作翻转列表 `acc_history`。

    ``` python
    acc_history = [63, 81, 89, 93, 95]
    acc_history = ...
    print(acc_history)  # [95, 93, 89, 81, 63]
    ```

    提示：切片操作的语法是 `a[start:stop:step]`，其中 `start` 为起始索引，`stop` 为结束索引，`step` 为步长。默认值分别为 `0`、`len(a)` 和 `1`。

    <!--
    ``` python
    a = [1, 2, 3, 4, 5]
    a = a[::-1]
    print(a)  # [5, 4, 3, 2, 1]
    ```
    -->

## [元组 (`tuple`)](https://docs.python.org/zh-cn/3/library/stdtypes.html#tuples){target="_blank"}

!!! tip "官方教程：元组"

    请参阅 [**Python 教程 » 5. 数据结构 » 5.3. 元组和序列**](https://docs.python.org/zh-cn/3/tutorial/datastructures.html#tuples-and-sequences){target="_blank"}。

    :material-timer-sand: 预计阅读时间：5 分钟
    {style="font-size: 0.8em"}

## [字典 (`dict`)](https://docs.python.org/zh-cn/3/library/stdtypes.html#mapping-types-dict){target="_blank"}

!!! tip "官方教程：字典"

    请参阅 [**Python 教程 » 5. 数据结构 » 5.5. 字典**](https://docs.python.org/zh-cn/3/tutorial/datastructures.html#dictionaries){target="_blank"}。

    :material-timer-sand: 预计阅读时间：5 分钟
    {style="font-size: 0.8em"}

??? question "小测：字典"

    现有 3 个目标检测模型在 4 个类别上的 mAP 值，如下所示。请打印 `Model1` 在 `person` 类别上的 mAP 值，若不存在则返回 `0`。

    ``` python
    model_mAPs = {
        'Model1': {'person': 0.75, 'car': 0.82, 'dog': 0.68, 'cat': 0.73},
        'Model2': {'person': 0.80, 'car': 0.78, 'dog': 0.70},
        'Model3': {'person': 0.70, 'car': 0.85, 'dog': 0.65, 'cat': 0.72}
    }
    ```

    提示：字典的取值操作是 `d[key]`，若 `key` 不存在则会抛出 `KeyError` 异常。可以使用 `d.get(key, default)` 来避免异常。

    <!--
    ``` python
    model_mAPs = {
        'Model1': {'person': 0.75, 'car': 0.82, 'dog': 0.68, 'cat': 0.73},
        'Model2': {'person': 0.80, 'car': 0.78, 'dog': 0.70},
        'Model3': {'person': 0.70, 'car': 0.85, 'dog': 0.65, 'cat': 0.72}
    }
    print(model_mAPs['Model1'].get('person', 0))
    ```
    -->
