---
layout: post
title: "亲测S905LS905LB安卓TV60通刷固件"
date:   2021-12-18
tags: [固件,S905L,刷机,开机,USB]
comments: true
author: admin
---
# 【亲测】S905L/S905L-B安卓TV6.0通刷固件

## 简介

本资源文件提供了一个适用于S905L和S905L-B芯片的安卓TV 6.0通刷固件。该固件经过亲测，可以在多种机型上成功刷入，并提供了一些额外的功能和优化。

## 固件特点

1. **通刷支持**：适用于S905L和S905L-B芯片的多种机型，包括R3300、MC8638S、MG101、B860AV2.1（wifi可能无法使用）、IPBS9505S、HM201等。
2. **自带TWRP**：固件自带TWRP Recovery，已删去原有root权限，如果需要root权限可以自行刷入supersu。
3. **Android TV全家桶**：开机时会遇到SetupWraith启动向导，需要连接一个有木弟子功能的wifi才能通过开机验证。
4. **遥控器兼容**：遥控器文件与原固件保持一致，亲测咪咕盒子遥控器和移动语音遥控器可用。
5. **线刷包**：本固件为线刷包，需要使用Amlogic USB Burning Tool进行刷机。
6. **CPU调度优化**：原固件的CPU调度是hotplug，使用起来有卡顿情况，修改为interactive以提升性能。

## 刷机步骤

1. **准备工作**：下载并安装Amlogic USB Burning Tool，准备好双公头USB线。
2. **进入线刷模式**：有些机型自带reset键，有的机型开机时持续按左键，或者是长按电源键之后插上电源触发线刷模式。中兴的盒子需要拆机短接。
3. **刷机操作**：打开USB烧录工具，加载固件，点击开始，将双公头USB线连接电脑和盒子，通电开机。
4. **首次开机**：开机需要5~10分钟，第一次可能会遇到wifi无法正常打开的情况，请关机再重启之。也可以在连上wifi之后通过adb禁用SetupWraith.apk进入桌面。

## 注意事项

- 刷机有风险，请确保备份重要数据。
- 刷机过程中请勿断电或拔线，以免造成设备损坏。
- 如果遇到问题，请参考刷机教程或联系技术支持。

## 更新日志

- 2023-06-29：首次发布，固件版本为安卓TV 6.0。

## 联系我们

如有任何问题或建议，请联系我们。

---

**免责声明**：本固件仅供学习和研究使用，请勿用于商业用途。刷机过程中造成的任何损失，作者概不负责。

## 下载链接

[亲测S905LS905L-B安卓TV6.0通刷固件分享](https://pan.quark.cn/s/0f79490a274d)