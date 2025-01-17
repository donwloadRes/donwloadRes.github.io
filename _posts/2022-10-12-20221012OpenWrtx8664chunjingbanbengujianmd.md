---
layout: post
title: "OpenWrt x8664 纯净版本固件"
date:   2020-06-13
tags: [网卡,AX,固件,200,无线]
comments: true
author: admin
---
# OpenWrt x86-64 纯净版本固件

## 简介

本仓库提供了一个自编译的OpenWrt x86-64固件，适用于x86-64架构的设备。该固件支持Intel AX 201无线网卡开启Master模式，并且加入了AX 200和AX 201网卡的驱动。理论上，该固件也支持AX 200和AX 210无线网卡，但由于我手头没有多余的网卡，仅测试过AX 201网卡。

## 主要特性

- **支持Intel AX 201无线网卡**：固件中集成了AX 201网卡的驱动，并支持开启Master模式。
- **兼容AX 200和AX 210网卡**：虽然未经过实际测试，但理论上该固件也支持AX 200和AX 210无线网卡。
- **纯净版本**：该固件为纯净版本，未添加任何第三方插件，适合需要自定义配置的用户。

## 使用说明

1. **下载固件**：请从本仓库的发布页面下载最新版本的固件文件。
2. **刷入固件**：将下载的固件文件刷入到你的x86-64设备中。
3. **配置网络**：刷入固件后，根据你的网络环境配置无线或有线网络。
4. **测试无线网卡**：如果你使用的是AX 200或AX 210网卡，请测试其功能是否正常。

## 注意事项

- 该固件为自编译版本，使用前请确保你了解OpenWrt的基本操作。
- 由于未对AX 200和AX 210网卡进行实际测试，使用这些网卡时可能会遇到问题，请自行解决。
- 如果你有其他无线网卡的需求，可以自行编译或联系我进行定制。

## 反馈与支持

如果你在使用过程中遇到任何问题或有任何建议，欢迎在仓库中提交Issue，我会尽快回复并提供帮助。

---

希望这个固件能帮助你更好地使用OpenWrt！

## 下载链接

[OpenWrtx86-64纯净版本固件](https://pan.quark.cn/s/2ee97c54f066)