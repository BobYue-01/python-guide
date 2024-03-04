# 内置类型

!!! tip "官方教程"

    请参阅 [Python 教程 » 3. Python 速览](https://docs.python.org/zh-cn/3/tutorial/introduction.html)。

    你大约需要 10 分钟来阅读上述内容。本页面仅提供深入补充知识。

## [数字类型 (`numbers.Number`)](https://docs.python.org/zh-cn/3/reference/datamodel.html#numbers-number)

!!! info "官方文档"

    关于数字类型的完整用法，见 [Python 标准库 » 内置类型](https://docs.python.org/zh-cn/3/library/stdtypes.html#numeric-types-int-float-complex)。

    关于数字类型的实现细节，见 [Python 语言参考手册 » 3. 数据模型](https://docs.python.org/zh-cn/3/reference/datamodel.html#numbers-number)。

### 整数 (`int`)

在 Python 中，整数可表示任意大小的数字，仅受限于可用的内存 (包括虚拟内存)。这是因为 Python 的整数是对象 (object)，而不是原生的机器级整型。当整数的值超出机器级整型的取值范围时，Python 会自动采用 [`long` 类型](https://github.com/python/cpython/blob/main/Include/cpython/longintrepr.h)来存储。<!-- 严谨性待审查 -->

``` python
a = 1234567890123456789012345678901234567890
print(a > 1e39)  # True
a *= a
print(a)         # 1524157875323883675049535156256668194500533455762536198787501905199875019052100
```

### 浮点型 (`float`)

在 Python 中，浮点型表示机器级的双精度浮点数。其所接受的取值范围和溢出处理将受制于底层的机器架构 (以及 C 或 Java 实现)。Python 不支持单精度浮点数；支持后者通常的理由是节省处理器和内存消耗，但这点节省相对于在 Python 中使用对象的开销来说太过微不足道，因此没有理由包含两种浮点数而令该语言变得复杂。

## [字符串 (`str`)](https://docs.python.org/zh-cn/3/library/stdtypes.html#textseq)

字符串是不可变的序列。字符串是 Unicode 字符的序列，而不是字节 (`bytes`，仅支持 0~255 的 ASCII 码) 的序列。

``` python
s = 'Hello, world!'
print(s[0])  # 'H'
s[0] = 'h'   # TypeError: 'str' object does not support item assignment
```

## [列表 (`list`)](https://docs.python.org/zh-cn/3/library/stdtypes.html#list)

