---
title: Day 1：内置类型
---

# Day 1<br>**内置类型**<p style="font-size: 0.5em"> :material-timer-sand: 预计阅读时间：30 分钟 </p>

!!! abstract "关于本章"

    本章「内置类型」将介绍 Python 的常用内置类型，包括数字、字符串、列表、元组、字典等。

!!! tip "文档"

    请阅读[**内置类型**](../doc/syntax/stdtypes.md){target="_blank"}。

    :material-timer-sand: 预计阅读时间：25 分钟
    {style="font-size: 0.8em"}

!!! question "小测：内置类型综合应用"

    目标检测模型通常包含多个评估指标，包括准确率（accuracy）、精确率（precision）、召回率（recall）和 F1 值（F1 score）。

    你现有一个字典 `metrics`，其中包含这些评估指标以列表存储的几条历史记录。且有一对元组，用于记录评估指标的多语言名称。

    ``` python
    metrics = {
        'accuracy': [0.9, 0.91, 0.92, 0.93, 0.94],
        'precision': [0.85, 0.86, 0.87, 0.88, 0.89],
        'recall': [0.8, 0.81, 0.82, 0.83, 0.84],
        'f1': [0.75, 0.76, 0.77, 0.78, 0.79]
    }
    metric_names_en = ('accuracy', 'precision', 'recall', 'f1')
    metric_names_ch = ('准确率', '精确率', '召回率', 'F1 值')
    ```

    请输出这些评估指标的最新值。格式如下：

    ``` plain
    准确率：0.94
    精确率：0.89
    召回率：0.84
    F1 值：0.79
    ```

    提示：可以使用 `zip` 函数将两个列表打包成元组。

    ``` python
    for name_en, name_ch in zip(metric_names_en, metric_names_ch):
        print(...)
    ```

    <!--
    ``` python
    for name_en, name_ch in zip(metric_names_en, metric_names_ch):
        print(f'{name_ch}：{metrics[name_en][-1]}')
    ```
    -->