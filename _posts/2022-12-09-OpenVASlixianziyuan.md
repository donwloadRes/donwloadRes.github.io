---
layout: post
title: "OpenVAS离线资源"
date:   2020-12-25
tags: [OpenVAS,离线,Deb,Vulnerability,GVMD]
comments: true
author: admin
---
# OpenVAS离线资源

## 概述

本资源库提供了OpenVAS（开源漏洞评估系统）的离线安装必备组件，特别适用于没有稳定网络连接或者需要在隔离环境中部署OpenVAS的用户。该资源集合包括了Debian（Deb）格式的安装包、用于扫描的离线NVT（Network Vulnerability Tests）、SCAP（Security Content Automation Protocol）安全自动化协议相关数据、CERT（Computer Emergency Response Team）发布的安全响应数据，以及GVMD（Greenbone Vulnerability Manager Daemon）所需的数据文件。尤为重要的是，本资源库还包含了对上述部分内容的中文语言翻译，以帮助国内用户更好地理解和操作OpenVAS。

## 资源详情

- **Deb包**：包含了OpenVAS的核心组件及其依赖的Deb安装包，方便用户在基于Debian的Linux发行版上进行离线安装。
  
- **NVT (Network Vulnerability Tests)**：一组脚本和配置文件，用于执行针对网络服务的安全测试，此离线包确保即使在无网络情况下也能更新测试库。

- **SCAP 数据**：一种标准化方法来定义、测量及验证系统的安全性，适合进行自动化的合规性检查。

- **CERT 数据**：收集自全球计算机应急响应小组的重要安全公告和补丁信息，有助于及时了解并应对网络安全事件。

- **GVMD_DATA**：Greenbone Vulnerability Manager的专用数据集，包含漏洞定义、报告模板等，是管理OpenVAS扫描结果的关键组件。

- **中文语言翻译**：为了让国内用户更顺畅地使用OpenVAS，我们提供了界面和文档的部分中文翻译，以便于理解与配置。

## 使用指南

1. **下载资源**：首先从本仓库下载所有必需的压缩包到本地。
   
2. **离线安装**：将Deb包复制到目标Linux系统，并通过命令行使用`dpkg -i <package_name.deb>`命令进行安装。
   
3. **数据导入**：对于NVT、SCAP、GVMD_DATA等数据，通常需放置到OpenVAS指定的目录或通过GVMD管理工具进行导入。

4. **启用中文支持**：根据提供的说明，配置OpenVAS以使用中文界面或查阅中文文档。

5. **安全评估**：利用新安装和配置的OpenVAS进行网络漏洞扫描和安全管理。

## 注意事项

- 请确保所使用的OpenVAS版本与提供的资源兼容。
- 安装过程中可能需要解决依赖关系，请准备完整的Debian软件包环境或使用apt-get下载缺失的依赖（如果在线环境允许）。
- 中文翻译可能存在不完全或准确性问题，建议参考官方文档以获得最准确的信息。

通过这份详尽的离线资源，即便是新手用户也能在无网络的条件下顺利搭建和配置OpenVAS系统，增强个人或企业的网络安全防护能力。

## 下载链接

[OpenVAS离线资源](https://pan.quark.cn/s/fffe4a4e28be)