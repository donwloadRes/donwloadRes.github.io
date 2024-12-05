---
layout: post
title: "Windows Server 2019安装NET Framework 35解决方案"
date:   2023-06-26
tags: [NET,Framework,安装,3.5,Windows]
comments: true
author: admin
---
# Windows Server 2019安装.NET Framework 3.5解决方案

在部署Windows Server 2019服务器或安装特定软件（如数据库软件）过程中，用户可能会遇到因缺少.NET Framework 3.5而导致的安装失败问题。这是因为Windows Server 2019默认并未启用或包含此版本的.NET Framework。为了解决这一常见问题，本仓库提供了必要的SxS（Side-by-Side）文件，以便用户能够通过指定备用源路径的方式成功安装.NET Framework 3.5。

### 解决步骤：

1. **下载资源**：首先，从本仓库下载提供的.sxs文件夹。这个文件夹包含了安装.NET Framework 3.5所需的组件。

2. **开启Server Manager（服务器管理器）**：登录到您的Windows Server 2019，打开“服务器管理器”。

3. **添加角色和功能**：点击“管理”菜单，然后选择“添加角色和功能”。

4. **安装类型**：保持默认的基于角色或基于功能的安装，并单击“下一步”。

5. **选择目标服务器**：如果需要，选择目标服务器（通常是本地服务器），然后点击“下一步”。

6. **选择功能**：在列表中找到并勾选“.NET Framework 3.5 功能”。通常，您不需要勾选子选项。

7. **指定源文件**：由于该功能未直接包含在系统镜像中，安装程序会要求提供源文件路径。此时，浏览至您下载的.sxs文件所在的目录，选择该文件夹作为来源。

8. **确认并安装**：检查信息无误后，点击“安装”，等待过程完成。

9. **验证安装**：安装完成后，可以通过运行命令提示符输入`net stop wuauserv & net start wuauserv`以重启Windows Update服务，随后可使用“控制面板”验证.NET Framework 3.5是否已成功安装。

请注意，确保在整个过程中具有足够的管理员权限，以避免任何权限相关的问题。通过本仓库提供的资源，您可以有效解决Windows Server 2019上安装.NET Framework 3.5的难题，顺利完成必要的系统配置。

## 下载链接

[WindowsServer2019安装.NETFramework3.5解决方案](https://pan.quark.cn/s/dfd5a75846aa)