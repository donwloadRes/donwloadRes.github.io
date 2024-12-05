---
layout: post
title: "Windchill单点登录实现方案"
date:   2020-11-03
tags: [Windchill,单点,认证,登录,方案]
comments: true
author: admin
---
# Windchill单点登录实现方案

## 资源文件描述

为了适应现代企业的系统整合需求，许多企业选择使用SSO（单点登录）来统一管理企业用户。在此背景下，我们基于Windchill的认证系统进行了重构，实现了单点登录功能，并与大家分享这一方案。

本次使用的认证系统是Windchill 10.2版本，该实现方式同样适用于Windchill 11版本，但不同版本在拦截认证信息时可能会有所不同，需要进行相应的测试。

### 测试环境

此方案已经过以下测试：
- Shell命令行
- Core认证
- WGM工具端认证
- 后台应用访问

### 自定义登录

如果需要实现自定义登录功能，也可以参考此方案。通过增加认证机制，可以进行用户注册等操作。由于安全性的考虑，请结合博客内容进行相应的修改。

### 附件内容

附件中包含了博客代码中缺少的部分内容，供大家参考和使用。

---

希望此资源文件能帮助到有需要的企业和个人，实现Windchill系统的单点登录功能。

## 下载链接

[Windchill单点登录实现方案](https://pan.quark.cn/s/245fae40dafe)