---
layout: post
title: "PAM交叉编译用到的源码包"
date:   2023-04-16
tags: [源码,PAM,编译,2.9,tar]
comments: true
author: admin
---
# PAM交叉编译用到的源码包

本仓库提供了一系列用于PAM（Pluggable Authentication Modules）交叉编译的源码包，这些源码包是进行PAM相关开发和集成时必不可少的资源。以下是本仓库提供的资源文件列表及其简要描述：

## 资源文件列表

1. **cracklib-2.9.7.tar.gz**
   - Cracklib是一个用于密码强度检查的库，该文件包含了Cracklib 2.9.7版本的源码。

2. **cracklib-words-2.9.7.bz2**
   - 这是Cracklib 2.9.7版本所使用的字典文件，用于密码强度检查。

3. **libpwquality-1.4.4.tar.gz**
   - libpwquality是一个用于生成和检查密码质量的库，该文件包含了libpwquality 1.4.4版本的源码。

4. **Linux-PAM-1.3.1.tar.gz**
   - Linux-PAM是Linux系统中用于认证模块的实现，该文件包含了Linux-PAM 1.3.1版本的源码。

5. **shadow-4.8.tar.gz**
   - Shadow是一组用于管理用户和组密码的工具，该文件包含了Shadow 4.8版本的源码。

## 使用说明

这些源码包适用于需要进行PAM交叉编译的开发者。你可以根据需要下载相应的源码包，并按照官方文档或相关教程进行编译和集成。

## 注意事项

- 请确保在编译前已经配置好交叉编译环境。
- 编译过程中可能会遇到依赖问题，请根据错误提示安装相应的依赖库。
- 建议在编译前阅读每个源码包的README文件，以获取更多详细信息和编译指导。

希望这些资源能够帮助你在PAM开发过程中顺利进行交叉编译。如果有任何问题或建议，欢迎提出反馈。

## 下载链接

[PAM交叉编译用到的源码包](https://pan.quark.cn/s/1c9f68eb7f1f)