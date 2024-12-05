---
layout: post
title: "VMware Horizon 8 安装部署指南（六）：部署Connection服务器"
date:   2021-05-12
tags: [Connection,服务器,配置,部署,VMware]
comments: true
author: admin
---
# VMware Horizon 8 安装部署指南（六）：部署Connection服务器

本资源文件提供了VMware Horizon 8安装部署的第六部分内容，重点介绍了如何部署Connection服务器。Connection服务器是VMware Horizon 8中的关键组件，负责管理和连接用户与虚拟桌面资源。

## 内容概述

1. **准备工作**：
   - 准备一台Windows Server 2016机器，进行基本配置，包括更改IP、计算机名称、加入域等。
   - 将所需软件上传到机器。

2. **软件下载**：
   - 提供VMware Horizon Connection Server的下载地址。

3. **安装步骤**：
   - 以管理员身份运行安装程序。
   - 选择标准服务器配置，IPV4，后期可配置HA高可用性。
   - 输入用于恢复的密码和提示。
   - 自动配置防火墙。
   - 默认使用授权用户。
   - 不加入体验计划。
   - 开始安装，完成后运行Connection服务器。

4. **登录与配置**：
   - 使用Edge或Chrome浏览器登录Connection服务器。
   - 输入用户名和密码进行登录。
   - 编辑许可证，输入许可密钥。
   - 配置vCenter Server，添加VCenter的地址、登录用户名和密码。
   - 处理证书问题，接受证书。
   - 配置Composer，选择独立的View Composer，输入Composer服务器地址、用户名和密码。
   - 处理Composer证书问题，接受证书。
   - 配置主机缓存大小，提交并完成配置。

5. **完成部署**：
   - 在设置中查看配置成功的信息，完成Connection服务器的部署。

## 注意事项

- 确保所有配置步骤严格按照指南进行，避免出现配置错误。
- 在处理证书问题时，务必仔细查看证书信息，确保安全。
- 配置完成后，进行全面测试，确保Connection服务器正常运行。

通过本指南，您将能够顺利完成VMware Horizon 8中Connection服务器的部署，为后续的虚拟桌面管理打下坚实基础。

## 下载链接

[VMwareHorizon8安装部署指南六部署Connection服务器](https://pan.quark.cn/s/d973e01076e3)