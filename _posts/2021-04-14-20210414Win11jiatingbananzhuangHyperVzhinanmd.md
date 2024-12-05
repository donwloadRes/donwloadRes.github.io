---
layout: post
title: "Win11家庭版安装HyperV指南
date   20211102
tags Hyper家庭版安装Windowshyper
comments true
author admin

 Win11家庭版安装HyperV指南

 资源简介
本文档为您提供详细指导帮助那些使用Windows 11家庭版的用户成功安装HyperVHyperV是一款强大的虚拟机管理程序通常预装在Windows的专业版及以上版本中然而对于家庭版用户来说原生并不支持此功能幸运的是通过一些技巧您也可以在家庭版上激活并使用HyperV

 文章来源
本指南基于CSDN博客httpsblogcsdnnetalang10241024articledetails136431123上的文章该文提供了详细的步骤和一个简便的CMD脚本使得家庭版用户无需升级系统即可享受HyperV带来的便利

 安装前提条件
 确保您的CPU支持虚拟化技术并在BIOS中已启用
 操作系统应为最新状态以便兼容所有必需的组件

 安装步骤简述
1 准备脚本 首先您需要下载或手动创建一个批处理文件bat其中包含必要的Dism命令来添加HyperV功能
   
   batch
   pushd dp0
   dir b SystemRootservicingPackagesHyperV mum hypervtxt
   for f i in findstr i  hypervtxt 2nul do dism online norestart addpackageSystemRootservicingPackagesi"
date:   2021-11-02
tags: [Hyper,家庭版,安装,Windows,hyper]
comments: true
author: admin
---
# Win11家庭版安装Hyper-V指南

## 资源简介
本文档为您提供详细指导，帮助那些使用Windows 11家庭版的用户成功安装Hyper-V。Hyper-V是一款强大的虚拟机管理程序，通常预装在Windows的专业版及以上版本中。然而，对于家庭版用户来说，原生并不支持此功能。幸运的是，通过一些技巧，您也可以在家庭版上激活并使用Hyper-V。

## 文章来源
本指南基于[CSDN博客](https://blog.csdn.net/alang10241024/article/details/136431123)上的文章，该文提供了详细的步骤和一个简便的CMD脚本，使得家庭版用户无需升级系统即可享受Hyper-V带来的便利。

## 安装前提条件
- 确保您的CPU支持虚拟化技术，并在BIOS中已启用。
- 操作系统应为最新状态，以便兼容所有必需的组件。

## 安装步骤简述
1. **准备脚本**: 首先，您需要下载或手动创建一个批处理文件(`.bat`)，其中包含必要的Dism命令来添加Hyper-V功能。
   
   ```batch
   pushd "%~dp0"
   dir /b %SystemRoot%\servicing\Packages\*Hyper-V* mum >hyper-v.txt
   for /f %%i in ('findstr /i . hyper-v.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"
   del hyper-v.txt
   dism /online /enable-feature /featurename:Microsoft-Hyper-V-All /LimitAccess /ALL
   ```

2. **管理员权限运行**: 保存上述代码为`install_hyper-v.bat`，并以管理员身份运行这个批处理文件。
   
3. **系统重启**: 跟随提示，可能需要重启电脑以完成安装过程。

4. **验证安装**: 安装完成后，您可以通过Windows PowerShell或控制面板检查Hyper-V是否已成功启用。

## 注意事项
- 确保在整个过程中遵循屏幕上的指示。
- 若遇到错误，检查您的系统是否满足硬件要求，或尝试更新系统补丁。
- 安全软件有时可能会干预此过程，请暂时禁用它们以防冲突。

## 结语
借助这份指南，即便您是Windows 11家庭版的用户，也能顺利地安装并利用Hyper-V的强大功能，为您的开发、测试等场景提供极大便利。记得，安全始终是第一位的，确保任何操作都在了解风险的前提下进行。祝您安装顺利！

## 下载链接

[Win11家庭版安装Hyper-V指南](https://pan.quark.cn/s/5645a5ea3208)