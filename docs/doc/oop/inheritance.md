---
title: 继承与多态
icon: material/call-split
---

# :material-call-split:<br>继承与多态

!!! tip "官方教程"

    请参阅 [**Python 教程 » 9. 类 » 9.5. 继承**](https://docs.python.org/zh-cn/3/tutorial/classes.html#inheritance){target="_blank"}。  
    如果官方教程较为困难，请直接阅读本页面。

    :material-timer-sand: 预计阅读时间：10 分钟
    {style="font-size: 0.8em"}

在面向对象编程中，继承是一种重要的特性。它允许我们定义一个新的类，从一个或多个现有的类中继承属性和方法。被继承的类称为**基类**（或**父类**），新的类称为**派生类**（或**子类**）。

## 继承

在 Python 中，继承的语法如下：

``` python
class BaseClass:
    pass

class DerivedClass(BaseClass):
    pass
```

在上述代码中，`DerivedClass` 继承了 `BaseClass` 的所有属性和方法。这意味着，`DerivedClass` 可以使用 `BaseClass` 中定义的所有属性和方法。

## 多态

多态是面向对象编程的另一个重要特性。它允许我们使用相同的方法名，但是在不同的类中有不同的实现。

在 Python 中，多态的实现非常简单。只需要定义一个方法，然后在不同的类中实现不同的行为即可。

``` python
class Animal:
    def speak(self):
        pass

    def happy(self):
        pass

class Dog(Animal):
    def speak(self):
        print("汪汪叫")

    def happy(self):
        print("小狗摇尾巴")

class Cat(Animal):
    def speak(self):
        print("喵喵叫")

    def happy(self):
        print("小猫蹦蹦跳")
```

在上述代码中，`Dog` 和 `Cat` 类都继承了 `Animal` 类，并且都实现了 `speak` 方法。但是它们的实现是不同的，这就是多态的体现。

多态的好处在于，我们可以使用相同的方法名，但是在不同的类中有不同的实现。这样，我们就可以在不同的类中使用相同的方法名，而不需要关心具体的实现。

例如：

``` python
def speak_happily(animal: Animal) -> None:
    animal.speak()
    animal.happy()
```

在上述代码中，`speak_happily` 方法接收一个 `Animal` 类型的实例，并且调用了 `speak` 和 `happy` 方法。这样，我们就可以在不同的类中使用相同的方法名，而不需要关心具体的实现。
