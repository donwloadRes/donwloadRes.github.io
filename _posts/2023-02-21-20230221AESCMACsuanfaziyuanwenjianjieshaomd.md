---
layout: post
title: "AES-CMAC算法资源文件介绍"
date:   2020-08-19
tags: [CMAC,AES,算法,XCBC,密钥]
comments: true
author: admin
---
# AES-CMAC算法资源文件介绍

本资源文件详细介绍了AES-CMAC算法的原理与实现，并附有C语言编写的样例程序。以下是原文的简介：

美国国家标准与技术研究院（NIST）最近规定了基于密码的消息认证码（CMAC）。CMAC [NIST-CMAC] 是一种基于对称密钥分组密码（如高级加密标准 [NIST-AES]）的密钥哈希函数。CMAC 等同于 Iwata 和 Kurosawa 提交的 One-Key CBC MAC1（OMAC1）[OMAC1a OMAC1b]。OMAC1 是对 Black 和 Rogaway 提交的扩展密码分组链接模式（XCBC）的改进 [XCBCa XCBCb]，而 XCBC 本身是对基本密码分组链接消息认证码（CBC-MAC）的改进。XCBC 有效地解决了 CBC-MAC 的安全缺陷，而 OMAC1 则有效地减少了 XCBC 的密钥大小。

AES-CMAC 提供了比校验和或错误检测码更强的数据完整性保证。校验和或错误检测码只能检测到数据的意外修改，而 CMAC 旨在检测数据的意外修改和有意未经授权的修改。AES-CMAC 实现了与 HMAC [RFC-HMAC] 类似的安全目标。由于 AES-CMAC 基于对称密钥分组密码 AES，而 HMAC 基于哈希函数（如 SHA-1），因此 AES-CMAC 适用于 AES 比哈希函数更易获取的信息系统。本备忘录指定了基于 AES-128 的 CMAC 认证算法。这种新的认证算法被称为 AES-CMAC。

通过本资源文件，您将深入了解AES-CMAC算法的原理，并通过提供的C语言样例程序，掌握其实际应用。

## 下载链接

[AES-CMAC算法资源文件介绍](https://pan.quark.cn/s/b2754c5c82a1)