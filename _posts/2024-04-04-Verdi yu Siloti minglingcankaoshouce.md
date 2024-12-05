---
layout: post
title: "Verdi 与 Siloti 命令参考手册"
date:   2020-12-12
tags: [Verdi,波形,fsdb,参考手册,Siloti]
comments: true
author: admin
---
# Verdi 与 Siloti 命令参考手册

## 资源文件描述

本资源文件为《Verdi 与 Siloti 命令参考手册》，基于最新版本 U-2023.03，发布于2023年3月。该手册主要面向 Verdi 用户，详细介绍了如何使用 Verdi 生成 fsdb 模型，并提供了与 VCS 使用的 vcd 文件相比的优劣势分析。

## 内容概述

Verdi 是一款广泛应用于 RTL 代码调试的工具，主要用于生成 fsdb 模型。与 VCS 使用的 vcd 文件相比，Verdi 使用的 fsdb 文件相当于经过霍夫编码压缩后的精简版，更适合用于查看 fsdb 波形并追踪 RTL 代码。

### Verdi 与 Modelsim 的比较

虽然 Verdi 和 Modelsim 都是用于调试波形的工具，但两者之间存在显著差异。Modelsim 的主要缺点是波形不会全 dump，如果 wave 窗口拉不全，需要重新运行仿真。而 Verdi 则支持边运行边查看波形，通过使用 tcl 指令设置仿真时间，每次 run 完毕后，可以在 nWave 窗口中通过 file -> 自动加载（快捷键 shift+L）来加载波形，操作异常方便。

## 使用说明

本手册详细介绍了 Verdi 的各种命令和操作方法，帮助用户更好地理解和使用 Verdi 工具。无论是初学者还是有经验的用户，都能从中获得有价值的信息。

## 适用人群

- RTL 代码调试工程师
- 硬件设计与验证工程师
- 对 Verdi 工具感兴趣的开发者

## 版本信息

- 版本：U-2023.03
- 发布日期：2023年3月

希望本手册能帮助您更好地使用 Verdi 工具，提升工作效率。

## 下载链接

[Verdi与Siloti命令参考手册](https://pan.quark.cn/s/e2d5a1d4b68e)