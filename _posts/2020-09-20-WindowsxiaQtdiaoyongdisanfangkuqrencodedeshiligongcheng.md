---
layout: post
title: "Windows下Qt调用第三方库qrencode的示例工程"
date:   2020-07-01
tags: [Qt,qrencode,示例,调用,工程]
comments: true
author: admin
---
# Windows下Qt调用第三方库qrencode的示例工程

本仓库提供了一个在Windows环境下使用Qt调用第三方库qrencode的示例工程。该示例工程包含两个子工程，分别展示了如何通过静态链接库（.a）和动态链接库（.dll）的方式调用qrencode库。

## 资源文件描述

示例工程中包含两个工程：
1. **调用静态链接库（.a）的方式**：展示了如何在Qt项目中使用静态链接库来调用qrencode库。
2. **调用动态链接库（.dll）的方式**：展示了如何在Qt项目中使用动态链接库来调用qrencode库。

示例工程中的链接资源均为相对路径，确保代码在不同环境下能够正常编译和运行。

## 环境要求

- 操作系统：Windows 10
- Qt版本：Qt 6.7、Qt 5.15 均能正常编译和运行

## 使用说明

1. **克隆仓库**：将本仓库克隆到本地。
2. **打开工程**：使用Qt Creator打开对应的工程文件（.pro）。
3. **编译运行**：根据需要选择静态链接库或动态链接库的工程进行编译和运行。

## 注意事项

- 确保Qt环境已正确配置，并且Qt Creator能够正常识别qrencode库。
- 如果遇到编译或运行问题，请检查Qt版本和操作系统环境是否符合要求。

通过本示例工程，您可以快速了解在Windows环境下如何使用Qt调用第三方库qrencode，并根据实际需求选择合适的链接方式。

## 下载链接

[Windows下Qt调用第三方库qrencode的示例工程](https://pan.quark.cn/s/2477f745f00e)