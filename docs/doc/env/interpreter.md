---
title: 安装 Python 解释器
icon: material/download-box
---

# :material-download-box:<br>安装 Python 解释器

!!! abstract "关于本节"

    Python 是一门[解释型语言](https://en.wikipedia.org/wiki/Interpreter_(computing)){target="_blank"}，我们需要安装 Python 解释器来执行 Python 代码。

    本节指导安装 Python 最新发行版的官方解释器。

## :material-download-outline: 下载

=== ":simple-windows: Windows"

    === "使用 `winget` (建议)"

        如果你的 Windows 10 / 11 近期已更新，你可以直接使用 `winget` 安装 Python 解释器。

        [以管理员权限](./terminal.md#admin-permission){target="_blank"}打开[终端](./terminal.md){target="_blank"}，输入并执行以下命令：

        ``` bash
        winget install -e --id Python.Python.3.12 --scope machine
        ```

    === "手动下载"

        <div class="annotate" markdown>

        1. 访问 [Python Releases for Windows | Python.org](https://www.python.org/downloads/windows/){target="_blank"}；
        2. 点击 `Python Releases for Windows` 下方的 `Latest Python 3 Release - Python 3.x.y`；
        3. 滚动至页面底部，在 `Files` 下方的表格中，点击 `Windows installer (64-bit)`；(1)
        4. 此时浏览器将会创建文件名为 `python-3.x.y-amd64.exe` 的下载任务。

        </div>

        5. 基于当前绝大多数个人计算机是 AMD64 (x86 64-bit) 架构的。  
        请根据你的计算机实际架构选择合适的安装程序。

=== ":simple-linux: Linux"

    !!! success "跳过此步"

        Python 预装在大多数 Linux 发行版上。请直接跳转至[验证](#验证)步骤。

        如有特殊需求，请参阅[官方文档](https://docs.python.org/3/using/unix.html){target="_blank"}。

## :material-package-variant: 安装

=== ":simple-windows: Windows"

    === "使用 `winget` (建议)"

        使用 `winget` 安装的 Python 解释器会自动添加到系统环境变量中。

        此外，我们建议取消 Windows 的路径长度限制。

        [以管理员权限](./terminal.md#admin-permission){target="_blank"}打开[终端](./terminal.md){target="_blank"}，输入并执行以下命令：

        ``` bash
        Set-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" -Name LongPathsEnabled -Value 1 -Force
        ```

    === "手动下载"

        1. 运行已下载的安装程序；
        2. 勾选下方的 `Add python.exe to PATH` 选项；
        3. 点击 `Install Now`；
        4. 等待安装完成；
        5. (建议) 点击 `Disable path length limit`；
        6. 点击 `Close`。

=== ":simple-linux: Linux"

    !!! success "跳过此步"

        Python 预装在大多数 Linux 发行版上。请直接跳转至[验证](#验证)步骤。

        如有特殊需求，请参阅[官方文档](https://docs.python.org/3/using/unix.html){target="_blank"}。

## :material-check-outline: 验证

=== ":simple-windows: Windows"

    打开[终端](./terminal.md){target="_blank"}，输入并执行以下命令：

    ``` bash
    python --version
    ```

    如果输出 `Python 3.x.y`，则安装成功。

=== ":simple-linux: Linux"

    打开[终端](./terminal.md){target="_blank"}，输入并执行以下命令：

    ``` bash
    python3 --version
    ```

    如果输出 `Python 3.x.y`，则安装成功。
