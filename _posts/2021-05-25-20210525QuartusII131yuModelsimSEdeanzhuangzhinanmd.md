---
layout: post
title: "Quartus II 13.1与Modelsim SE的安装指南"
date:   2020-05-16
tags: [安装,Quartus,II,13.1,dll]
comments: true
author: admin
---
# Quartus II 13.1与Modelsim SE的安装指南

本资源文件提供了Quartus II 13.1和Modelsim SE的详细安装步骤，适合初学者参考。以下是安装过程的简要概述：

## 资源下载
1. **软件资源下载链接**：提取码：38ny
2. **注册资源下载链接（用于Quartus II）**：提取码：zbho
3. **注册资源下载链接（用于Modelsim）**：提取码：hi5b

## 软件安装
### 1. Quartus II 13.1的安装
- 解压 `QuartusSetup-13.1.0.162.rar` 文件。
- 运行可执行程序，按照提示点击 `next`。
- 选择安装位置和安装内容，等待安装完成。
- 最后点击 `finish` 和 `OK`。

### 2. Quartus II注册
- 将下载的注册资源放在安装目录下的 `bin64` 文件夹中。
- 在目录下找到 `sys_cpt.dll` 文件，并新建一个 `license.dat` 文件。
- 打开 `sys_cpt.dll` 文件，放入可执行程序，点击应用并保存。
- 重新打开Quartus II 13.1，选择第二个选项并点击 `OK`，完成注册。

### 3. Modelsim SE版本安装
- 解压文件并运行可执行程序。
- 选择安装位置，点击 `agree`，等待安装完成。
- 出现两次提示框并点击 `yes`，最后选择 `done`。

### 4. Modelsim注册
- 重启电脑后，打开下载的注册资源。
- 在安装目录的 `win64` 文件夹下找到 `mgls64.dll` 文件，去掉“只读”选项。
- 将 `patch_dll.bat` 和 `MentorKG.exe` 文件放入 `win64` 文件夹中，运行 `patch_dll.bat`，生成 `license` 文件。
- 在系统变量中新建环境变量 `MGLS_LICENSE_FILE`，变量值为 `LICENSE.TXT` 的路径。

通过以上步骤，您可以顺利完成Quartus II 13.1和Modelsim SE的安装与注册。

## 下载链接

[QuartusII13.1与ModelsimSE的安装指南](https://pan.quark.cn/s/9333499e862e)