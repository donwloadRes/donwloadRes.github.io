---
layout: post
title: "两款常用的 MQTT 调试工具"
date:   2020-04-12
tags: [MQTT,测试,客户端,支持,MQTTBox]
comments: true
author: admin
---
# 两款常用的 MQTT 调试工具

本文介绍了MQTT协议及其关键特性，并详细讲解了两个常用的MQTT客户端工具——MQTTBox和MQTT.fx。MQTTBox支持全面的协议，包括WebSocket，提供负载测试功能，而MQTT.fx则具有美观的界面和JS脚本支持。两者都可用于测试MQTT服务器的性能，选择使用取决于具体需求。

## 一、前言

我们可以使用 MQTT 客户端来测试 MQTT 的通讯功能，这里介绍常用的两款工具 MQTTBox 和 MQTT.fx。

## 二、预备知识

MQTT（MQ Telemetry Transport）协议是 IBM 公司在 1999 年开发的轻量级网络协议，它有三个主要特点：
1. 采用二进制的消息内容编码格式，所以二进制数据、JSON 和图片等负载内容都可以方便传输。
2. 协议头很紧凑，协议交互也简单，保证了网络传输流量很小。
3. 支持 3 种 QoS（Quality of Service，服务质量）级别，便于应用根据不同的场景需求灵活选择。

这三个特点让 MQTT 协议非常适合计算能力有限、网络带宽低、信号不稳定的远程设备，所以它成为了物联网系统事实上的网络协议标准。

## 三、MQTTBox

### 1. 介绍
MQTTBox 支持全面的协议，包括 TCP、TLS、WebSocket 和 Secure Web Sockets。它具有以下特点：
- 支持发布和订阅多个主题。
- 支持主题的单级和多级订阅。
- 支持 MQTT 负载测试。
- 支持并发测试实例，为同一个测试用例创建最多10个实例。
- 实时查看测试进程，测试结果能以图表展示。

### 2. 下载
MQTTBox 支持在 Windows、Mac 和 Linux 上面运行，我们到其官网选择合适的版本下载安装即可。

### 3. 入门使用
前提：已启动 MQTT 服务器。
点击 Create MQTT Client 按钮来创建一个 MQTT 客户端。接下来对 MQTT 客户端进行配置，主要是配置好协议端口、连接用户名密码和 QoS 即可。

### 4. 负载测试
测试参数和测试过程可以根据具体需求进行配置，测试结果展示比较直观。

## 四、MQTT.fx

### 1. 介绍
MQTT.fx 支持 TCP 和 TLS 协议，具有以下特点：
- 界面美观，操作便捷。
- 基于 Java 开发，支持代理。
- 通过 Nashorn Engine 的 JS 脚本支持。
- 全平台支持，Broker 状态检测（HiveMQ & mosquitto）。
- 操作日志查看，payload 的格式解析：文本、JSON、HEX、Base64、Sparkplug。

### 2. 下载
下载地址：http://www.jensd.de/apps/mqttfx/1.7.1/

### 3. 入门使用
点击 ⚙ 按钮来创建一个 MQTT 客户端。接下来对 MQTT 客户端进行配置，主要是配置好协议端口、连接用户名密码和 QoS 即可。

### 4. JS 脚本
MQTT.fx 支持通过 JS 脚本进行更复杂的操作，如发布消息、订阅主题等。

## 总结

MQTTBox 和 MQTT.fx 都是强大的 MQTT 客户端工具，适用于测试 MQTT 服务器的性能。选择使用哪个工具取决于具体需求，如是否需要 WebSocket 支持、是否需要负载测试功能等。

## 下载链接

[两款常用的MQTT调试工具分享](https://pan.quark.cn/s/d4e264e3c568)