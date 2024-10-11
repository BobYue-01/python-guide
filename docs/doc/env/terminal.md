---
title: 了解终端
icon: material/console
---

# :material-console:<br>了解终端 (命令行界面, CLI)

!!! abstract "关于本节"

    终端（Terminal），通常表示命令行界面（Command-Line Interface，CLI）。它是在图形用户界面得到普及之前使用最为广泛的用户界面，用户通过键盘输入指令，计算机接收到指令后，予以执行。

    在接下来的学习中，我们不可避免地需要使用终端，因此有必要了解一些基本的终端操作。

## 启动终端 {#start-terminal}

=== ":fontawesome-brands-windows: Windows"

    Windows 系统中的终端是命令提示符（Command Prompt）和 PowerShell。

    我们建议使用 PowerShell，因为它比命令提示符更加强大，具备更接近 Unix 系统的命令行工具。

    你可以通过以下方式打开 PowerShell：

    - 通过 ++win+r++ 唤起「运行」，输入 `powershell`；
    - 通过 ++win+x++ 唤起「快捷菜单」，按下 ++i++ 键；
    - 通过 ++win+s++ 唤起「搜索」，输入 `powershell`。

    在 Windows 11 中，你唤起的通常是 Windows Terminal，它集成了命令提示符、PowerShell，是一个更加美观、强大的终端工具。

    如果你当前使用的是 Windows 10，你可以通过 [Microsoft Store](https://apps.microsoft.com/detail/9n0dx20hk701){target="_blank"} 下载安装。

=== ":simple-linux: Linux"

    在大多数 Linux 发行版中，你可以通过以下方式打开终端：

    - 通过快捷键 ++ctrl+alt+t++；
    - 通过应用菜单，找到并点击 `终端`。

=== ":simple-apple: macOS"

    在 macOS 中，你可以通过以下方式打开终端：

    - 通过快捷键 ++command+space++，唤起「Spotlight」，输入 `Terminal`；
    - 通过 Finder，前往 `应用程序` -> `实用工具`，双击 `终端`。

## 基本概念

### 目录与路径

目录（Directory）是文件系统中的一种特殊文件，用于存放文件和其他目录。通俗地，目录就是我们常说的文件夹。

在终端中，你可以通过 `ls` 命令查看当前目录下的文件和目录。

路径（Path）是指文件或目录在文件系统中的位置。

#### 绝对路径

绝对路径（Absolute Path）指从文件系统的根目录开始，一直到目标文件或目录的路径。

=== ":fontawesome-brands-windows: Windows"

    在 Windows 中，根目录通常是 `C:\`。

=== ":simple-linux: Linux"

    在类 Unix 系统中，根目录通常是 `/`。

=== ":simple-apple: macOS"

    在类 Unix 系统中，根目录通常是 `/`。

#### 相对路径

相对路径（Relative Path）指从当前目录开始，一直到目标文件或目录的路径。

`..` 表示上一级目录，`.` 表示当前目录，`/` 表示目录的分隔符。

### 用户目录

用户目录（User Directory）是指当前用户的个人目录。它通常用 `~` 表示，例如 `~/Documents` 表示当前用户的 `Documents` 目录。

=== ":fontawesome-brands-windows: Windows"

    在 Windows 中，用户目录通常是 `C:\Users\用户名`。

=== ":simple-linux: Linux"

    在 Linux 中，用户目录通常是 `/home/用户名`。

=== ":simple-apple: macOS"

    在 macOS 中，用户目录通常是 `/Users/用户名`。

### 工作目录

工作目录（Working Directory）是指当前终端所在的目录。执行命令时，相对路径都是基于工作目录的。

大多数终端中，工作目录的路径通常会显示在命令行的最前面。

通常地，你打开终端时，工作目录会被设置为用户目录。

在终端中，你可以通过 `cd` 命令切换工作目录，通过 `pwd` 命令查看当前工作目录的路径。

### 管理员权限 {#admin-permission}

=== ":fontawesome-brands-windows: Windows"

    在 Windows 中，你需要以管理员权限运行终端，才能执行一些需要管理员权限的操作。

    你可以通过以下方式以管理员权限运行终端：

    - 通过 ++win+x++ 唤起「快捷菜单」，按下 ++a++ 键；
    - 通过 ++win+s++ 唤起「搜索」，输入 `powershell`，右键点击 `Windows PowerShell`，选择 `以管理员身份运行`。

=== ":simple-linux: Linux"

    在 Linux 中，你可以通过 `sudo` 命令以管理员权限运行某些命令。

    例如，你可以通过 `sudo -i` 命令切换到管理员权限的终端。
