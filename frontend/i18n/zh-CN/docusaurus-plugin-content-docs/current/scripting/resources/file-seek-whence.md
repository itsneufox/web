---
title: 文件定位基准
sidebar_label: 文件定位基准
description: 文件定位基准定义（用于fseek函数）
---

:::note

这些定义适用于[fseek](../functions/fseek)函数。

:::

| 定义         | 描述                                                       |
| ------------ | ---------------------------------------------------------- |
| seek_start   | 设置相对于文件起始位置的文件指针（定位参数必须为正值）     |
| seek_current | 设置相对于当前文件位置的偏移量（定位参数将叠加到当前位置） |
| seek_end     | 设置相对于文件末尾的位置（定位参数必须为零或负值）         |
