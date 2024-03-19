---
title: Day 3：面向对象
---

# Day 3<br>**面向对象**<p style="font-size: 0.5em"> :material-timer-sand: 预计阅读时间：30 分钟 </p>

!!! abstract "关于本章"

    本章「面向对象」将介绍 Python 的面向对象编程（OOP）特性，包括类、对象、继承、多态等。

## 作用域与命名空间

!!! info "跳过此节"

    如果你能直接完成下面的小测，可以跳过此节。

!!! tip "文档"

    请阅读 [**:material-variable: 作用域与命名空间**](../doc/oop/scope.md){target="_blank"}。

    :material-timer-sand: 预计阅读时间：5 分钟
    {style="font-size: 0.8em"}

!!! question "小测：作用域与命名空间"

    请问，以下代码的输出是什么？

    ``` python
    x = 10

    def foo() -> None:
        x = 20
        print(x, end=' ')

    foo()
    print(x)
    ```

    <!--
    - [ ] `10 20`
    - [ ] `20 20`
    - [ ] `20 10`
    - [ ] `10 10`
    -->

    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-0-option-0" class="mdl-radio__button" name="quiz-3-0" value="`10 20`">
      <span class="mdl-radio__label">`10 20`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-0-option-1" class="mdl-radio__button" name="quiz-3-0" value="`20 20`">
      <span class="mdl-radio__label">`20 20`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-0-option-2" class="mdl-radio__button" name="quiz-3-0" value="`20 10`">
      <span class="mdl-radio__label">`20 10`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-0-option-3" class="mdl-radio__button" name="quiz-3-0" value="`10 10`">
      <span class="mdl-radio__label">`10 10`</span>
    </label>

## 类与对象

!!! tip "文档"

    请阅读 [**:material-cube-outline: 类与对象**](../doc/oop/class.md){target="_blank"}。

    :material-timer-sand: 预计阅读时间：10 分钟
    {style="font-size: 0.8em"}

!!! question "小测：类与对象"

    下面是（伪）多层感知机模型 `MLP` 的定义。

    ``` python
    class MLP:
        def __init__(self,
            input_size: int = 784,
            hidden_size: int = 256,
            output_size: int = 10
        ) -> None:
            self.input_size = input_size
            self.hidden_size = hidden_size
            self.output_size = output_size
            self.init_weights()

        def init_weights(self) -> None:
            self.weights = [
                [[0] * self.hidden_size] * self.input_size,
                [[0] * self.output_size] * self.hidden_size
            ]

        def forward(self, x) -> None:
            pass

    model = MLP(hidden_size=512)
    ```

    请问，`model.weights` 的形状是什么？即 `len(model.weights[0])`，`len(model.weights[0][0])`，`len(model.weights[1])`，`len(model.weights[1][0])` 分别是多少？

    <!--
    - [ ] `784, 256, 256, 10`
    - [ ] `784, 512, 512, 10`
    - [ ] `256, 784, 10, 256`
    - [ ] `512, 784, 10, 512`
    -->

    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-1-option-0" class="mdl-radio__button" name="quiz-3-1" value="`784, 256, 256, 10`">
      <span class="mdl-radio__label">`784, 256, 256, 10`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-1-option-1" class="mdl-radio__button" name="quiz-3-1" value="`784, 512, 512, 10`">
      <span class="mdl-radio__label">`784, 512, 512, 10`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-1-option-2" class="mdl-radio__button" name="quiz-3-1" value="`256, 784, 10, 256`">
      <span class="mdl-radio__label">`256, 784, 10, 256`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-1-option-3" class="mdl-radio__button" name="quiz-3-1" value="`512, 784, 10, 512`">
      <span class="mdl-radio__label">`512, 784, 10, 512`</span>
    </label>

## 继承与多态

!!! tip "文档"

    请阅读 [**:material-call-split: 继承与多态**](../doc/oop/inheritance.md){target="_blank"}。

    :material-timer-sand: 预计阅读时间：10 分钟
    {style="font-size: 0.8em"}

!!! question "小测：继承与多态"

    下面是（伪）模型基类 `Model` 和（伪）多层感知机模型 `MLP` 的定义。

    ``` python
    class Model:
        def __init__(self, input_size: int, output_size: int) -> None:
            self.input_size = input_size
            self.output_size = output_size

        def init_weights(self) -> None:
            self.weights = []

        def get_weights(self) -> list:
            return self.weights

        def forward(self, x) -> None:
            pass

    class MLP(Model):
        def __init__(self,
            input_size: int = 784,
            hidden_size: int = 256,
            output_size: int = 10
        ) -> None:
            super().__init__(input_size=input_size, output_size=output_size)
            self.hidden_size = hidden_size
            self.init_weights()

        def init_weights(self) -> None:
            self.weights = [
                [[0] * self.hidden_size] * self.input_size,
                [[0] * self.output_size] * self.hidden_size
            ]

        def forward(self, x) -> None:
            pass
    ```

    请问，以下代码的输出是什么？

    ``` python
    model = MLP(hidden_size=1024)
    print(model.get_weights())
    ```

    <!--
    - [ ] `[]`
    - [ ] `[[[0] * 256] * 784, [[0] * 10] * 256]`
    - [ ] `[[[0] * 512] * 784, [[0] * 10] * 512]`
    - [ ] `[[[0] * 256] * 512, [[0] * 10] * 256]`
    - [ ] `[[[0] * 512] * 512, [[0] * 10] * 512]`
    -->

    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-2-option-0" class="mdl-radio__button" name="quiz-3-2" value="`[]`">
      <span class="mdl-radio__label">`[]`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-2-option-1" class="mdl-radio__button" name="quiz-3-2" value="`[[[0] * 256] * 784, [[0] * 10] * 256]`">
      <span class="mdl-radio__label">`[[[0] * 256] * 784, [[0] * 10] * 256]`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-2-option-2" class="mdl-radio__button" name="quiz-3-2" value="`[[[0] * 512] * 784, [[0] * 10] * 512]`">
      <span class="mdl-radio__label">`[[[0] * 512] * 784, [[0] * 10] * 512]`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-2-option-3" class="mdl-radio__button" name="quiz-3-2" value="`[[[0] * 256] * 512, [[0] * 10] * 256]`">
      <span class="mdl-radio__label">`[[[0] * 256] * 512, [[0] * 10] * 256]`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-3-2-option-4" class="mdl-radio__button" name="quiz-3-2" value="`[[[0] * 512] * 512, [[0] * 10] * 512]`">
      <span class="mdl-radio__label">`[[[0] * 512] * 512, [[0] * 10] * 512]`</span>
    </label>
