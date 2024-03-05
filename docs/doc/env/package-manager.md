# 配置 Python 包管理器

!!! abstract "关于本节"

    Python 包 (package) 是一些 Python 模块 (module) 的集合。一些知名的 Python 包包括 `numpy`、`pandas`、`matplotlib` 等。它们为 Python 扩展了丰富且方便的专业功能，使得 Python 成为了一门强大的数据分析和科学计算工具。

    Python 包管理器是用于安装、升级、卸载 Python 包的工具。

    本节将介绍如何配置 Python 包管理器。

## :simple-pypi: pip

`pip` 是 Python 包管理器的标准工具。它可以安装、升级、卸载 Python 包。

如果你安装了原生的 Python 解释器，`pip` 已经预装在你的计算机上。你可以在终端中输入以下命令验证：

```bash
pip --version
```

## :simple-anaconda: Conda

`Conda` 是一个开源的软件包管理系统和环境管理系统，用于安装多个版本的软件包并提供环境隔离，且能方便地切换。

在数据分析、科学计算和机器学习等领域，由于不同项目之间的依赖经常存在冲突，`Conda` 的环境管理功能非常有用。

### 安装

访问 [Conda Documentation](https://docs.conda.io/projects/conda/en/stable/){target="_blank"}，选择对应系统的安装指南进行安装。

### 验证

安装完成后，你可以在终端中输入并执行以下命令验证：

```bash
conda --version
```

如果输出 `conda` 的版本号，说明安装成功。