---
layout: post
title: "VScode LaTeX Workshop 插件配置模板"
date:   2021-06-11
tags: [VScode,模板,LaTeX,插件,SumatraPDF]
comments: true
author: admin
---
# VScode LaTeX Workshop 插件配置模板

## 资源描述

本仓库提供了一个针对 VScode 中 LaTeX Workshop 插件的 `settings.json` 配置模板。该模板旨在帮助用户快速配置 VScode 以支持 LaTeX 文档的编写和编译。

## 安装与配置说明

### 1. 安装 TeX Live

- 安装 TeX Live 并确保其路径已添加到系统的环境变量 `PATH` 中。
- 例如，将 `E:\Asoftware\texlive\2023\bin\windows` 添加到 `PATH` 中。

### 2. 配置 VScode

- 安装 LaTeX Workshop 插件。
- 将本仓库提供的 `settings.json` 模板内容复制到 VScode 的设置文件中。

### 3. 配置 SumatraPDF

- 安装 SumatraPDF 并配置反向搜索。
- 在 SumatraPDF 的设置中，添加以下命令：
  ```
  D:/software/Microsoft VS Code/Code.exe -r -g %f:%l
  ```
  请根据实际的 VScode 安装路径进行修改。

### 4. 使用说明

- **正向搜索**：在 VScode 中使用 `Ctrl+Alt+J` 或鼠标右键选择 `syncTex from cursor`。
- **反向搜索**：先打开 SumatraPDF，然后在 VScode 中使用 `Ctrl+Alt+V` 打开 PDF 文件，在 SumatraPDF 中双击即可跳转到对应的代码位置。

## 注意事项

- 请确保所有路径与实际安装路径一致。
- 如有任何问题，请参考相关文档或社区支持。

---

希望这个模板能帮助你更高效地使用 VScode 进行 LaTeX 文档的编写和编译！

## 下载链接

[VScodeLaTeXWorkshop插件配置模板分享](https://pan.quark.cn/s/fc5f90754eff)