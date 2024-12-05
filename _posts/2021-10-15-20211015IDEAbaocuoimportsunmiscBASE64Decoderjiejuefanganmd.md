---
layout: post
title: "IDEA报错import sunmiscBASE64Decoder 解决方案"
date:   2022-11-17
tags: [misc,sun,BASE64Decoder,JDK,IDEA]
comments: true
author: admin
---
# IDEA报错：import sun.misc.BASE64Decoder 解决方案

## 简介

本仓库提供了一个解决方案，用于解决在IntelliJ IDEA中导入`sun.misc.BASE64Decoder`时出现的“Cannot resolve symbol 'BASE64Decoder'”错误。该错误通常是由于JDK版本升级导致的，特别是在JDK 9及以上版本中，`sun.misc.BASE64Decoder`和`sun.misc.BASE64Encoder`不再可用。

## 问题描述

在JDK 9及以上版本中，`sun.misc.BASE64Decoder`和`sun.misc.BASE64Encoder`被标记为不推荐使用，因此在导入这些类时会出现“Cannot resolve symbol”错误。

## 解决方案

本仓库提供了两种解决方案：

### 方案一：更换JDK版本

将JDK版本降级到JDK 8，因为在JDK 8中，`sun.misc.BASE64Decoder`和`sun.misc.BASE64Encoder`仍然可用。

### 方案二：手动导入jar包

1. 下载`BASE64Decoder.jar`文件。
2. 将下载的jar文件保存到指定位置。
3. 在IDEA中，右键点击项目，选择`Open Module Settings`。
4. 选择刚才下载的jar包，点击`Apply`。
5. 导入成功，问题解决。

## 使用方法

1. 克隆本仓库到本地。
2. 根据需要选择合适的解决方案。
3. 按照解决方案中的步骤进行操作。

## 注意事项

- 如果选择方案二，请确保下载的jar包与项目兼容。
- 建议在生产环境中使用`java.util.Base64`类进行Base64编码和解码，而不是依赖于`sun.misc`包中的类。

## 参考资料

- [CSDN博客：IDEA报错：import sun.misc.BASE64Decoder](https://blog.csdn.net/qq_40301475/article/details/116081669)

## 贡献

欢迎提交问题和改进建议。

## 下载链接

[IDEA报错importsun.misc.BASE64Decoder解决方案](https://pan.quark.cn/s/5caf4ed84c7f)