---
layout: post
title: "SX1268官方驱动（含SX1278）"
date:   2021-04-14
tags: [示例,LoRaWAN,LoRaMac,终端设备,Class]
comments: true
author: admin
---
# SX1268官方驱动（含SX1278）

本资源库致力于提供一个LoRaWAN端点栈实现的示例。项目包含三个活跃分支，以满足不同开发需求和标准兼容性。`master`分支提供最新的稳定代码版本(v4.4.2)，支持LoRaWAN规范v1.0.3及LoRaWAN区域参数v1.0.3revA，全面实现了Class A、B和C终端设备类别。`develop`分支则展示了即将发布的新特性（里程碑4.4.3），同样基于相同的规范版本，并保持全部类别的终端设备实现。而`feature/5.0.0`分支则是针对LoRaWAN规范v1.1及LoRaWAN区域参数v1.1rB的前瞻版本，同样全面支持所有终端设备类别。

此项目不仅提供了包括SX1272/73, SX1276/77/78/79以及SX1261/2在内的无线电驱动程序，还特别包含了针对SX1268（同时适用于SX1278）的官方驱动。针对每一个目前支持的平台，都有相应的示例应用程序：

- **LoRaMac/classA**: Class A终端设备的示例应用。
- **LoRaMac/classB**: Class B终端设备的示例应用。
- **LoRaMac/classC**: Class C终端设备的示例应用。
- **LoRaMac/fuota-test-01**: FUOTA测试场景01的终端设备示例应用。
- **LoRaMac/periodic-uplink-lpp**: 支持Class A/B/C的终端设备示例，周期性地使用Cayenne LPP协议上行数据。
- **ping-pong**: 点对点RF链路的示例应用。
- **rx-sensi**: 用于测量无线电接收灵敏度的应用程序，利用RF发生器。
- **tx-cw**: 展示如何生成RF连续波传输的示例应用。

每个LoRaWAN应用示例（如LoRaMac/classX）均内置了LoRa Alliance的LoRaWAN认证协议实现。此外，LoRaWAN栈的API文档可访问[LoRaMac-doc](http://stackforce.github.io/LoRaMac-doc/)查看。（注：此处按要求不放置实际链接，请手动查找访问。）

此资源对于开发基于SX1268或SX1278等系列芯片的LoRaWAN设备至关重要，无论是研究最新标准还是进行产品开发，都能找到详尽的资料和技术支持。

## 下载链接

[SX1268官方驱动含SX1278](https://pan.quark.cn/s/156ecaa4c7d5)