---
layout: post
title: "Windows Server 2012上安装NET Framework 35"
date:   2020-03-10
tags: [安装,界面,点击,服务器,NET]
comments: true
author: admin
---
# Windows Server 2012上安装.NET Framework 3.5

## 简介

本资源文件提供了在Windows Server 2012上安装.NET Framework 3.5的详细步骤和所需文件。通过本指南，您可以顺利完成.NET Framework 3.5的安装，解决在安装过程中可能遇到的问题。

## 安装步骤

1. **下载.NET 3.5安装包**：首先，下载.NET 3.5安装包，并将其解压到您希望安装的位置（例如：C盘下的WIN2012R2_Net3.5文件夹）。

2. **进入服务器管理器**：在Windows Server 2012服务器桌面上，点击任务栏的“服务器管理器”。

3. **添加角色和功能**：在服务器管理器界面中，点击“添加角色和功能”。

4. **进入添加角色和功能向导**：在添加角色和功能向导界面中，直接点击“下一步”。

5. **选择安装类型**：在安装类型界面中，使用默认设置，直接点击“下一步”。

6. **选择服务器**：在服务器选择界面中，使用默认设置，直接点击“下一步”。

7. **选择服务器角色**：在服务器角色选择界面中，选择“Web服务（IIS）”。

8. **添加功能**：在弹出的对话框中，选择“添加功能”。

9. **继续选择角色**：回到服务器角色选择界面，直接点击“下一步”。

10. **选择功能**：在功能添加界面中，选择“.NET Framework 3.5 功能”，完成后点击“下一步”。

11. **进入Web服务器角色界面**：在Web服务器角色界面中，直接点击“下一步”。

12. **选择角色服务**：在角色服务界面中，使用默认设置，直接点击“下一步”。

13. **确认安装内容**：在确认安装所选内容界面中，选择左下角的“指定备用源路径”（注意：必须指定.NET 3.5的安装路径，否则会导致安装不成功）。

14. **设置备用源路径**：在弹出的对话框中，在路径设置中填写安装路径（注意：此路径填写刚解压文件所在的位置），完成后点击“确定”。

15. **开始安装**：回到确认界面，在界面中点击下方的“安装”，进入安装步骤。

16. **等待安装完成**：等待系统自动安装，安装完成后，可以在进度条看到提示功能安装已经成功了，接着点击下方的“关闭”，退出安装界面。

## 注意事项

- 确保指定的备用源路径正确，否则可能导致安装失败。
- 如果安装过程中遇到问题，请参考提供的描述文章中的详细步骤和解决方案。

通过以上步骤，您应该能够成功在Windows Server 2012上安装.NET Framework 3.5。

## 下载链接

[WindowsServer2012上安装.NETFramework3.5分享](https://pan.quark.cn/s/8089252f899b)