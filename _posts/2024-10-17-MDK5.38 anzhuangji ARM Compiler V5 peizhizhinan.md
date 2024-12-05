---
layout: post
title: "MDK5.38 安装及 ARM Compiler V5 配置指南"
date:   2021-07-09
tags: [ARM,Compiler,V5,安装,MDK5.38]
comments: true
author: admin
---
# MDK5.38 安装及 ARM Compiler V5 配置指南

本资源文件提供了 MDK5.38 的安装包、许可证生成工具以及 ARM Compiler V5 的安装程序。通过本指南，您可以顺利完成 MDK5.38 的安装，并配置 ARM Compiler V5 以确保代码兼容性。

## 资源内容

- **MDK5.38 安装程序**：用于安装 MDK5.38 开发环境。
- **许可证生成工具**：用于生成 MDK5.38 的许可证文件。
- **ARM Compiler V5 安装程序**：用于安装 ARM Compiler V5 编译器。

## 安装步骤

### 1. MDK5.38 安装

1. 双击运行 MDK5.38 安装程序。
2. 点击 "Next"，勾选同意软件许可协议。
3. 选择软件及 Pack 安装位置，点击 "Next"。
4. 填写信息（可随意填写），点击 "Next"。
5. 安装完成后，点击 "Finish"。

### 2. 许可证安装

1. 以管理员身份运行注册机。
2. 打开 MDK 许可证管理工具，复制 CID。
3. 将 CID 粘贴到注册机 CID 处，Target 选择 ARM，点击 "Generate"。
4. 复制生成的 LIC，粘贴到 MDK LIC 处，点击 "Add LIC"。
5. 出现 "2032" 即为注册成功。

### 3. ARM Compiler V5 安装

1. 双击运行 ARM Compiler V5 安装程序。
2. 点击 "Next"，勾选同意许可协议。
3. 修改安装位置（重要），在 MDK 安装目录 ARM 文件夹下新建一个 AC5 文件夹，将 ARM Compiler V5 安装在这里。
4. 点击 "Next"，点击 "Install" 开始安装。
5. 安装完成后点击 "Finish"。

### 4. 配置 ARM Compiler V5

1. 打开 MDK，点击 "添加另一个 ARM Compiler"。
2. 选择 ARM Compiler V5 安装目录，可以看到 AC 5.06 已添加成功，点击 "Close"。
3. 按以下步骤选择使用 AC5 编译器即可。

## 注意事项

- 安装过程中请确保网络连接稳定，以便下载必要的组件。
- 在安装 ARM Compiler V5 时，请确保选择正确的安装路径，以避免兼容性问题。

通过以上步骤，您可以顺利完成 MDK5.38 的安装及 ARM Compiler V5 的配置，开始您的嵌入式开发工作。

## 下载链接

[MDK5.38安装及ARMCompilerV5配置指南](https://pan.quark.cn/s/5c5660f3fcc3)