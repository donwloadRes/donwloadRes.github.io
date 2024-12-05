---
layout: post
title: "Linux虚拟机网络配置-桥接网络配置"
date:   2022-10-28
tags: [虚拟机,网络,桥接,Linux,配置]
comments: true
author: admin
---
# Linux虚拟机网络配置-桥接网络配置

## 简介

本文档旨在指导用户如何在虚拟环境中配置Linux系统的桥接网络，以实现虚拟机与物理主机以及外部网络的直接通信。桥接网络允许虚拟机如同一台独立的物理机一样直接连接到物理网络，从而可以被分配一个独立的IP地址，并能够与网络中的其他设备直接交互。

## 适用范围

- 虚拟化软件：如VirtualBox、VMware等。
- 操作系统：主要针对Linux发行版（如Ubuntu、CentOS等）作为虚拟机 guest OS。

## 配置步骤

### 1. 打开虚拟机设置

- 启动你的虚拟机软件，选择你想要配置的Linux虚拟机。
- 进入“设置”或类似命名的菜单。

### 2. 选择网络适配器模式

- 在“网络”设置选项中，找到“网络适配器”或类似的条目。
- 设置网络连接模式为**桥接网卡**（Bridge Adapter）。这将使虚拟机直接接入物理主机的网络接口。

### 3. 选择物理网卡

- 如果有多个物理网卡，从下拉列表中选择你想桥接到的物理网络接口，通常是与互联网连接的那个。

### 4. 在Linux虚拟机内进行配置

#### 自动获取IP

1. **对于Debian/Ubuntu系**，打开终端，输入：
   ```
   sudo dhclient -r
   sudo dhclient ens33    # “ens33”是常见的虚拟网卡名称，具体名称可能不同，请根据实际情况替换。
   ```

#### 静态IP配置

如果需要静态IP地址，你需要编辑网络配置文件，例如，在Ubuntu中：

1. 找到对应的网络配置文件，通常位于`/etc/network/interfaces`（对于较新版本的系统，可能是使用Netplan或NetworkManager配置，请参考相应文档）。
2. 编辑文件，添加或修改如下内容：
   ```
   auto ens33          # 替换为正确的网卡名
   iface ens33 inet static
       address 192.168.1.x   # 请替换为你的静态IP地址
       netmask 255.255.255.0
       gateway 192.168.1.1   # 网关地址
       dns-nameservers 8.8.8.8 8.8.4.4       # DNS服务器地址
   ```

3. 保存更改并重启网络服务：
   ```
   sudo systemctl restart networking
   ```

或如果是使用Netplan配置，则在`/etc/netplan/`目录下编辑或创建.yaml文件来定义静态IP。

### 5. 测试连接

- 使用命令`ping google.com`测试网络是否正常工作。成功返回表明配置完成。

## 注意事项

- 确保物理主机的防火墙和虚拟机的防火墙规则允许必要的网络流量。
- IP地址应遵循同一子网内的有效范围，避免与其他设备冲突。
- 某些企业级网络环境可能需要额外的网络策略配置，比如VLAN设置。

通过以上步骤，你可以成功地配置Linux虚拟机的桥接网络，使其无缝融入到物理网络环境中。祝配置顺利！

## 下载链接

[Linux虚拟机网络配置-桥接网络配置](https://pan.quark.cn/s/8e89f424856b)