---
layout: post
title: "STM32G474 CANFD 测试用例资源文件"
date:   2024-10-23
tags: [CANFD,测试用例,文件,STM32G474,stm32g4]
comments: true
author: admin
---
# STM32G474 CANFD 测试用例资源文件

## 简介

本仓库提供了一个名为 `stm32g4_canfd.zip` 的资源文件，该文件包含了针对 STM32G474 微控制器的 CANFD 测试用例。该测试用例特别添加了 Bus-Off 处理功能，并配置了以下参数：

- **仲裁段**：500K
- **仲裁段采样点**：0.8
- **数据段**：2M
- **数据段采样点**：0.75

## 文件内容

`stm32g4_canfd.zip` 文件中包含了以下内容：

1. **源代码**：用于配置和测试 CANFD 功能的源代码文件。
2. **配置文件**：包含 CANFD 的配置参数，如波特率、采样点等。
3. **文档**：详细说明如何使用该测试用例的文档。

## 使用说明

1. **下载文件**：点击仓库中的 `stm32g4_canfd.zip` 文件进行下载。
2. **解压缩**：将下载的 ZIP 文件解压缩到本地目录。
3. **导入工程**：将解压后的文件导入到你的 STM32CubeIDE 或其他 STM32 开发环境中。
4. **配置参数**：根据需要调整 CANFD 的配置参数。
5. **编译与烧录**：编译代码并将其烧录到 STM32G474 微控制器中。
6. **测试**：运行测试用例，验证 CANFD 功能是否正常工作。

## 参考资料

本测试用例的详细说明和配置方法可以参考以下博客文章：

[STM32G474 CANFD 用例详解](https://example.com/blog-link)

## 贡献

如果你有任何改进建议或发现了问题，欢迎提交 Issue 或 Pull Request。

## 许可证

本项目采用 MIT 许可证，详情请参阅 [LICENSE](LICENSE) 文件。

## 下载链接

[STM32G474CANFD测试用例资源文件](https://pan.quark.cn/s/d8bbbac4ec71)