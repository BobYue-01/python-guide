---
title: 类与对象
icon: material/cube-outline
---

# :material-cube-outline:<br>类与对象

!!! tip "官方教程"

    请参阅 [**Python 教程 » 9. 类 » 9.3. 初探类**](https://docs.python.org/zh-cn/3/tutorial/classes.html#a-first-look-at-classes){target="_blank"}。

    :material-timer-sand: 预计阅读时间：10 分钟
    {style="font-size: 0.8em"}

如果你暂时对类和对象的概念感到困惑，不用担心，这是一个普遍的现象。

为了更好地理解类和对象，我们可以作如下类比：

| 类 | 属性 | 方法 | 对象 |
| --- | --- | --- | --- |
| 狗 | 品种、年龄、名称…… | 吠叫、摇尾巴、跑…… | 一只哈士奇（4 岁，旺财）<br>一只巴哥犬（8 岁，小李） |
| 车 | 品牌、型号、牌号…… | 加速、刹车、转弯…… | 一辆奔驰（S 级，京 A 12345）<br>一辆宝马（X5，京 B 67890） |

在 Python 中，上述类比可以这样表示：

```python
class Dog:
    def __init__(self, breed, age, name):
        self.breed = breed
        self.age = age
        self.name = name
        print(f"一只 {self.breed}（{self.age} 岁，{self.name}）已经创建")

    def bark(self):
        print(f"{self.name} 汪汪叫")

    def wag_tail(self):
        print(f"{self.name} 摇尾巴")

    def run(self):
        print(f"{self.name} 跑")

my_husky = Dog("哈士奇", 4, "旺财")
my_pug = Dog("巴哥犬", 8, "小李")

my_husky.bark()
my_pug.wag_tail()
```

其输出结果为：

```plaintext
一只 哈士奇（4 岁，旺财）已经创建
一只 巴哥犬（8 岁，小李）已经创建
旺财 汪汪叫
小李 摇尾巴
```

在上述代码中，`Dog` 是一个类，`my_husky` 和 `my_pug` 是两个对象。

在类中，`__init__` 方法是一个特殊的方法，用于初始化对象的属性。它在对象创建时自动调用。

在上述代码中，`__init__` 方法接收 4 个参数，其中 `self` 是一个特殊的参数，用于指代对象本身。因此，在初始化对象时，我们只需要传入后 3 个参数。
