---
layout: post
title: "Microsoft Visual C 140 安装解决方案
date   20220706
tags 安装MicrosoftVisualC140
comments true
author admin

 Microsoft Visual C 140 安装解决方案

 简介

本资源文件提供了针对Microsoft Visual C 140 is required问题的解决方案该问题通常出现在Windows环境下当用户尝试安装某些Python包特别是包含C扩展的包如NumpyScipy或Pandas时系统会提示缺少Microsoft Visual C 140编译环境

 问题描述

在使用Python进行开发时尤其是在Windows系统上安装某些依赖包时可能会遇到以下错误提示


error Microsoft Visual C 140 is required Get it with Microsoft Visual C Build Tools"
date:   2022-07-06
tags: [安装,Microsoft,Visual,C++,14.0]
comments: true
author: admin
---
# Microsoft Visual C++ 14.0 安装解决方案

## 简介

本资源文件提供了针对“Microsoft Visual C++ 14.0 is required”问题的解决方案。该问题通常出现在Windows环境下，当用户尝试安装某些Python包（特别是包含C扩展的包，如Numpy、Scipy或Pandas）时，系统会提示缺少Microsoft Visual C++ 14.0编译环境。

## 问题描述

在使用Python进行开发时，尤其是在Windows系统上，安装某些依赖包时可能会遇到以下错误提示：

```
error: Microsoft Visual C++ 14.0 is required. Get it with "Microsoft Visual C++ Build Tools"
```

这表明系统缺少必要的C++编译环境，导致无法成功安装所需的Python包。

## 解决方案

为了解决这个问题，我们提供了以下两种解决方案：

### 方案一：下载离线安装包

1. 下载提供的离线安装包（2选1即可）：
   - 百度网盘链接: [下载链接]
   - 超星云盘免登录高速下载链接（分为2卷，都要下载，下载后要放在一个文件夹）：
     - 1卷：msbulidtools.z01
     - 主卷：msbulidtools.zip

2. 下载后将`msbulidtools.zip`后缀改为`zip`，解压后双击`VisualCppBuildTools_Full.exe`即可成功安装。

### 方案二：安装Visual Studio Build Tools

1. 访问Microsoft官方网站，下载并安装Visual Studio Build Tools。
2. 在安装过程中，确保选择安装MSVC v142和Windows 10 SDK。
3. 安装完成后，重启电脑，再次尝试安装Python包。

## 使用说明

1. 根据上述方案选择一种方法进行安装。
2. 安装完成后，重新运行`pip install`命令，确保问题已解决。

## 注意事项

- 安装过程中请确保网络连接稳定，避免下载中断。
- 安装完成后，建议重启电脑以确保所有环境变量生效。

通过以上步骤，您应该能够成功解决“Microsoft Visual C++ 14.0 is required”问题，顺利安装所需的Python包。

## 下载链接

[MicrosoftVisualC14.0安装解决方案分享](https://pan.quark.cn/s/5945fd3263ed)