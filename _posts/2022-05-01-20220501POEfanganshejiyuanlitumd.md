---
layout: post
title: "POE 方案设计原理图"
date:   2024-04-02
tags: [POE,原理图,以太网,方案设计,传输]
comments: true
author: admin
---
# POE 方案设计原理图

## 资源描述

本仓库提供了一份名为“POE 方案设计原理图”的资源文件，该文件详细描述了如何利用局域网电缆中未被使用的线对来传输直流电。在10M/100M以太网中，通常只使用电缆中的两对电线来传输数据，而剩余的两对电线则可以被用来传输电力。这种设计充分利用了现有网络基础设施，减少了额外的布线需求。

然而，需要注意的是，在1000M以太网中，所有四对电线都被用来传输数据，因此无法再采用这种方式来传输电力。在这种情况下，需要采用其他技术来实现电力传输。

## 适用场景

- 适用于10M/100M以太网环境，利用未使用的线对传输电力。
- 适用于需要减少布线复杂性的网络部署场景。

## 注意事项

- 该方案不适用于1000M以太网环境。
- 在实施前，请确保网络设备支持相应的POE技术。

## 使用方法

1. 下载本仓库中的“POE 方案设计原理图”文件。
2. 根据原理图进行网络布线和设备配置。
3. 确保所有设备支持POE技术，并正确连接。

## 贡献

如果您有任何改进建议或发现了错误，欢迎提交Issue或Pull Request。

## 许可证

本资源文件遵循MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[POE方案设计原理图](https://pan.quark.cn/s/7e2cd5c4f072)