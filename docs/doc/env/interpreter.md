# 安装 Python 解释器

Python 是一门[解释型语言](https://en.wikipedia.org/wiki/Interpreter_(computing))，我们需要安装 Python 解释器来执行 Python 代码。

## 下载

=== "Windows"

    <div class="annotate" markdown>

    1. 打开 [Python 官网](https://www.python.org/downloads/windows/)；
    2. 点击 `Python Releases for Windows` 下方的 `Latest Python 3 Release - Python 3.x.y`；
    3. 滚动至页面底部，在 `Files` 下方的表格中，点击 `Windows installer (64-bit)` (1) ；
    4. 此时浏览器将会创建一个下载任务。

    </div>

    1. 基于当前绝大多数个人计算机是 amd64 (x86 64-bit) 架构的。  
    请根据你的计算机实际架构选择合适的安装程序。

=== "Linux"

    !!! success "跳过此步"

        Python 预装在大多数 Linux 发行版上。请直接跳转至[验证](#验证)步骤。

        如有特殊需求，请参阅[官方文档](https://docs.python.org/3/using/unix.html)。

## 安装

=== "Windows"

    1. 运行已下载的安装程序；
    2. 勾选下方的 `Add python.exe to PATH` 选项；
    3. 点击 `Install Now`；
    4. 等待安装完成；
    5. （建议）点击 `Disable path length limit`；
    6. 点击 `Close`。

=== "Linux"

    !!! success "跳过此步"

        Python 预装在大多数 Linux 发行版上。请直接跳转至[验证](#验证)步骤。

        如有特殊需求，请参阅[官方文档](https://docs.python.org/3/using/unix.html)。

## 验证

=== "Windows"

    1. 打开命令提示符或 PowerShell 等终端；
        - 按下 ++win+r++，输入 `cmd`，按下回车。
    2. 输入 `python --version`；
    3. 如果输出 `Python 3.x.y`，则安装成功。

=== "Linux"

    1. 打开终端；
    2. 输入 `python3 --version`；
    3. 如果输出 `Python 3.x.y`，则安装成功。
