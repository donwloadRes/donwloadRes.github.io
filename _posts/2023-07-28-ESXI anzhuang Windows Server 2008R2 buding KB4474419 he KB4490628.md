---
layout: post
title: "ESXI 安装 Windows Server 2008R2 补丁 KB4474419 和 KB4490628"
date:   2023-03-18
tags: [补丁,安装,KB4474419,KB4490628,VMware]
comments: true
author: admin
---
# ESXI 安装 Windows Server 2008R2 补丁 KB4474419 和 KB4490628

## 简介

本仓库提供了一个资源文件，包含补丁 **KB4474419** 和 **KB4490628**，用于解决在 VMware ESXI 上安装 Windows Server 2008R2 时无法安装 VMware Tools 的问题。

## 问题描述

在 VMware ESXI 上安装 Windows Server 2008R2 时，可能会遇到无法安装 VMware Tools 的情况。这个问题通常是由于系统缺少必要的更新补丁导致的。通过安装本仓库提供的补丁 **KB4474419** 和 **KB4490628**，可以有效解决这一问题。

## 使用方法

1. **下载补丁文件**：
   - 从本仓库中下载补丁文件 `KB4474419.msu` 和 `KB4490628.msu`。

2. **安装补丁**：
   - 将下载的补丁文件上传到你的 Windows Server 2008R2 虚拟机中。
   - 打开命令提示符（以管理员身份运行），然后依次执行以下命令来安装补丁：
     ```bash
     wusa KB4474419.msu /quiet /norestart
     wusa KB4490628.msu /quiet /norestart
     ```
   - 安装完成后，重启虚拟机。

3. **验证安装**：
   - 重启后，尝试重新安装 VMware Tools，确认问题是否已解决。

## 注意事项

- 在安装补丁之前，建议备份重要数据，以防万一。
- 如果系统已经安装了其他更新，请确保这些更新与本补丁兼容。

## 贡献

如果你有任何改进建议或发现了其他相关问题，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的资源文件遵循 [MIT 许可证](LICENSE)。

## 下载链接

[ESXI安装WindowsServer2008R2补丁KB4474419和KB4490628](https://pan.quark.cn/s/2e635750a65d)