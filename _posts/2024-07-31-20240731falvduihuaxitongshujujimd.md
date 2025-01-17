---
layout: post
title: "法律对话系统数据集"
date:   2022-10-14
tags: [对话,文件,测试,资源,test]
comments: true
author: admin
---
# 法律对话系统数据集

## 描述

本仓库提供了一个法律对话系统的资源文件，包括源代码和语言资源。该资源文件旨在支持法律服务对话系统的开发与测试。仓库中包含了FAQ、FF、重启和问候语处理程序的代码，以及专门为法律领域设计的各种语言资源，如训练数据集和会话测试集。

`session_test_set.xlsx` 文件包含了旨在测试用户与对话系统之间所有可能的唯一对话的对话流。每个对话流都是一个由多个句子组成的多轮对话。电子表格中的奇数标签由包含偶数标签及其各自意图的对话组成。

`test_unseen_sent.py` 脚本用于测试每个对话并生成报告，显示系统正确识别的对话数。在测试对话之前，会话将重新启动。

## 使用说明

1. **下载资源文件**：请从本仓库下载所需的资源文件，包括代码文件和数据集文件。
2. **安装依赖**：确保您的开发环境已安装所需的依赖库。
3. **运行测试**：使用 `test_unseen_sent.py` 脚本对对话系统进行测试，并查看生成的报告。

## 注意事项

- 本资源文件仅供学习和研究使用，请勿用于商业用途。
- 在使用过程中，请确保遵守相关法律法规。

## 贡献

欢迎对本仓库进行贡献，包括但不限于代码优化、数据集扩展等。请通过提交Pull Request的方式进行贡献。

## 许可证

本资源文件遵循MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[法律对话系统数据集](https://pan.quark.cn/s/3cc2da4d0797)