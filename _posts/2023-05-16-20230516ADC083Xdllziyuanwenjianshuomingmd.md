---
layout: post
title: "ADC083Xdll 资源文件说明"
date:   2020-03-01
tags: [ADC083X,Proteus,dll,文件,DLL]
comments: true
author: admin
---
# ADC083X.dll 资源文件说明

## 简介

本仓库提供了一个名为 `ADC083X.dll` 的资源文件，该文件主要用于解决在 Proteus 仿真软件中遇到的特定报错问题。具体来说，当 Proteus 仿真时提示“External model DLL ‘ADC083X.DLL’ not found. GLE=0x000036B1.”错误时，可以通过下载并使用本仓库中的 `ADC083X.dll` 文件来解决该问题。

## 问题描述

在使用 Proteus 进行仿真时，可能会遇到以下报错信息：

```
External model DLL “ADC083X.DLL“ not found. GLE=0x000036B1.
```

该错误提示表明 Proteus 无法找到所需的 `ADC083X.DLL` 文件，导致仿真无法正常进行。

## 解决方案

为了解决上述问题，您可以按照以下步骤操作：

1. **下载 `ADC083X.dll` 文件**：
   - 点击本仓库中的 `ADC083X.dll` 文件进行下载。

2. **将文件放置到正确的目录**：
   - 将下载的 `ADC083X.dll` 文件放置到 Proteus 安装目录下的 `MODELS` 文件夹中。例如，如果您的 Proteus 安装在 `C:\Program Files (x86)\Labcenter Electronics\Proteus 8 Professional` 目录下，则应将 `ADC083X.dll` 文件放置到 `C:\Program Files (x86)\Labcenter Electronics\Proteus 8 Professional\MODELS` 目录中。

3. **重新启动 Proteus**：
   - 关闭并重新启动 Proteus 仿真软件，以确保更改生效。

## 参考链接

有关该问题的详细解决步骤和更多信息，请参考以下博文链接：

[【Protues报错】protues仿真报错提示“External model DLL “ADC083X.DLL“ not found. GLE=0x000036B1.” 的问题的解决](https://blog.csdn.net/weixin_42640280/article/details/129099693?spm=1001.2014.3001.5502)

## 贡献

如果您有任何改进建议或发现了新的问题，欢迎提交 Issue 或 Pull Request。我们非常欢迎社区的贡献和反馈。

## 许可证

本仓库中的资源文件遵循相应的开源许可证。具体许可证信息请参考文件本身的说明或联系仓库维护者。

---

希望本仓库提供的 `ADC083X.dll` 文件能帮助您顺利解决 Proteus 仿真中的报错问题。如有任何疑问，请随时联系我们。

## 下载链接

[ADC083X.dll资源文件说明](https://pan.quark.cn/s/87f98a0ffd8d)