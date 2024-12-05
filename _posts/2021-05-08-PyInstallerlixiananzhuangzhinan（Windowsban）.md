---
layout: post
title: "PyInstaller离线安装指南（Windows版）"
date:   2021-05-01
tags: [Python,PyInstaller,离线,安装,Windows]
comments: true
author: admin
---
# PyInstaller离线安装指南（Windows版）

## 概述

针对需要在无网络环境下的Windows系统中安装PyInstaller的用户，本仓库提供了一份完整的离线安装包。PyInstaller是一款强大的Python脚本打包工具，能够将Python程序及其依赖转换成独立的可执行文件，适用于多种操作系统平台。对于那些因安全策略或特殊环境限制而无法直接访问互联网的计算机而言，此离线安装包显得尤为实用。

## 环境需求

- **操作系统**: Windows 7/8/10 或 Windows Server 2012 R2及以上版本
- **Python**: 已安装Python 3.6至3.9之间的任意版本（推荐最新稳定版）

## 使用步骤

1. **下载离线包**：从本仓库下载提供的离线安装包到您的本地计算机。
   
2. **确保Python环境**：确认您的机器上已正确安装了Python，并通过命令行输入`python --version`或`py --version`来验证Python的版本。

3. **关闭所有Python进程**：在安装之前，请确保没有运行任何Python应用程序或解释器，以避免潜在的文件锁定问题。

4. **执行安装**：
   - 解压缩下载的离线安装包。
   - 打开命令提示符（CMD）或 PowerShell 作为管理员权限运行。
   - 导航到解压后的目录，那里应该包含`pip install`命令能识别的`.whl`文件。
   - 运行安装命令，例如，如果文件名为`PyInstaller-X.X.X-py3-none-any.whl`，则输入:
     ```
     pip install PyInstaller-X.X.X-py3-none-any.whl
     ```

5. **验证安装**：安装完成后，可以通过命令行输入`pyinstaller --version`来检查PyInstaller是否成功安装及其版本号。

## 注意事项

- 请根据您Python的位数（32位或64位）选择对应的安装包。
- 安装过程中如遇到权限问题，确保以管理员身份运行命令行工具。
- 此离线包的PyInstaller版本可能随时间更新，请定期检查是否有新版本可供升级。

通过遵循上述步骤，您便能在没有网络连接的情况下，在Windows环境下成功安装并开始使用PyInstaller进行Python应用的打包工作。

## 下载链接

[PyInstaller离线安装指南Windows版](https://pan.quark.cn/s/e736bc2e5f77)