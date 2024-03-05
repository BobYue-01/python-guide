---
title: Day 0：部署环境
---

# Day 0<br>**部署环境**

!!! abstract "关于本章"

    首先，我们需要为 Python 配置一个合适的运行环境。

    本章「部署环境」将介绍如何准备 Python 编程环境，包括 Python 解释器、编辑器、包管理器等。

## 了解终端

!!! info "跳过此节"

    如果你能直接完成下面的小测，可以跳过此节。

!!! tip "文档"

    请花费约 5 分钟阅读[**了解终端**](../doc/env/terminal.md)。

!!! question "小测：终端"

    请打开终端，输入并执行以下命令：

    ``` bash
    mkdir ./hello
    cd ./hello
    echo "Hello, World!" >> world.txt
    ```

    请问，这段命令的作用是什么？（提示：可以使用 `cat world.txt` 查看文件内容）

    <!--
    - [ ] 输出 `Hello, World!` 到终端
    - [ ] 输出 `Hello, World!`，将其追加到 `world.txt`
    - [ ] 输出 `Hello, World!`，将其覆盖到 `world.txt`
     -->

    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-0-option-0" class="mdl-radio__button" name="quiz-0-0" value="输出 `Hello, World!` 到终端">
      <span class="mdl-radio__label">输出 `Hello, World!` 到终端</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-0-option-1" class="mdl-radio__button" name="quiz-0-0" value="输出 `Hello, World!`，将其追加到 `world.txt`">
      <span class="mdl-radio__label">输出 `Hello, World!`，将其追加到 `world.txt`</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-0-option-2" class="mdl-radio__button" name="quiz-0-0" value="输出 `Hello, World!`，将其覆盖到 `world.txt`">
      <span class="mdl-radio__label">输出 `Hello, World!`，将其覆盖到 `world.txt`</span>
    </label>

## 安装 Python 解释器

!!! info "跳过此节"

    如果你已经安装了较新的 Python 解释器，或者你将使用 Conda / Miniconda / Anaconda 等环境，可以跳过此节。

!!! tip "文档"

    请花费约 5 分钟阅读[**安装 Python 解释器**](../doc/env/interpreter.md)。

!!! question "小测：交互式命令行"

    请进入 Python 交互式环境，输入并执行以下命令：

    ``` python
    import this
    ```

    此时你将会看到诗作 *The Zen of Python*「Python 之禅」。请问，这段诗的作者是谁？

    <!-- 
    - [ ] Guido van Rossum
    - [ ] Tim Peters
    - [ ] Alex Martelli
    - [ ] Raymond Hettinger
    - [ ] Rick Astley
     -->

    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-1-option-0" class="mdl-radio__button" name="quiz-0-1" value="Guido van Rossum">
      <span class="mdl-radio__label">Guido van Rossum</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-1-option-1" class="mdl-radio__button" name="quiz-0-1" value="Tim Peters">
      <span class="mdl-radio__label">Tim Peters</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-1-option-2" class="mdl-radio__button" name="quiz-0-1" value="Alex Martelli">
      <span class="mdl-radio__label">Alex Martelli</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-1-option-3" class="mdl-radio__button" name="quiz-0-1" value="Raymond Hettinger">
      <span class="mdl-radio__label">Raymond Hettinger</span>
    </label>
    <br>
    <label class="mdl-radio mdl-js-radio mdl-js-ripple-effect">
      <input type="radio" id="quiz-0-1-option-4" class="mdl-radio__button" name="quiz-0-1" value="Rick Astley">
      <span class="mdl-radio__label">Rick Astley</span>
    </label>

## 选择并配置集成开发环境 (IDE)

!!! info "跳过此节"

    如果你已经选择了合适的集成开发环境 (IDE)，可以跳过此节。

!!! tip "文档"

    请花费约 5 分钟阅读[**选择并配置集成开发环境 (IDE)**](../doc/env/ide/index.md)。

!!! question "小测：IDE"

    使用你选择的集成开发环境 (IDE)，请完成以下任务：

    1. 创建一个新的 Python 文件 `hello.py`
    2. 在文件中输入以下代码：
    ``` python
    print("Hello, World!")
    ```
    3. 运行该文件，查看输出结果

!!! question "小测：Jupyter Notebook"

    使用你选择的集成开发环境 (IDE)，请完成以下任务：

    1. 创建一个新的 Jupyter Notebook
    2. 在第一个单元格中输入以下代码：
    ``` python
    print("Hello, World!")
    ```
    3. 运行该单元格，查看输出结果
