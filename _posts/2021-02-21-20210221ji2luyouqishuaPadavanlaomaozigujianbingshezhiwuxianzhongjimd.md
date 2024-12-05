---
layout: post
title: "极2路由器刷Padavan老毛子固件并设置无线中继"
date:   2023-02-26
tags: [固件,Padavan,路由器,无线,刷入]
comments: true
author: admin
---
# 极2路由器刷Padavan(老毛子)固件并设置无线中继

本资源文件详细介绍了如何将极2路由器（型号HC5761）刷入Padavan（老毛子）固件，并设置无线中继功能。通过刷入Padavan固件，用户可以实现更高级的路由器功能，如无线中继、去广告、云储存、QOS等。

## 主要步骤

1. **准备软件和固件**
   - 下载Winscp、putty、引导加载器breed-mt7620-hiwifi-hc5761.bin、Padavan固件RT-AC51U-GPIO-12-ji2-128M_3.4.3.9-099.trx。

2. **开通极2路由的Root权限**
   - 通过官方申请root权限，步骤包括登录路由器后台、申请开发者模式、验证手机短信和绑定微信。

3. **刷引导加载器Breed**
   - 使用Winscp将breed-mt7620-hiwifi-hc5761.bin上传到路由器的/tmp目录，然后使用putty登录路由器并执行刷入命令。

4. **刷Padavan固件**
   - 路由器断电后按住RST键通电，进入Breed Web恢复控制台，选择并上传Padavan固件进行刷入。

5. **设置无线中继**
   - 登录极2路由后台，设置无线AP工作模式为AP-Client+AP，选择LAN bridge模式，确保与主路由在同一网段内，关闭DHCP服务。

## 注意事项

- 刷机有风险，请确保备份重要数据。
- 刷入Padavan固件后，后台默认IP地址为192.168.123.1，用户名和密码均为admin。
- 设置无线中继时，确保极2路由的IP地址不在主路由的DHCP范围内，避免冲突。

通过以上步骤，您可以成功将极2路由器刷入Padavan固件并设置无线中继，实现更稳定和功能丰富的网络环境。

## 下载链接

[极2路由器刷Padavan老毛子固件并设置无线中继](https://pan.quark.cn/s/95ccc430bc2b)