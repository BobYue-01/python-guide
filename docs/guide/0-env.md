# Day 0 - 部署环境

首先，我们需要为 Python 配置一个合适的运行环境。

## 了解终端

!!! abstract "文档"

    请花费约 5 分钟阅读[了解终端](../doc/env/terminal.md)。

!!! question "小测"

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

!!! abstract "文档"

    请花费约 5 分钟阅读[安装 Python 解释器](../doc/env/interpreter.md)。

!!! question "小测"

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